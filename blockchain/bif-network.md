## Overview
- Name: 星火链网
  - Local: BIF; International: ASTRON
- Official site: https://bitfactory.cn/
  - Weibo: https://weibo.com/u/7395287091
- Blockchain explorer: https://explorer.bitfactory.cn/
- Brief history:
  - 2020年8月正式启动部署
  - 2021年8月3日，中国信通院正式发布了“星火·链网”底层区块链平台BIF-Core
- Technology highlights
  - Architecture
    - 采用“1+N”主从链群架构，支持标识数据链上链下分布式存储功能，同时既可支持同构和异构区块链接入主链。
    - 超级节点: 作为国家链网顶层，提供关键资产、链群运营管理、主链共识、资质审核，并面向全球未来发展
    - 骨干节点:锚定主链，形成子链与主链协同联动
    - 超级节点和骨干节点具备监管功能，并协同运行监测平台，对整个链群进行合法合规监管
  - [Core technology: BIF][bif-overview]
    - Concensus: Optimized DPOS + PBFT
    - Storage engine: Rocksdb, TiKV
    - Smart contract languages: Solidity, Javascript
    - Performance: second-level transaction latency, 30k+ TPS
  - Wallet: Blockchain-based IDentifier (BID) 致力于为人、设备、虚拟对象等提供可信自主主权身份服务，能够使用户回收数据的所有权、控制权和使用权
  - Token: 星火令 (XHT)

[bif-overview]: https://bif-doc.readthedocs.io/zh-cn/3.0.0/quickstart/%E6%98%9F%E7%81%AB%E9%93%BE%E5%BA%95%E5%B1%82%E5%8C%BA%E5%9D%97%E9%93%BE%E5%B9%B3%E5%8F%B0%E4%BB%8B%E7%BB%8D.html

## Technical Details

- [General documentation][gen-doc]
  - [Blockchain design and implementation, e.g., transaction, concensus, storage, virtual machine][gen-doc-design]
  - [Blockchain-based identifier][gen-doc-bid]

[gen-doc]: https://github.com/caict-4iot-dev/bif-doc/
[gen-doc-design]: https://github.com/caict-4iot-dev/bif-doc/tree/2.0.0/docs/source/bifChain
[gen-doc-bid]: https://github.com/caict-4iot-dev/bif-doc/tree/2.0.0/docs/source/bid

### Smart Contract Development

