## 2. Developers

### 2.1. How do developers build on Arcology?

Developers can use their Ethereum toolchains like Truffle / Remix directly. They can also redeploy their contracts on the network. Arcology supports all standard Ethereum RPC interfaces. You don’t have to change anything, unless you want to write concurrent smart contracts, which will give significant speedup, but it is purely optional.

### 2.2. What are concurrent smart contracts?

Arcology allows multiple transaction calling the same contract simultaneously without causing any consistency related problems. This feature is unique to Arcology and especially useful for large-scale DApps.

### 2.3. Why do we need concurrent smart contracts in the first place?

The short answer is that if you want to build applications that can handle tens of thousands of calls per second, the concurrent smart contracts are the only answer.
All other scaling solutions only deal with inter-application parallelization, which basically means transactions calling different smart contracts may somehow get process in parallel by multiple sidechains or whatever. We call it inter-contract parallelization.

The type of solutions will bring some performance enhancement but totally incapable of handling huge influx of calls to the same contracts. Transactions calling the same contract are still processed in serial order. This is a serious shortfall for many popular applications.
On the contrary, Arcology can do both inter-contract and intra-contract parallelization. In Arcology, multiple calls to the same concurrent contracts are processed simultaneously.

### 2.4. How can we write concurrent contracts?

Concurrent contracts aren’t as difficult to write as them may sound. There is a developer’s guide to walk you through the process.
