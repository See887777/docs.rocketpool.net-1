# Node Requirements and Choosing a Platform

Alright!
So you've decided to try your hand at running a Rocket Pool node.
The first step of the process is to decide what kind of platform you want to run your node on.
If you already have one in mind, great!
You can skip to the next section.
If you aren't sure yet, then read on for some information about your options.

## Full Node Requirements

A **full node** is one that runs both an Execution Client and Consensus Client along with the Rocket Pool stack.
Now that the Merge has occurred, Rocket Pool nodes are required to run this configuration (though the Execution and Consensus clients can be externally managed for users already running a solo-staking setup - we'll cover this in more detail later).

Here is a simple breakdown of what is required to run a full Rocket Pool node well:

- A **stable Internet connection**. The longer you stay online, the better your rewards. A spotty Internet connection will hurt your returns, and by extension, the rETH ratio growth.
- At least **10Mbps of bandwidth both up and down**. A full node usually takes around 8Mbps to 10Mbps up & down of network traffic, depending on your configuration and number of minipools.
- **No data cap** imposed by your ISP. Running a full node will take a lot of data - we have seen reports of over 2 TB per month on chain data alone. This can be mitigated somewhat with a few settings tweaks to the ETH clients, but as a rule of thumb, don't run a full node if your Internet plan comes with a monthly data cap.
- **Stable electricity**. For the same reason as needing a stable Internet connection, you also want to have reliable power. This can be mitigated with a large UPS (backup battery) to deal with short blackouts.
- A **computer** with sufficient specs. This is pretty flexible because it _really_ depends on what Execution and Consensus client you use, and what settings you configure them with. The computer can be a local machine, or it can be a Virtual Private Server (VPS) hosted in the cloud. Read below for some more information on those two options, and how to decide which is best for you.

The computer must meet the [hardware guidelines](./local/hardware.md)

::: warning NOTE
At this time, only **Linux** and **macOS** platforms are supported.
**Windows is not currently supported** for Smartnode operation.
:::

## Running a Local Node

If you have reliable electricity and uncapped Internet access, and are willing to build (or buy pre-made) and maintain a computer, then running a local node might be a great choice for you. With this option, you will set up a dedicated computer as a Rocket Pool node and run it locally in your own home.

Advantages:

- No monthly fees, other than utilities
- Complete control over your own machine and its data (including your wallet's key)
- Access to perform maintenance and upgrades whenever you want
- Contributes to Execution and Consensus's, and Rocket Pool's decentralization (and thus, their security)

Disadvantages:

- Requires stable, uncapped Internet and electricity
  - **Running a node uses at least 1.5 TB of data per month. If you have a data cap below this amount, you may run into problems while running a local node!**
- You're solely responsible for network & computer security
- Can be challenging if you're not experienced with computer maintenance
- Vulnerable to theft

If the advantages sound like they outweigh the disadvantages for you, then take a look at our [Local Node Operator's Guide](./local/hardware.html).

## Running a VPS on the Cloud

If you don't have a reliable uncapped Internet plan, or you just don't want to deal with building and maintaining your own physical computer, you may want to look at running a virtual private server. These are virtual servers that you rent from hosting providers, such as Amazon Web Services, Microsoft Azure, OVH, or other companies. Essentially, these companies will happily create and run a server for you, for a monthly fee. If you don't mind that fee and want to run a Rocket Pool node, using a VPS can be a good strategy.

Advantages:

- No maintenance, support is usually available to fix issues
- Doesn't affect your Internet plan or data cap
- Usually run in a professional data center, very little down time
- May be more cost effective than buying / building your own computer

Disadvantages:

- Makes Execution and Consensus, and Rocket Pool somewhat more centralized, which weakens the security of the networks
- Monthly fees
- Servers may come with data caps, or have expensive network I/O rates
- Possible for hosts to examine your machine's contents and take your wallet's key if not secured

If those advantages sound like they outweigh the disadvantages for you, then take a look at our [VPS Node Operator's Guide](./vps/providers.html).
