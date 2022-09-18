# An Introduction to Mining

<hr/>

### Intro

Hello again privacy fans.

Welcome to our second series; An Introduction to Mining.

We presume you have already [**Gotten to Grips with Monero**](https://www.youtube.com/watch?v=AKB4w-L5ECA&list=PLcyDcJ4lpDVBpsnI-fbkB-7O4M63VIA2g) before embarking on your mining journey. If you haven't, please check out our first video series!

In this two part series we'll be covering all the basic information you may need when embarking on your mining adventure.

This video will cover mining as a concept, the different ways you can mine and what to consider when buying hardware or preparing to mine Monero.

For those interested in getting into the economics of mining; be prepared for some maths!

Well, let's get into it.


### The Monero Protocol

To achieve its distributed consensus, Monero relies on proof-of-work (PoW) mining.

PoW is a form of cryptographic proof in which miners aim to prove to each other that they have achieved a certain amount of computational effort. This computational effort must satisfy conditions set by the networks current difficulty, the existing blockchain data and any new transnational data.

For a really good explanation of PoW and its practical use case, we suggest you take a look at the following video from [3Blue1Brown](https://yewtu.be/bBC-nXj3Ng4?t=669).

Monero is different from other protocols in a few ways, one of which is the pursuit of egalitarian mining, which aims to give the common person the ability to successfully mine for themselves. Those who believe in Monero's approach more seriously prescribe to Satoshi's vision of [one-CPU-one-vote](https://www.bitcoin.com/satoshi-archive/whitepaper/#4-proof-of-work).

To achieve this, Monero uses a hashing algorithm called [RandomX](https://www.getmonero.org/resources/moneropedia/randomx.html). This PoW algorithm is resistant to both GPUs and application-specific integrated circuits (ASICs), which means it's extremely impractical and expensive to build specialised hardware to mine Monero. 

Miners must hence use consumer and server grade hardware which allows users to compete much more fairly!

So what exactly are miners competing for?

Well, that would be the precious block reward.


### The Block Reward and Network Difficulty

Miners, which consist of both hardware and software, are constantly trying to calculate and prove that the hashes they have derived both represent the most work done and all the most recent valid transactions. 

Together, this information forms the next block in the block chain.

Block rewards are the new coins issued by the network for each successfully solved block. These coins, plus the transaction fees generated from spent outputs are awarded to the miner who mints that block!

The likelihood that any one miner is able to calculate the required hashes and hence solve the next block, is directly correlated to the number of hashes they can calculate per second (H/s). This is also known as the miners hashrate.

That being said, it may not necessarily be the miner with the largest hashrate who mints the next block. This is in part due to the complexity of the task at hand. There is in fact an element of luck in this process, as each and every hash has an equal and valid chance of satisfying the next block in the chain.

The Monero network aims to add a new block onto the chain approximately every 120 seconds, which is equal to around 720 blocks per day. To achieve this rate a balance is required to prevent miners from solving blocks too quickly or too slowly. This balance is called the network difficulty. 

The network difficulty is calculated by looking at the average block time from the last day, whilst also excluding random outliers, mainly the very slow or very fast blocks. The difficulty is hence adjusted accordingly. This difficulty value gives us an insight into the average number of hashes required, from which we can also infer our luck.

It's from this difficulty value that we can estimate the hashrate of the entire network. Taking the current network difficulty and then dividing it by the block target gives us this estimate. With a difficulty of 300G we can estimate the entire network hasrate to be around 2,5GH/s; 300GH ÷ 120s = 2,5GH/s.

The existence of the block reward incentives competition between miners and hence drives up the total hash rate of the network. That is typically until the cost of adding more hashing power is higher than the reward of obtaining that proportion of mined blocks. We emphasise 'typically', as die hard Monero fans will even mine at a loss during those bear market scenarios.

Likewise as Monero becomes more valuable, the total hash rate of the network should theoretically increase proportionately and hence become progressively more difficult and expensive.


### Network Security

Consensus, is the method by which judgement is cast and the state of the block chain is determined. For consensus to be reached, more than 50% of the network participants must agree on the state of the block chain.

Strictly speaking; miners are not only competing for the block reward and fees, but the right to mint the next block in the chain and to propagate their version of the block chain history.

Given that consensus is required by the Monero protocol, users are forced to consider the following; In the event that rule breaking and dishonest miners out number the rule abiding and honest ones, the legitimate block chain history will be broken.

In other words, the legitimate history can be broken by an individual or group of miners who control more than 50% of the hashing power of the network.

This may sound scary at first, but owning more that 50% of the hash rate at the time of making this video, is extremely expensive. 

For greater context; as of the 15^th of May 2022, the global hash rate of the Monero network is around 2,8 GH/s. One of the most powerful server grade CPUs currently available, retailing for around €6500 can achieve a hash rate of 100 kH/s. 

Just to start, the attacker would need more than 28000 of these CPUs costing over €182m. This is obviously quite a simple and brutal estimation and it may be simpler to hijack an existing pools capabilites, however it illustrates the point well enough.

Next we could consider the more realistic scenario, a group takes control.

To introduce the next topic we should make solving the next block analogous with winning the lottery. Although it's not entirely correct, for those taking part with a comparatively low hash rate the ability to solve a block tends to it.

A rough calculation for the time an individual needs to solved a block follows; network hashrate ÷ personal hasraterate × block time = time to find a block.

Using the same CPU we mentioned previously, it would take; ((2,5×10^9)÷(100×10^3))×(120)=3000000 s or 35 days to solve a block. This assumes that you are not 'unlucky' and do indeed solve one during this time. Luck in this case is often calculated as a percentage of this value.

When trying to win the lottery one can compete on their own or alongside others in the form of a syndicate. Syndicates in this case are called pools and are a common way for miners to ensure that they receive a steady income for the work the produce.

For both a mining calculator and a list of the current publicly available pools please take a look at [miningpoolstats.stream](https://miningpoolstats.stream/monero). Here we can find links to the pools, view how the hashrate and blocks are distributed across them and use the calculator.


### Solo vs. Pool mining

Miners are free to decide if they prefer mining as part of a pool or by themselves (solo). Each method has its benefits and drawbacks and this table aims to illustrate just a few:

|Pool type|Payouts|Fee|Min. payout|Centralised?|Stability|Control|Setup
|-|-|-|-|-|-|-|-|
|Centralised pool|Regular|0-3%|0,001-0,01 XMR|Yes|Less stable due to pool server outages|Pool admin controls your mined funds, what you mine and can execute >50% network attacks|Only miner software is required
|Solo|Rare|0%|0,6 XMR or more|No|As stable as your Monero node|100% under your control|Monero node + optional miner

All you need to mine on your own is a stable internet connection, a Monero node and some mining software. There are a few different options for mining software, the official Monero GUI even has it built in.

[Developed and worked on by community members](https://github.com/xmrig/xmrig/graphs/contributors), [XMRig](https://github.com/xmrig) is the go to for mining software. All that is required is a primary Monero address and a connection to the RPC server of a Node. It's recommended that you host your own node, firstly for privacy reasons and secondly, that you are responsible for its up time and stability. If you don't already have your own node, please follow our guide entitled [**setting up your own node**](https://moneroguides.org/tutorials/01x02-setting-up-your-own-node/) in order to get yourself set up.

Solo mining means you are only as likely to solve a block as the hashing power of your miner. It does however mean that when you do solve a block you keep all of the block reward and transaction fees. Your mining experience is totally under your control and there are no third parties involved.

With centralised pool mining that is not the case. With this type on mining all you need is the miner software. This is because it is to their node that you are dedicating your hashing power and their wallets which receive the block rewards and transaction fees. 

The main advantage is that you will always get a share of the solved blocks, regardless of whether or not your miner's successful. There are a few different types of payout systems, to learn more we suggest you take a look at the following bitcoin [wiki](https://en.bitcoin.it/wiki/Comparison_of_mining_pools).

Centralised pool operators are in direct control of the funds you helped to mine and they also typically charge a fee for their withdrawal. These are not the only disadvantages; they control what and when you mine and they can even use your hashing power to break the networks security!

[miningpoolstats.stream](https://miningpoolstats.stream/monero) also gives you information about the pool fees, minimum payout and number of active miners. Don't be attracted to the top performing pools, they often have higher fees and higher minimum payouts. Choosing these pools helps to centralise the security of the network and in the worst case could lead to a breaking of that security.

You may think that the larger pools will offer more reliable and consistent payouts, due to them finding more blocks. However, your average mining income will remain the same and choosing pools at the top of this list offers no real benefit!

We at Moneroguides recommend P2Pool for those interested in pool mining, the details of which we'll be covering in the following section.

We'd like to close this section by drawing your attention to [Moneroocean](https://moneroocean.stream/). Mooneroocean is a rather unique pool as it offers you the ability to mine other coins with your hardware and get paid in Monero! Although it doesn't help with network security it does add buying pressure to Monero, which is also of benefit to the community. 

If you are mining on your home pc, then there is a chance you have a GPU capable of mining. At idle this GPU will still consume power, so it's best to put it to use and generate further income.

For more info on how to get started, head over to the *help* sections of the website.


### P2Pool & Income

P2Pool is also rather unique and a relatively new entry into the mining world. It's a decentralised pool which leverages a side chain to manage the active miners and their rewards. P2Pool is a innovative way of mining Monero which allows miners to receive the frequent payouts offered by pools without needing to trust a centralised pool.

As a decentralised pool, P2Pool greatly increases the security of the network and helps to reduce the risks posed by centralised pools. It is for this reason alone that we recommend you aim to mine using P2Pool if you use a pool at all.

The following table aims to illustrate some of the differences. 

|Pool type|Payouts|Fee|Min. payout|Centralised?|Stability|Control|Setup
|-|-|-|-|-|-|-|-|
|Centralised pool|Regular|0-3%|0,001-0,01 XMR|Yes|Less stable due to pool server outages|Pool admin controls your mined funds, what you mine and can execute >50% network attacks|Only miner software is required
|Solo|Rare|0%|0,6 XMR or more|No|As stable as your Monero node|100% under your control|Monero node + optional miner
|**P2Pool**|Regular|0%|~0,0003 XMR|No|As stable as your Monero node|100% under your control|Monero node + P2Pool node + mine

The P2Pool sidechain works much faster than Moneros and all P2Pool blocks are potentially Monero blocks. Each miner submits block templates that include payouts to all of the miners that have shares currently in the PPLNS window.

Let's head over to the [P2Pool.observer](https://p2pool.observer/) website and take a look at a miners current status.

As you can see, this is a rather successful miner with a large hashrate. Bellow the statistics you will see information about the shares they have found and what the diagram represents.

Once a miner has found a share you will see it move from right to left with time. It will stay in the PPLNS window for a total of 2160 pool blocks or 6 hours; this is a result of having a block creation target of 10 seconds. The moment P2Pool finds a valid Monero block and there is at least 1 pool share in PPLNS window, you'll get a payout! This is because the block reward is split proportionately between all the wallets with valid shares in the PPLNS window.

If P2Pool's hashrate isn't high enough to find Monero blocks every 6 hours as a minimum, not all shares will result in a payout. With Moneros current difficulty value, that would require a pool hastrate of 15 MH/s. Even if the pool hashrate is equal to 15 MH/s or higher, bad luck can sometimes result in a share going through PPLNS window without being rewarded. However, in the long run it will be compensated for by other shares receiving multiple payouts. Keep this in mind; payouts will average out over time to equal what you'd get with any centralised pool.

[P2Pool.observer](https://p2pool.observer/) also has a form of calculator on their web page. You can use this calculator to estimate the time in which it will take you to find a share. It does this by dividing the current difficulty by your hashrate. Let's head back to the main page; you will see it labelled *Average Share Time Calculator*. After entering our machines hashrate and hitting the *calculate* button, we'll be given our estimate.

You may have noticed when we visited [miningpoolstats.stream](https://miningpoolstats.stream/monero) that there were two entries for P2Pool. At the time of making this video there are two different P2Pools; the first and largest is the original the second, nicknamed 'mini' is a smaller and newer edition. Mini was established in order to reduce the intervals between shares found and further bolster the number of decentralised pools which support the network. In an ideal world, all the current pools would switch the the decentralised model, howver progress takes time.

To get an idea of how much Monero you may mine per day you can do you own calculation. You need to first multiply the number of blocks produced each day by the amount of Monero supplied with each block. As the Monero network has entered its tail emission phase, each block is now worth 0,6 XMR and will continue like this indefinitely which will hold true, unless the code is changed. As discussed, we already know that around 720 blocks are produced each day. 

We then need to multiply that by hashrate your miner produces, as a percentage of the networks hashing power as a whole. Let's do a little bit of maths to help solidify that idea. With a miner hashing at 10 kH/s and a network hashrate of 2,5 GH/s one could expect to receive a daily income of 0,0017 XMR per day, here are the calculations; (0,6⋅720) × ((10×10^3)÷(2,5×10^9)) ≈ 0,0017.

In this case you are likely to get paid multiple times per day when taking part in a P2Pool.

You may now be wondering what your machines capabilities are, or if your planning to buy hardware for this purpose, what return you might expect on your investment. The next section of this video will cover hardware in more detail.


### Mining Hardware

Monero can be mined with both CPUs and GPUs, however the former is much more efficient and the method we'll be focusing on throughout this series.

As we mentioned already, [XMRig](https://github.com/xmrig) is the go to software to mining Monero. This is primarily due to its advanced features such as the 'Model-specific registers' (MSR).

In the tool bar at the top of this page, we'll find a link entitled [**Benchmark**](https://xmrig.com/benchmark). This part of the website, shows user submitted benchmarks for all kinds of CPU.

You will immediately see that AMD dominates the upper tier when is comes to mining. This has a lot to do with their construction and specification and the requirements of XMRig. If we head back to the main page and the click on *Docs* we can find out precisely why.

Click on the heading [**RandomX Optimization Guide**](https://xmrig.com/docs/miner/randomx-optimization-guide). Here you will notice that 2 MB of L3 cache is required for each mining thread. AMD CPUs fair well when mining Monero, as each CPU thread has access to 2 MB of L3 cache. 

Conversely, Intel CPUs typically have smaller L3 caches, meaning there isn't enough memory for every CPU thread. Let's take a look at the Intel Core i9-10900K as an example. This an extremely capable processor in general, but due to it only have 20 MB of cache, it utilises just 10 threads while mining Monero. If we take a look back at the benchmarks, this means it scores even lower than AMD's 5700x.

The hashrate displayed to the right of each processor is always the highest score from all the submissions. It's wrong to presume that just because you have this CPU or plan to buy it, that this is the hashrate you will achieve.

These values displayed are a  result of numerous factors, the first of which will be the clock speed and power consumed by the chip. You may have already come across the term [overclocking](https://en.wikipedia.org/wiki/Overclocking); these high scores are often achieved because the hardware has been pushed to the limits of stability. 

These scores are typically achieved using an enormous amount of power whilst generating just as much heat! You will find that these scores are more about showing off, rather than something desirable in any normal mining machine. As a miner, it is in your economic interest to use as little electricity as possible! Our experience shows that common Ryzen dektop processors are utilised sensibly and effciently when hasrate is equal to around 80% of these top scores.

If we click on the the name of the CPU we will be taken to a page which will show us details of more submitted benchmarks. You will find quite a lot of variance here and further details of each result can be seen using the button provided.

Other that your choice of processor, there are two other factors which greatly affect these scores. They are RAM latency and the number of memory channels available.

The faster your memory, the better it will perform when mining. Absolute latency is calculated as being equal to **(CAS latency×2000)÷Frequency**. An example follows; a memory module running @ 3200Mhz with a CAS Latency (CL) of 14 has a latency of 9.75 ms. Typically, B-die from Samsung performs best in this regard. That being said, one should always consider price relative to the performance increase.

Next, is the number of memory channels. Let's stick with the 5700x as an example. According to AMD's website, the 5700x has 2 memory channels available. One might think that it's only necessary to provide two [DIMMs](https://en.wikipedia.org/wiki/DIMM) in this case. 

In fact, you benefit from providing four DIMMs or two DIMMs which are [multi rank](https://en.wikipedia.org/wiki/Memory_rank); this is a result of [interleaving memory](https://en.wikipedia.org/wiki/Interleaved_memory), when one bit on memory is being used, the next is ready in the queue. All of this is hardware dependant, so it's good to take a look at the manufacturers specifications. 

All of that information might have left your head spinning, but don't fret. Watch this section as many times as you require to take it all in.

Having the fastest CPU and memory is all well and good, but without considering additional factors such as efficiency and cost, you could well be digging yourself into a hole. That's why we want to cover some additional thoughts in the next section of this video.


### Efficiency & Cost

We at moneroguides believe in using hardware as efficiently as possible, like [dollar cost averaging](https://en.wikipedia.org/wiki/Dollar_cost_averaging)(DCA), this is both the most cost effective way to earn Monero and support the network.

In order to know how efficiently we are mining, we need to know how fast our machines are hashing and the amount of power that is required to do so. With this information we can get a ratio, detailing the number hashed generated per unit of power.

Let's use the previous example where we have a machine hashing at 10 kH/s and them give it an arbitrary power value. In this calculation we are going to determine the number of hashes per [Joule](https://en.wikipedia.org/wiki/Joule).

-> 10000 H/s ÷ 96W ≈ 104 H/J

To make this more relatable we can then convert this to hashes per [kilowatt-hour](https://en.wikipedia.org/wiki/Kilowatt-hour). The purpose of doing this is to make it more relatable to the way in which electricity is bought.

-> 104 H/J ÷ (1÷3600000)  ≈  374×10^6 H/kWh

Knowing this we can take things even further; now we can calculate the cost or profit we stand to make whilst mining Monero.

Let's assume a domestic electricity cost of €0.19 per 1 kWh. We can hence say that for every €0.19 we spend of electricity, we buy 374×10^6 H/kWh.

Now you may be fortunate enough to be using wind or solar power and this calculation is not exactly required; you may even have free electricity! Regards of these facts it is still an interesting exercise and food for thought.

Next, let's assume you decide to mine with P2Pool mini. As discussed, you are paid proportionately to the blocks you produce on that chain. To move forward we need to know both the difficulty of producing those blocks as well as an approximate value for each one found.

P2Pool mini has a block target of 10 seconds, 12 times faster than the main Monero chain. The difficulty can be calculated as equal to the block speed multiplied by the pool's hashrate.

With a pool hashrate of 11x10^6 H/s the difficulty would hence be 110×10^6 H.

-> 10 ⋅ 11x10^6 H/s = 110×10^6 H per share

We already know that €0,19 buys us 316×10^6 H/kWh. So we can then calculate the cost of each share using the following equation:

-> 374×10^6 H/kWh ÷ 110×10^6 H ≈ 3,4 
-> €0,19 ÷ 3,4 ≈ €0,055

The value of each of these shares is always changing and directly correlated to the price of Monero. Assuming one has a single share in the PPLNS window when a Monero block is found, a share is then worth 1/2160 of the block reward. Using €167 as the value of Monero, we can calculate the value of a single share:

-> 0,6×(1/2160) ≈ 0,00027 XMR per share 
-> 0,00027×**€167** ≈ €0.043

We are mining at a considerable loss in this example. It costs €0,055 to mine €0,042 worth of XMR which equates to a whopping 23% loss!

In order to break even in this case, either Monero needs a value of €203 or 1 kWh of electricity must cost **€0,14**

Especially during [bear markets](https://en.wikipedia.org/wiki/Market_trend#Bear_market) you should count yourself rather lucky if mining Monero is still profitable.

As we mentioned already, these calculations may seem a little complex and over the top, but for many this offers a great insight into the efficiency and profitability of their hardware!


### OUTRO

We've covered a lot of information in just a short time. As with all videos like this, please take your time to take this information in and re watch it as needed. 

Don't forget that you can find the transcript either on our website www.moneroguides.org or on github. These scripts are free to use, alter and redistribute so don't hold back!

That's it for the first part in this series. The next video will cover the software side of getting your hardware up a running.


~moneroguides
