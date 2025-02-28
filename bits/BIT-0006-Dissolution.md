# BIT-0006: Council Dissolution of dTAO Subnet

- **BIT Number:** 0006
- **Title:** Council Dissolution of dTAO Subnet
- **Author(s):** CapriciousSage
- **Status:** Draft
- **Type:** Core
- **Created:** 28/02/2025
- **Updated:** 28/02/2025

## Abstract

Introduction of emergency/last resort governance powers to the Root Network Validator Council to dissolve a dTAO Subnet to avoid network/systemic risk 

## Motivation

While the "lolocaust" (SN28 consensus change to incentivise dumping the token) has been an effective way of dealing with unwanted/dangerous subnet economics (ponzi), it does not allow for the removal of unwanted/dangerous subnets themselves (malware, CSAM, other illicit content, etc). As such, a mechanism to remove subnets that present a significant risk to the broader ecosystem is required.

## Specification

- Addition of new governance capabilities to allow for senate members to create and vote on proposals that, should the proposal pass by a super-majority, will automatically dissolve a dTAO-subnet.
- Dissolution process would also need to include the forced fire-sale of outstanding dtao tokens back to TAO utilising the existing pool liquidity.
  -- It is vital that the dtao fire-sale all done at the same price, completed in a manner that equalises the price impact among all eligible participants.
  -- The applicable dTAO tokens in the subnet owner's wallet should be excluded from this fire-sale process ('burnt')
- To prevent bad actors from 'rugging' the subnet during the governance window, certain activities on the subnet should be frozen once the governance proposal is submitted
  -- These include the LP (preventing buying/selling), token issuance (miner/vali/subnet owner rewards), and miner/vali registrations).
- To avoid abuse (unwarranted dissolution proposals), the governance proposer should be required to lock an amount of tao equal to the registration cost of the subnet.
- Due to the lack of a "No with Veto" mechanic, voting results would need to accommodate three outcomes (Yes/Split Vote/No
  -- Yes (66% Super Majority in support): Subnet is dissolved, locked tokens returned to proposer 
  -- Split Vote (34% - 65% in support): Subnet is not dissolved, locked tokens returned to proposer
  -- No (33% or less in support): Subnet is not dissolved, locked tokens are recycled

## Rationale

Subnets being used to distribute malicious or illicit material (malware, CSAM, etc) pose an existential risk to the entire network. It is vital that the network have a manner in which to remove these threats. Additionally, should certain subnets become abandoned, it may be necessary to remove these abandoned subnets to reduce unnecessary chain bloat/overhead.

## Backwards Compatibility

It is unknown whether the introduction of additional capabilities to the governance module (including integrating with locking tokens when submitting a dissolution proposal) may have backwards compatibility issues with the existing governance framework.

## Reference Implementation (Optional)

The Cosmos SDK provides a well-known example of governance proposals requiring a deposit, which is then burnt in the event of a "No with Veto" outcome

## Security Considerations

The existence of a dissolution procedure is not a panacea against abuse. Senate members may have vested interests (or lack of interest in voting) that may prevent the successful dissolution of a subnet where it may be otherwise needed. However, this is always a risk in any decentralised ecosystem and relies on network participants showing wisdom in selecting which validator to delegate to.  

## Copyright

This document is licensed under [The Unlicense](https://unlicense.org/).

