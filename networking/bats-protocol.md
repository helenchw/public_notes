# Notes on BATS(TM) protocol

## Documentation on performance evaluation

Source: https://github.com/n-hop/bats-documentation/blob/main/README.md

- Improve the data transmittion over lossy network links.
- 'Classic' network topology: a linear chained network of single or multiple hosts
- Support single-hop and multi-hop. Multi-path network is a pending feature.
- Network metrics: bandwidth, latency, jitter, and loss rate.
- Packet loss models
  - Random
  - State: 4-state Markov chain
  - Gilbert-Elliot: Markov chain model with two states (good and bad); probabilities to transit between the two and loss rate in the two.
- Evaluation metrics
  - Throughput
  - Latency
  - Reliability = (packets received) / (packets sent)
  - Residual loss rate
     - This metric is not evaluated in the documentation.
- Evaluation results
  - Basic setup: Linear chained networks of 3 or 6 hops; Links are 300Mbps each; Packet loss are random.
  - Under no packet loss, BATS(TM) adds around 30% latency overhead (10ms over a 3-hop network with 5ms per-link latency) and some overhead in throughput (over a 6-hop network).
  - Under 2% or more per-link packet loss rates, BATS(TM) outperforms TCP and KCP in throughput and latency.
  - Under 10% or more per-link packet loss rates and a 6-hop network, BATS(TM) outperforms UDP in throughput.

### Remarks

- Why the throughput and latency results are presented under different network settings (6-hop and 3-hop)?

## Testing Suite, Oasis

Source: https://github.com/n-hop/oasis

- Protocols
  - BATS: https://github.com/n-hop/oasis/tree/main/bats
  - Only a binary release of the protocol is available, as the protocol is still close-source.
- Network topology and runtime environment 
  - Simulated using [Containernet](https://containernet.github.io/) (a tool that runs [Mininet](https://mininet.org/) with Docker containers instead of VMs)
  - Only support linear chained networks in the released code, see [the network configuration parser](https://github.com/n-hop/oasis/blob/main/src/containernet/linear_topology.py) and [the network configuration example](https://github.com/n-hop/oasis/blob/main/src/config/predefined.topology.yaml).
  - But the [general configuration parser](https://github.com/n-hop/oasis/blob/808eff17a1074e9b4d57b90d5dd8c19cad4a25a3/src/containernet/config.py#L27) suggests there might be a 'full version' that supports star, tree, butterfly and mesh networks.
- Interfaces for applications
  - The [diagram](https://github.com/n-hop/oasis/blob/main/bats/imgs/arch.png) suggests an IPC interface support, but no related documentation (or source code) is found in the repository.

### Remarks

N/A
