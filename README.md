# eth-client-exporter
A prometheus exporter for ethereum clients.

Exposed Metrics:

| Metric Name             | Labels     | Type  |
|-------------------------|------------|-------|
| eth_peers               | peer_state | Gauge |
| eth_block_transactions  | block_type | Gauge |
| eth_hashrate            | None       | Gauge |
| eth_gas_price           | None       | Gauge |
| eth_sync_block_pending  | None       | Gauge |
| eth_sync_block_earliest | None       | Gauge |
| eth_sync_block_latest   | None       | Gauge |
| eth_node_sync           | None       | Enum  |

## Usage

```commandline
./eth-client-exporter [HOST] [--target-port PORT] [--metrics-port PORT]
```

- `HOST` is the URL of the ethereum address **without** the port
- `--target-port` specifies the HOST's RPC port. Defaults to `8545`.
- `--metrics-port` specifies the port on which the exporter should serve
   its `/metrics` endpoint on the local machine. Defaults to `9999`.