- [Overview](https://bif-doc.readthedocs.io/zh-cn/3.0.0/contract/%E6%99%BA%E8%83%BD%E5%90%88%E7%BA%A6%E5%BC%80%E5%8F%91%E6%95%B4%E4%BD%93%E4%BB%8B%E7%BB%8D.html)
  - Supported smart contract languages: Solidity (modified), Javascript (modified), C/C++ (coming soon)
- Compiation of contracts written in Solidity: [Guide][smart-contract-solidity-guide], Compiler ([Nodejs package][smart-contract-solidity-compiler]; [source code][smart-contract-solidity-compiler-source])
- Deployment: [Guide][smart-contract-deployment-guide]
  - Use one of the SDKs in [Java][bif-sdk-java], [Go][bif-sdk-go], [Nodejs][bif-sdk-nodejs] and [C][bif-sdk-c]
  - Deploy to a sub-chain / main-chain via APIs
- [Examples](https://github.com/caict-4iot-dev/bif-contracts)

[smart-contract-solidity-guide]: https://bif-doc.readthedocs.io/zh-cn/3.0.0/contract/Solidity%E5%90%88%E7%BA%A6%E4%BB%8B%E7%BB%8D.html
[smart-contract-solidity-compiler]: https://www.npmjs.com/package/@bifproject/solc-bif
[smart-contract-solidity-compiler-source]: https://github.com/caict-4iot-dev/solc-js
[smart-contract-deployment-guide]: https://bif-doc.readthedocs.io/zh-cn/3.0.0/quickstart/%E4%BD%BF%E7%94%A8SDK%E5%BF%AB%E9%80%9F%E4%BD%93%E9%AA%8C%E6%98%9F%E7%81%AB%E9%93%BE.html
[bif-sdk-java]: https://bif-doc.readthedocs.io/zh-cn/3.0.0/instructions/JavaSDK%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E.html
[bif-sdk-go]: https://bif-doc.readthedocs.io/zh-cn/3.0.0/instructions/GoSDK%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E.html
[bif-sdk-nodejs]: https://bif-doc.readthedocs.io/zh-cn/3.0.0/instructions/NodejsSDK%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E.html
[bif-sdk-c]: https://bif-doc.readthedocs.io/zh-cn/3.0.0/instructions/CSDK%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E.html

### Wallet / Blockchain-based Identifier (BID)

- [Overivew documentation](https://bif-doc.readthedocs.io/zh-cn/bid/)
- How to get one? Apply through the [official wallet application](https://bitfactory.cn/szsf.html) and follow the [official guide to register one](https://bif-doc.readthedocs.io/zh-cn/1.0.0/tools/wallet.html)
  - [Obtain the token through application](https://bif-doc.readthedocs.io/zh-cn/3.0.0/quickstart/%E4%BD%BF%E7%94%A8SDK%E5%BF%AB%E9%80%9F%E4%BD%93%E9%AA%8C%E6%98%9F%E7%81%AB%E9%93%BE.html#id3)

### Infrastructure

#### 骨干节点

- [How to connect a 骨干节点 to a 超级节点?](https://bif-doc.readthedocs.io/zh-cn/1.0.0/business/main_node.html)
  - 获取数字身份 (BID) -> 节点申请 -> 底层链锚定 -> 同步业务数据

#### 超级节点

N/A

#### Testnet

- Endpoint: test.bifcore.bitfactory.cn:7053
- HTTPS and websocket
- [Quicknode setup using BIF docker image](https://bif-doc.readthedocs.io/zh-cn/1.0.0/app/qnode.html)

#### Sub-chain

- [List of sub-chains](https://test-cq-explorer.bitfactory.cn/subchain)
  - Concensus algorithms: CITA-BFT, DPOS+BFT, Raft, PBFT

#### Cross-chain

- [Standard adopted in BIF][bif-cross-chain-std]
- Integration with [AntChain][antchain-github] (from AntGroup)
  - [News](https://weibo.com/ttarticle/p/show?id=2309405026823464419579)
  - Tools: [Relayer][antchain-relayer], [Plugin server][antchain-plugin-server], [Plugin SDK][antchain-plugin-sdk]

[bif-cross-chain-std]: https://github.com/caict-4iot-dev/bif-rfcs/blob/main/RFCs/4-ADOPTED/%E6%98%9F%E7%81%AB%E9%93%BE%E7%BD%91RFC-009%EF%BC%9A%E6%98%9F%E7%81%AB%E9%93%BE%E7%BD%91%E8%B7%A8%E9%93%BE%E5%8D%8F%E8%AE%AE%E8%A7%84%E8%8C%83.md
[antchain-github]: https://github.com/AntChainOpenLabs
[antchain-relayer]: https://github.com/caict-4iot-dev/AntChainBridgeRelayer
[antchain-plugin-server]: https://github.com/caict-4iot-dev/AntChainBridgePluginServer
[antchain-plugin-sdk]: https://github.com/caict-4iot-dev/AntChainBridgePluginSDK

### Misc

- Consensus algorithm: [Xbft](https://github.com/caict-4iot-dev/Xbft/blob/main/docs/Hotstuff%E5%85%B1%E8%AF%86%E7%AE%97%E6%B3%95.md) ([source code](https://github.com/caict-4iot-dev/Xbft), [paper (PODC'19)](https://dl.acm.org/doi/10.1145/3293611.3331591))
- [Reports at ASTRON Ecology Conference 2024](https://weibo.com/ttarticle/p/show?id=2309405031846542180656)
