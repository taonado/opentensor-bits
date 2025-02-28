# BIT-0000: dTAO Subnet Immunity Window

- **BIT Number:** 0000
- **Title:** dTAO Subnet Immunity Window
- **Author(s):** CapriciousSage
- **Status:** Draft
- **Type:** Core
- **Created:** 28/02/2025

## Abstract

Introduce the dTAO equivalent of the "pre-dtao" 7-day immunity period. Have pool locked and inflation paused for the first 7 days of new subnet registration to allow the subnet owner a chance to get things ready without miners and validators exploiting the subnet for dtao tokens.

## Motivation

Pre-dtao, new subnets experienced a 7-day immunity period, which allowed a subnet owner to verify the discord channel, publish their repo, onboard valis and miners, and 'get things rolling' - all without pressure of deregistration and without any real money on the table.

Sadly, dTAO lacks this functionallity, and instead creatives an incentive to 'rush' new subnets with bogus validator or mining code to try and establish early vtrust and child hotkey delegations. This not muddies the early token supply (causing undue market damage) but also undermines the subnet owner's attempts to launch the subnet correctly.

By allowing a similar 7-day window, Subnet onwers get a chance to establish themselves without being pushed around in their own network, and network participants get 7 days to evaliate "do I want to mine, validate or buy this token" (minimising the chances of getting rekt on a rugnet/ponzi). It also ensures that subnet owners know they are "on the clock" and only have 7-days to get their act together.

## Specification

Option 1 (Clean): All new subnets automatically enter a 7-day "immunity period" where the LP is locked, with no tao/dtao added and no trading possible, and no dtao Token Emissions. Validators and miners can register, build vtrust/trust, but no emissions or dividends are paid out (disincentivising running "arbitrary weights" code). After 50,400 blocks, the ball starts rolling automatically.

Option 2 (Clunky): Alternatively, just start all new subnets with registration disabled. This is an easier technical solution but has other problems.

## Rationale

Every single new subnet launched since dTAO has seen it's dtao token exploited by validators and miners running fake/arbitrary code (not supplied by the subnet owner). As network participants are also attempting to 'fomo' into these new subnets based on rumours of what they might be, this has allowed the exploiters to use retail as exit liquidity (or gain an unfair advantage in the new subnet prior to its practical-launch with a proper repo).

## Backwards Compatibility

While not a backwards compatibility issue specifically, dTAO subnets that go live prior to the implementation of this BIT should consider manually implementing "option 2" (disabling registrations on their SN) as a temporary work-around until they're ready to launch their repo to avoid being gamed.

## Reference Implementation (Optional)

N/A

## Security Considerations

The 7-day window does not guarantee that the subnet will be ready by the end of the 7-days, so gaming/exploiting may still occur, but at the very least it gives the subnet owner a fighting chance with a reasonable timeframe to get ahead of the problem

## Copyright

This document is licensed under [The Unlicense](https://unlicense.org/).

