# Crypto exchange API (WIP)

To run: `go run` or `make run`

To test: `go test` or `make test`

To use the API use:
> POST bid limit order
> ```bash
> curl -d '{
>   "bid":true,
>   "size":10,
>   "price":10000,
>   "type":"LIMIT",
>   "market":"ETH"
> }' -X POST http://localhost:3000/order
> ```

> POST ask limit order
> ```bash
> curl -d '{
>   "bid":false,
>   "size":10,
>   "price":10000,
>   "type":"LIMIT",
>   "market":"ETH"
> }' -X POST http://localhost:3000/order
> ```

> POST ask limit order
> ```bash
> curl -d '{
>   "bid":false,
>   "size":1,
>   "type":"MARKET",
>   "market":"ETH"
> }' -X POST http://localhost:3000/order
> ```

> GET book
> ```bash
> curl http://localhost:3000/book/ETH | json_pp
> ```
