# HIP Split Claimed Rewards Between Multiple Wallets

- Author: [@cipherkilledit] (https://github.com/cipherkilledit) [@workingtitle]
- Start Date: 8/30/2024 
- Category: Technical, Economic
- Original HIP PR: <!-- leave this empty; maintainer will fill in ID of this pull request -->
- Tracking Issue: <!-- leave this empty; maintainer will create a discussion issue -->
- Vote Requirements: veMOBILE Holders ? , veHNT Holders, veIOT Holders ?? 

## Summary

This HIP proposes the introduction of a Deputy NFT system to facilitate transparent and fair reward splitting between deployers and hosts within the Helium ecosystem. By adopting a tokenized Deputy system, it allows deployers and hosts to share rewards in predefined ratios, while creating clear incentives for each party involved in hotspot deployment and maintenance.
This model ensures trustless distribution of rewards, encouraging collaboration and improving network scalability. The introduction of NFTs as "Deputies" allows for automated reward management, further enabling the Helium Ecosystem Deployers to promote each subnetworks scalable, decentralized, and transparent qualities.


## Motivation

Currently, deployers and hosts face difficulties in managing reward distribution, potentially this can lead to disputes over earnings or unclear terms. This proposal solves these challenges by:
1. Automating the reward-splitting process using blockchain-secured NFTs.
2. Ensuring both deployers and hosts benefit from the network's expansion without conflict.
3. Introducing transparency in agreements, which enhances trust among stakeholders.

## Stakeholders

- Builders actively deploying hotspots at scale across third party hosts
- Operators who manage existing hotspots 
- Property Owners hosting hotspots
- Prospective Property Owners seeking a portion of rewards post-deployment

## Detailed Explanation

In this proposal we formally introduce the concept of splitting rewards between multiple wallets by creating DEPUTY NFTs. Upon approval of this HIP, hotspots would be configurable to allow Deployers to specify additional DEPUTY NFTs to receive rewards and choose what percentage of the rewards each DEPUTY NFT (wallet) would receive when rewards are calculated (claiming). Example: a commercial Property Owner could allow a Builder to deploy hotspots throughout their property in exchange for 50% of the ongoing rewards. Upon (claiming) calculating the rewards, the Builder and the Property Owner would each receive 50% of the calculated (claimed) rewards in their respective wallets. 

The DEPUTY NFT reward split is determined by the parties involved in an off-chain agreement. Both parties through their wallets will be required to approve establishing the rewards each DEPUTY NFT is entitled to, and both wallets will be required to sign off on any changes to the rewards split. 

Economic and Functional Role Overview:
Deputy NFT: A non-fungible token that manages the reward splitting between deployer and host. The NFT is tied to the hotspot’s unique identifier and stores the reward split parameters. 
Both parties should agree off-chain on the split percentages and terms before hotspot deployment.
Ensures adherence to the terms agreed upon between deployers and hosts, secured via smart contracts.

Deployer: Responsible for purchasing and setting up the Helium Ecosystem devices in optimal locations.Currently onboarding a device deployers creates a Device NFT, deployers can then establish the share of rewards they allocate to hosts and others through Deputy NFTs.
Receives a pre-agreed portion of rewards based on Deputy NFT parameters.

Host: Hosts the hotspot on their premises and ensures it remains operational.
Earns rewards through a split set by the Deployer through the Deputy NFT.

Real-World Example:
In a scenario where a deployer sets up a Helium Mobile hotspot at a rural Diner. The diner is owned by a host who benefits from local network coverage.
Deployer’s Perspective: The deployer seeks to maximize coverage in rural areas where cell tower coverage is spotty and wants to ensure the host keeps the hotspot active. With the Deputy NFT, the deployer can automate a reward split (e.g., 40% deployer, 60% host). The deployer doesn’t need to worry about manually splitting rewards, as it’s handled by the blockchain.
Host’s Perspective: The host benefits from local network coverage for their customers Mobile devices used while dining. In return, they receive the daily stream of rewards from the network. The transparency of the Deputy NFT ensures that the host receives an agreed upon share of the rewards automatically, encouraging long-term participation.

Benefits to the Helium Ecosystem
Transparency: Both parties have visibility into reward distribution, preventing disputes.
Decentralized Agreements: The Deputy NFT system allows the Helium Deployers to operate more efficiently without needing to maintain long term reward redistribution agreements manually. . 
Scalability: As Helium expands, this system will help streamline relationships between hosts and deployers, fostering further growth in network infrastructure. 
Ecosystem Table Stakes: As Helium adds various future subnetworks, the Deputy NFT system will allow DePin projects to easily reward various participants. 

Implementation
NFT Creation: Deployers mint a Deputy NFT and assign reward splits before or during deployment.
Smart Contracts: These contracts, tied to each Deputy NFT, automatically distribute rewards between deployers and hosts.
Governance: Two wallets must approve changes to the split between the Device NFT and the Deputy NFT. 
Scale: A Device NFT can add 99 Deputy NFTs with a minimum of 1% of rewards assigned to each NFT. This is a total of 100 maximum NFTs per device. 

Conclusion
The Deputy NFT system is a scalable, transparent, and fair solution that will enhance collaboration between deployers and hosts, drive network growth, and create an equitable trustless reward structure in the Helium ecosystem. By utilizing NFTs, we bring automation and security to reward management, allowing the network to grow without compromising on trust or fairness.

## Drawbacks

1. There will be more NFTs to track on chain.
2. Community tools may have some difficulty tracking different NFTs and tracking a devices entire reward allocation
3. Once a Deputy NFT is created and sent to a second wallet, both wallets must sign off on changes. Unknown how real world relationships may impact the networks. 

## Rationale and Alternatives

The current approach to splitting rewards is a time-consuming process in which the party custodying the hotspot's NFT claims the rewards and then sends the other party their portion of the rewards manually in a separate transaction. 
The party custodying the single NFT is responsible for financial accounting and rewards transfer record keeping. 
At scale this manual tracking and distribution of rewards adds time and costs to every subnetworks expansion. Manual distribution of awards to hosts that may not be following the changes to rewards driven by HIPs requires a deployer to communicate those changes. 

One alternative is to mint multiple NFTs immediately for each device and set a fixed split percentage at onboarding. 
Example: each device onboards with 5 NFTs each eligible for 20% of device rewards, these NFTs can then be transferred to other wallets for hosts and others rewards. This approach has limited flexibility for deployers. 

Another alternative is to establish a split of rewards directly from a deployers wallet and when rewards are claimed they deposit into the deployers wallet and then are sent to hosts wallets automatically. 
This approach does not lift the burden of reward accounting from deployers. 

## Unresolved Questions

What happens in the event one party wants to make changes to the split percentage?  
If one party loses access to their wallet, how would the split percentage or wallet address be revised? 
If a device gets resold will the resellers reveal the reward splits for that device? 
Will splitting rewards allow gamers to hide more effectively by lowering the amount of rewards each Device NFT and Deputy NFT receives? 


## Deployment Impact TBD

Nova Labs will collaborate with the Helium Foundation to complete the implementation, should this HIP pass voting. Specific deployment impact details and timeframe will be filled out by engineering prior to HIP going to vote. 

## Success Metrics

1. This HIP has been deployed successfully when rewards are sent to multiple wallets in accordance with the defined split percentage and listed addresses upon daily reward calculations (claiming).
2. Success can be measured by deployer feedback on the ease and efficiency of setting up host wallets and transferring deputy NFTs.
3. Success can be measured by an increase of hosts wallets holding only Deputy NFTs and no Device NFTs.  
