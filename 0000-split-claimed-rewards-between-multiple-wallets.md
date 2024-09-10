# HIP Split Claimed Rewards Between Multiple Wallets

- Author: [@cipherkilledit] (https://github.com/cipherkilledit)
- Start Date: 8/30/2024 
- Category: Technical, Economic
- Original HIP PR: <!-- leave this empty; maintainer will fill in ID of this pull request -->
- Tracking Issue: <!-- leave this empty; maintainer will create a discussion issue -->
- Vote Requirements: veMOBILE Holders

## Summary

This Helium Improvement Proposal introduces the concept of splitting claimed rewards between multiple wallets by creating DEPUTY rewardable NFTs that each wallet can hold. 

## Motivation

Most commercial venues and hosts want a share of the rewards, but do not possess the technical knowledge or will to deploy hardware themselves. To grow coverage of the Helium subnetworks (mobile network) more efficiently, it makes sense to provide Builders a way to share rewards with (Property owners) hosts or other interested parties without acting as a financial advisor or fiduciary. This would enable (both) multiple parties to be rewarded in separate wallets at an agreed upon (specified) percentage. Example: When (claiming,) rewards are distributed the Builder's wallet (receives) 50% for their DEPUTY NFT and Property Owner's wallet recieves 50% for their DEPUTY NFT, assuming they Builder and the Property Owner have an off chain agreement in place that spells out the 50/50 share. (This will also reduce the gas fees paid by users who required 2 separate transactions to acheive this result manually.) This will cleanly direct rewards to each party for tracking and accounting purposes. It will no lomger be required that one entity claim, track and distribute rewards for someone else. 

## Stakeholders

- Builders actively deploying hotspots
- Operators who manage existing hotspots 
- Property Owners hosting hotspots
- Prospective Property Owners seeking a portion of rewards post-deployment
- All future subnetworks

## Detailed Explanation

In this proposal we formally introduce the concept of splitting rewards between multiple wallets by creating DEPUTY NFTs. Upon approval of this HIP, hotspots would configurable to allow Deployers to specify additional DEPUTY NFTs to receive rewards and choose what percentage of the rewards each DEPUTY NFT (wallet) would recieve when rewards are calculated (claiming). Example: a commercial Property Owner could allow a Builder to deploy hotspots throughout their property in exchange for 50% of the ongoing rewards. Upon (claiming) calculating the rewards, the Builder and the Property Owner would each receive 50% of the calculated (claimed) rewards in their respective wallets. 

The DEPUTY NFT reward split is deteremined by the parties invloved in an off-chain agreement. Both parties through their wallets will be required to approve establishing the rewards each DEPUTY NFT is entitled to, and both wallets will be required to sign off on any changes to the rewards split. 

## Drawbacks

(Introducing rewards splits would enable the party in custody of the hotspot's NFT to change the split percentage at any time without approval from the other party.) 
- Splitting one hotspot rewards into multiple rewardable DEPUTY NFTs will increase the potential for one party to loose control of their wallet and temporarily or permanently reduce the rewards available to that hotspot.
- Hosts may be more inclined to immeadiately exchange their rewards for fiat and negatively impact stakers and holders of veMOBILE and veIOT.
- 

## Rationale and Alternatives

The current approach to splitting rewards is a time-consuming process in which the party custodying the hotspot's NFT to claim the rewards and then send the other party their portion of the rewards manually in a separate transaction. The party custodying the single NFT is responsible for financial accounting and rewards transfer record keeping. 

## Unresolved Questions

What happens in the event one party makes unauthorized changes to the split percentage? Could a smart contract be implemented that requires a signature from both parties before a split percentage is changed? If one party loses access to their wallet, how would the split percentage or wallet address be revised? 

## Deployment Impact

Nova Labs will collaborate with the Helium Foundation to complete the implementation, should this HIP pass voting. Specific deployment impact details and timeframe will be filled out by engineering prior to HIP going to vote. 

## Success Metrics

This HIP has been deployed successfully when rewards are sent to multiple wallets in accordance with the defined split percentage and listed addresses upon daily reward calculations (claiming). Success can be measured by comparing the gas fees paid by users who were manually splitting rewards prior to the implementation of this HIP.
