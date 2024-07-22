| 页面Pages | 字段Label | 释义 | 检查 | 来源 |
| - | - | - | - | - |
| 区块详情页 | Block Height | Also known as Block Number. The block height, which indicates the length of the blockchain, increases after the addition of the new block. | checked(sven) | - |
| / | Cell | CKB adopts cell model, which is more generic than UTXO model. A transaction destroys some outputs created in previous transactions and creates some new outputs. Every transaction's output is a cell. | checked(sven) | [transaction struc](https://github.com/nervosnetwork/rfcs/blob/master/rfcs/0022-transaction-structure/0022-transaction-structure.md#code-locating)  |
| / | Live Cell | A live cell is the one that appears as an output but not as an input in all the older transactions. A dead cell has already been used as an input in any older transaction. A transaction can only use live cells as inputs. | checked(sven) | [transaction struc](https://github.com/nervosnetwork/rfcs/blob/master/rfcs/0022-transaction-structure/0022-transaction-structure.md#code-locating) |
| / | Capacity | The Capacity in the cell is not only just the amount of the stored tokens, but it is also a limit on how many data the cell can store. That's where the name comes from, It is the storage capacity of the cell. | checked(sven) | [cell data](https://github.com/nervosnetwork/rfcs/blob/master/rfcs/0022-transaction-structure/0022-transaction-structure.md#cell-data.) |
| / | Capacity unit | The basic unit for capacity is shannon, a bigger unit CKByte, or just CKB is also used. 1 CKB equals 10**8 shannons.1 CKB equals 1 Byte, it means the cell can store 1 byte of information | checked(sven) | [Data Structure](https://docs.nervos.org/docs/reference/cell/#data-structure) |
| 区块详情页 | Transactions | The number of transactions in the block. | checked(sven) | - |
| 区块详情页 | Size | Block Size refers to the size of a block, typically used to describe the number of transactions within a block. The block size is actually determined by the block's gas limit. | checked(sven) | - |
| 区块详情页 | Cycles | Cycles are fees paid to miners based on the amount of computer resources that are used to verify a transaction. These are measured by CKB-VM during the execution of any smart contracts in a transaction. | checked(sven) | - |
| 区块详情页 | Proposal Transactions | In CKB,a proposal refers to the first step in the confirmation process of a transaction. NC-MAX splits the confirmation process into two steps: propose and commit. During the proposal step, a transaction is first proposed to the network. This involves broadcasting the transaction to the network and allowing it to propagate among the nodes. The proposal step gives more time for transaction propagation without slowing down block propagation.| checked(sven) | [NC-MAX](https://eprint.iacr.org/2020/1101.pdf) |
| 区块详情页 | Miner Reward | Native tokens that are paid to a miner in exchange for providing the computational resources required for mining. | checked(sven) | https://docs-old.nervos.org/glossary/glossary-general#mining-reward |
| 区块详情页 | Difficulty | A measurement of how difficult it is to solve the Proof of Work cryptographic puzzle required to create a block. Networks automatically adjust the difficulty to control the speed at which blocks are generated as mining participants enter and exit the network." | checked(sven) | https://docs-old.nervos.org/glossary/glossary-technical#difficulty | - | - |
| 区块详情页 | Nonce | In cryptography, a value that can only be used once. Nonce can refer to two things in blockchain context: 1. a proof-of-work nonce is the random value in a block satisfying the proof of work requirement; 2. an account nonce is a transaction counter in each account, which is used to prevent replay attacks. The nonce here refers to the first case.x| checked(sven) | [CKB Docs](https://docs.nervos.org/docs/basics/glossary/#nonce) |
| 区块详情页 | Uncle Count | The number of [uncle blocks](https://docs.nervos.org/docs/basics/glossary/#uncle) in the current block. | checked(sven) | - |
| 区块详情页 | Miner | A miner is a computer that provides computing power to validate transactions and create the blocks in the blockchain. |checked(sven) | https://docs-old.nervos.org/glossary/glossary-general#miner |
| 区块详情页 | Miner Message | 矿工对当前区块的留言。 | checked(sven) | - |
| 区块详情页 | Epoch | In CKB, an Epoch is a fixed period of time during which the difficulty level for Proof of Work (PoW) mining is held constant. The duration of an Epoch is set to 4 hours, so the actual Epoch interval is always **around** 4 hours, and all the blocks in the same Epoch share the same difficulty target. The difficulty adjustment algorithm aims to stabilize the orphan block rate at 2.5% by adjusting the difficulty level for each Epoch based on the average block time of the previous Epoch. The Epoch is used to ensure that the network remains secure and that miners are incentivized to continue mining the network. The Epoch concept is used in many other blockchain networks as well, and is an important component of the consensus mechanism. | checked(sven) | [CKB doc](https://docs.nervos.org/docs/basics/glossary#epoch) |
| 区块详情页 | Epoch Start Number | In CKB, Epoch Start Number refers to the block number at which a new Epoch begins. The Epoch Start Number is calculated based on the number of blocks that have been mined since the last Epoch started. Specifically, the Epoch Start Number is equal to the current block number minus the remainder of the current block number divided by the Epoch length. For example, if the current block number is 1000 and the Epoch length is 180 blocks, then the Epoch Start Number would be 1000 - (1000 % 180) = 940. The Epoch Start Number is used to determine when the difficulty level for Proof of Work (PoW) mining should be adjusted, and is an important component of the consensus mechanism in CKB. | checked(sven) | - |
| 区块详情页 | Block Index | In CKB, Block Index refers to the numerical index assigned to a block in the blockchain. The Block Index is a unique identifier for each block in the chain, and is used to order the blocks in the blockchain. The first block in the chain, also known as the Genesis Block, has a Block Index of 0, and each subsequent block is assigned the next sequential index. The Block Index is an important component of the blockchain, as it is used to maintain the integrity and security of the network by ensuring that all nodes on the network agree on the ordering of the blocks in the chain. | checked(sven) | [more info](https://github.com/nervosnetwork/rfcs/blob/9aef152a5123c8972de1aefc11794cf84d1762ed/rfcs/0027-block-structure/0027-block-structure.md#epoch-uint64) |
| 区块详情页 | Timestamp | In CKB, Timestamp refers to the timestamp of a block, which represents the time at which the block was created by a miner. However , the timestamp in the block header is an arbitrary value filled by the miner.| checked(sven),revised(Chenyu) | - |
| 区块详情页 | Transactions Root | In CKB, Transactions Root refers to the root of a Merkle tree that contains the transaction hashes of all the transactions included in a block. The Transactions Root is calculated by hashing together all of the transaction hashes in the Merkle tree, and is included in the block header as a way of verifying the integrity of the transactions in the block. The Transactions Root is used to ensure that all of the transactions in the block are valid and that none have been tampered with. It is also used to efficiently retrieve a specific transaction from a block, as the Merkle tree structure allows for quick verification of the transaction's inclusion in the block. The Transactions Root is an important component of the consensus mechanism in CKB. | checked(sven) | - |
| 区块详情页 | Cellbase for Block | The cellbase transaction of block N is sent to the miner of block N-11 as reward, learn more from our [Consensus Protocol](https://docs.nervos.org/docs/basics/concepts/consensus/) | checked(sven) | Current hint |
| 交易详情页 | Transaction Status | Transaction Status represent the status of current transaction, They are Pending, Comfirming and Rejected. | checked(sven) | - |
| 交易详情页 | CellDeps | CellDeps is one of dependency in the transaction data structure, it allows scripts in the transaction to access (read-only) referenced live cells. For more info, check about [Code Locating](https://github.com/nervosnetwork/rfcs/blob/master/rfcs/0022-transaction-structure/0022-transaction-structure.md#code-locating) | checked(sven) | [Dependencies](https://docs.nervos.org/docs/essays/dependencies/#how-dependencies-work) |
| 交易详情页 |OutPoint| The OutPoint is a reference type. The transaction uses OutPoint in inputs to reference the previously created cells instead of embedding them. |checked(sven)|[transaction struc](https://github.com/nervosnetwork/rfcs/blob/master/rfcs/0022-transaction-structure/0022-transaction-structure.md#code-locating)|
| 交易详情页 | OutPoint.TxHash | OutPoint.TxHash is a field that represents the transaction hash of a particular output Cell in a transaction. It's used to locate a cell with OutPoint.Index | checked(sven) | - |
| 交易详情页 | OutPoint.Index | OutPoint Index is the one of the params which are used to locate a Cell  | checked(sven) | - |
| 交易详情页 | DepType | DepType in CKB is a field in CellDep to differentiate the normal cells which provide the code directly, and the dep groups which is expanded to its members inside cell_deps. If the uint8 value is 0, the cell provide the code, if the uint8 value is 1, the cell includes a dep group. On the website, the DepType will show as code or dep_group.  | checked(sven) | [transaction struc](https://github.com/nervosnetwork/rfcs/blob/master/rfcs/0022-transaction-structure/0022-transaction-structure.md) |
| 交易详情页 | dep_group | dep_group is one selection of DepType.It is used to simplify the process of adding multiple dependencies to a transaction. | To be confirmed | [transaction struc](https://github.com/nervosnetwork/rfcs/blob/master/rfcs/0022-transaction-structure/0022-transaction-structure.md) |
| 交易详情页 | HeaderDeps | header_deps is one of dependency in the transaction data structure, it allow scripts in the transaction to access (read-only) data of referenced past block headers of the blockchain.| checked(sven) | [Dependencies](https://docs.nervos.org/docs/essays/dependencies/#how-dependencies-work) |
| 交易详情页 | Witness | Witness is a field in the CKB transaction structure that always contains the signature in a transaction| checked(sven) | [reference](https://github.com/nervosnetwork/ckb/blob/3de5a20ce60619927f41f81d9584cab9d39d1275/util/types/schemas/blockchain.mol#L114-L118) |
| 交易详情页 | Witnesses | Witnesses is an array of Witness that contains all the witnesses in a transaction. | checked(sven) | - |
| 交易详情页 | Lock Script | Lock Script in CKB is a script that is attached to a Cell's lock field. Every cell has a lock script.It is used to enforce certain conditions that must be met in order to spend the Cell's capacity. The Lock Script can be thought of as the Cell's "owner", as it defines the conditions under which the Cell's capacity can be spent. The Lock Script is executed by the CKB VM during the transaction verification process. | checked(sven) | - |
| 交易详情页 | Type Script | Type Script in CKB is a script that is attached to a Cell's type field. It is used to enforce additional validation rules on the Cell's data. The Type Script can be used to define custom data formats, or to implement more complex validation logic beyond what is possible with the Lock Script alone. The Type Script is executed by the CKB VM during the transaction verification process. Type script is optional. CKB run the type scripts in both inputs and outputs in a transaction.| checked(sven) | - |
| 交易详情页 | Capacity Usage | Capacity Usage shows how many capacity are declared and occupied. A transaction in CKB must create an output cell which occupied capacity is less than the cell capacity. | checked(sven) | - |
| 交易详情页 | deprecated addresses | Deprecated addresses in CKB refer to old address formats that are no longer recommended for use. These addresses were used in earlier versions of the CKB protocol, but have since been replaced by newer, more secure address formats. While deprecated addresses can still be used to send and receive transactions, it is recommended to use the newer address formats for improved security and compatibility with future versions of the CKB protocol. | checked(sven) | - | - | - |
| Script详情页 | Script Name | Script Name is the name of a Script. A script is a data structure represents a reference to a piece of on-chain runnable code. | checked(sven) | - |
| Script详情页 | Code Hash | Code Hash in CKB is a field in the Script data structure that represents the hash of the script code.Code Hash is used to locate the code of a script. The script code is compiled into RISC-V binary. The binary is stored as the data in a cell. When the hash_type is `type` , the Code Hash the hash of a type script, otherwise it is hash of the code| checked(sven) | - |
| Script详情页 | Hash Type | Hash Type in CKB is a field in the Script that specifies how the Code Hash field should be interpreted when looking for script code to run from cell dependencies. | checked(sven) | - |
| Script详情页 | Type Id | Type ID describes a way of using a special type script which can create a singleton type - there's only one live cell of this type. With Type ID nobody could create another code cell with the same type script hash, which makes it a useful companion to Type hash type. | checked(sven) | - |
| Script详情页 | Capacity of deployed cells | Capacity of deployed cells in CKB refers to the maximum amount of space (in bytes) that a cell can occupy on the Nervos CKB. The capacity field is one of the four fields in the Cell data structure, and limits the size of the cell. In order to store data on the CKB, a user must hold 1 CKB for every 1 byte of space that the cell occupies. This means that the capacity of a cell directly affects the amount of CKB that a user must hold in order to store data on the network. | checked(sven) | - |
| 地址详情页 | Live Cells | Live Cells in CKB refer to unspent cells on the blockchain that contain assets owned by users. They are similar to Unspent Transaction Outputs (UTXOs) in Bitcoin.| checked(sven) | - |
| - | Occupied | The total occupied CKB this address have invested in Nervos DAO | checked(sven) | - |
| - | Nervos DAO Deposit | The total CKB this address have deposited in Nervos DAO | checked(sven) | - |
| - | Nervos DAO Compensation | The total CKB this address have received from Nervos DAO | checked(sven) | - |
| - | Block Mined | The number of block this address has minted | checked(sven) | - |
| - | Args| In CKB, the public key information can be stored in the args field in the script structure. The args is used when script executing, e.g. the args can be a public key hash when the script is used to verify the owner of a private key| checked(sven) | - |
| 地址详情页 | Capacity Change | 该地址CKB余额在交易前后的变化值 | checked(sven) | - |
| NervosDAO | Estimated APC | Estimated Annual Percentage Compensation | checked(sven) | [APC calculation]([https://github.com/nervina-labs/ckb-nft-scripts](https://github.com/CipherWang/Nervos-DAO-RFC/blob/master/APC-Calculation.md#simple-calculation-formula)) |
| - | Secondary Issuance | Secondary Issuance in CKB refers to a fixed inflation schedule of 1.344 billion CKBytes per year that is used to incentivize miners, Nervos DAO users, and the Nervos Treasury for continued development. Unlike Base Issuance, Secondary Issuance is not distributed to everyone on the network, but rather targeted at users who occupy space on Nervos or hold their CKBytes outside of Nervos DAO. The CKBytes from Secondary Issuance are used to collect state rent and are distributed to miners who maintain the network (State Rent), Nervos DAO users, and the Nervos Treasury. CKBytes holders can lock their tokens in Nervos DAO to gain interest in a similar manner to staking on other platforms, which offsets the long-term inflationary effects of Secondary Issuance exactly, resulting in no loss of value over time. | checked(sven) | - |
| NFT Collection | CoTA | A kind of NFT protocal. A Compact Token Aggregator Standard for Extremely Low Cost NFTs and FTs. For more details, please check the [CoTA RDC](https://talk.nervos.org/t/rfc-cota-a-compact-token-aggregator-standard-for-extremely-low-cost-nfts-and-fts/6338)  | checked(sven) | - |
| NFT Collection | m-NFT | The NFT Type Scripts implement of RFC: Multi-purpose NFT Draft Spec on Nervos CKB. For more details, please check the [CKB-NFT-Script](https://github.com/nervina-labs/ckb-nft-scripts) | checked(sven) | - |
| NFT Collection | NRC 721 | NRC-721 is a token standard for non-fungible tokens (NFTs) on the Nervos CKB blockchain. It is similar to the ERC-721 token standard used on the Ethereum blockchain, and provides a common interface for creating, managing, and transferring unique digital assets on the CKB network. NRC-721 tokens are unique and non-interchangeable, which makes them ideal for representing assets such as collectibles, game items, and other unique digital assets. | checked(sven) | - |
| 图表页 | Hash Rate | Hash Rate is a measure of the computational power per second used when mining a cryptocurrency. It represents the number of hash operations that can be performed by a miner in a given period of time. In the context of blockchain, hash rate is used to measure the amount of work that is being done by the network to maintain the blockchain. A higher hash rate indicates that the network is more secure, as it becomes more difficult for a malicious actor to perform a 51% attack. | checked(sven) | - |