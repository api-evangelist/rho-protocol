---
name: Place and manage Rho X orders
description: Place, cancel, and manage orders and withdrawals on Rho X — requires a FullAccess credential.
api: openapi/rho-protocol-openapi-original.json
operations:
  - POST /orders
  - POST /orders/cancel
  - POST /orders/cancel-all
  - POST /users/withdrawals
---

# Place and manage Rho X orders

Trading and withdrawal operations are **write** operations and require a `FullAccess`
credential (Bearer access token or a `FullAccess` API key). A `ReadOnly` key returns `403`.
Base URL: `https://x.rho.trading/api/v1`.

## Steps

1. **Authenticate with FullAccess** — obtain a Bearer access token via `POST /auth-api/v1/login`, or use a `FullAccess` API key.
2. **Place an order** — `POST /orders` with body `dto.RestCreateOrderRequest`:
   - required: `symbol`, `orderType` (`limit` | `market`)
   - `side` (`buy` | `sell`), `price`, `quantity` (strings), `timeInForce` (`GTC` | `IOC`)
   - optional `clientOrderId` (string, ≤36 chars) for client-side tracking/deduplication
   - optional `flags: [close-position]`
3. **Cancel one** — `POST /orders/cancel` with `dto.RestCancelOrderRequest`.
4. **Cancel all** — `POST /orders/cancel-all` with `dto.RestCancelAllOrdersRequest`.
5. **Withdraw** — `POST /users/withdrawals` (`dto.RestWithdrawalRequest`) returns `202 Accepted` for asynchronous processing.

## Conventions & errors

- Set a unique `clientOrderId` per order so retries can be reconciled — there is no global Idempotency-Key header.
- Errors return a `{code, message, params}` envelope (`dto.ExternalError`), not RFC 9457.
- `400` invalid params, `403` insufficient scope, `429` rate limited (back off using `X-RateLimit-*` headers), `500` server error.
- Watch order state via the `user-orders` WebSocket private channel rather than polling.
