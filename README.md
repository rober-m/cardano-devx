# Developer Experience Strategy for 2026/27

This repository contains an ecosystem-wide strategy to improve DevX (developer experience) in Cardano. It is not an official statement from any entity but a document used to gather feedback from and align with the companies of the ecosystem that work on tooling, libraries, documentation, and other aspects that affects the DevX in Cardano.

The structure is as follows:

1. [Vision](#vision)
1. [Executive Summary](#executive-summary)
1. [Why is this strategy needed?](#why-is-this-strategy-needed)
    1. Builders are fundamental for the success of the ecosystem.
    2. Cardano has a DevX issue
    3. An ecosystem-wide strategy is needed
1. [Personas](#personas)
1. [Deliverables](#deliverables)
1. [How we will measure success](#how-we-will-measure-success)
1. [Conclusion](#conclusion)
1. [Teams on board with this strategy](#teams-on-board-with-this-strategy)

## Vision

Make Cardano known for great developer experience across the entire Blockchain ecosystem.

## Executive Summary

**As a builder new to Cardano, I want to go from zero to an MVP on testnet in under two weeks, so that I can validate whether Cardano is the right platform for my project without a large upfront time investment.**

**Problem:** The current developer experience (DevX) on Cardano is poor and fragmented, making it difficult for new and experienced developers to build, test, and deploy decentralized applications efficiently. Friction points include a lack of standardized tooling, non-canonical patterns and data representations, and outdated, fragmented documentation and libraries. All of which slow down development cycles and increase the barrier to entry for developers from other ecosystems (EVM, Web2). However, the underlying issue is not a lack of effort but rather misaligned incentives and a lack of an ecosystem-wide strategy.

**Solution:** The core of this proposal is to provide an ecosystem-wide strategy that allows different companies that affect DevX to align in achieving a DevX initially on par with, and eventually superior to, what EVM developers are used to. The end result being that newcomers face less friction when getting started in Cardano than in other ecosystems. We’ll do this by:

- Keeping track of the current and future state of all the projects that affect DevX and help them fit in the broader context.
- Unifying and improving the onboarding and educational resources.
- Selectively contributing to the developer experience of key projects.
- Creating missing tooling.

**Why now:** The best time was years ago; the second-best time is today.

## Why is this strategy needed?

If you are not convinced by the next statements, open the toggles to see the reasoning behind it. We'll use both the statements and the reasoning behind them as premises to derive the strategy.

<details>

<summary>Builders are fundamental for the success of the ecosystem</summary>

Unlike with Bitcoin, the value of Cardano and similar programmable blockchains is directly tied to the value its ecosystem provides to its users. Independently of cycles, market conditions, or other factors, if something is useful, it will be used.

We'll call builders to the people who create the products and services people use in the ecosystem.

As such, builders are the foundation of the ecosystem. They are the ones who create the products and services people will use Cardano for. On the long run, they are the ones who make the ecosystem successful.

</details>

<details>

<summary>Cardano has a DevX issue</summary>

The next information is based on:

- **Electric Capital's [Open Dev Data](https://opendevdata.org/about)**: An open source platform that provides the crypto industry with a single source of truth for measuring developer activity. Data until January 2026.
- **Cardano Foundation's [Developer Survey](https://cardano-foundation.github.io/state-of-the-developer-ecosystem/2025)**: With responses from a significant portion (109) of the developers on up to 36 questions, the 2025 survey offers valuable insights into the needs and experiences of those building on Cardano.

### Developer activity: Cardano vs Ethereum and Solana

There's a huge gap between Cardano, Ethereum and Solana across any metric related to developer activity:

| Developer Category                | Cardano | Ethereum | Solana | Eth/Cardano | Sol/Cardano |
| --------------------------------- | ------- | -------- | ------ | ----------- | ----------- |
| All developers                    | 678     | 11,624   | 4,519  | 17.1x       | 6.7x        |
| One-time developers               | 55      | 1,624    | 787    | 29.5x       | 14.3x       |
| Part-time developers              | 355     | 6,234    | 2,510  | 17.6x       | 7.1x        |
| Full-time developers              | 268     | 3,766    | 1,222  | 14.1x       | 4.6x        |
| New Developers (0-1 year)         | 199     | 4,650    | 2,177  | 23.4x       | 10.9x       |
| Emerging Developers (1-2 years)   | 101     | 1,578    | 622    | 15.6x       | 6.2x        |
| Established Developers (2+ years) | 378     | 5,396    | 1,720  | 14.3x       | 4.6x        |

From this table, we can see that not only Eth and Sol have 17.1x and 6.7x (respectively) more developers than Cardano, but also that new developers are 23.4x and 10.9x likelier to choose Ethereum or Solana over Cardano, and new contributors are 29.5x and 14.3x likelyer to choose Ethereum or Solana over Cardano.

That's the current state, but what about the evolution in time? The next chart shows the growth of developers since May of 2020 (when we start to have data for Solana):

![Developers growth since May 2020](./assets/total-devs_trend_since_SOL.png)

We can see that:

- Cardano is the only blockchain with almost no growth in the last ~6 years (82 devs/year on average).
- On average, Ethereum grows by 1940 devs/year (almost 3x the TOTAL amount of developers in Cardano) while Solana grows by 884 devs/year (1.3x the TOTAL amount of developers in Cardano).
- If we normalize growth by the initial amount of developers (to reduce networking effect), we still see that both Eth and Sol would grow faster than Cardano if starting with the same amount of developers.

By itself, this doesn't suggest that Cardano has a weak DevX. This metric is not only affected by DevX but also positioning, marketing, and other factors.

### Developers VS Token Price

The difference in developers is not **_only_** a matter of "token go up, developer activity goes up". We can explore that in the following chart that shows the number of *new* developers vs token price for all three ecosystems:


![New developers vs token price](./assets/new-devs_vs_price.png)


One thing to notice is that there's a slight delay between token price and new developer activity. Both going up and going down. And that the ecosystem that manages to retain developers after the token price drops, might carry significant advantage over the rest.

However, even if there is a clear correlation, it's far from being a 1:1 relationship. To highlight this, here's a direct comparison between number of *total* developers (new and established) and price with a linear regresion to highligh the relationship:

![Total developers vs token price](./assets/total-devs_vs_price.png)

As we can see, the amount of developers (both new and established) is somewhat correlated with price, but the huge spread suggests that it's far from being a

This also doesn't prove causation, though, only correlation. And we have to also take into account that these are not independent variables. More developers means more tooling developers, which means better 

### Developer survey results

The developer survey results are an even stronger indicator of the DevX issue. It's worth reviewing the survey results in detail to understand the full picture, but here I'll present the most relevant points:

- **Over 60% of respondents report 7+ years of software engineering experience, with another 25% in the 2–7 year range.** Early-career developers remain a minority, consistent with 2024. Compared with broader industry benchmarks such as the Stack Overflow Developer Survey, **the Cardano ecosystem remains significantly more senior than average**". This suggests that Cardano **is not appealing** to newcomers.
- When asked "What should be the biggest priority on the Cardano technical roadmap?", the option with the second and third highest rankings (behind higher-throughput) were "Better documentation and explainers" and "Accessibility & use cases enablers". **Suggesting that lack of proper documentation and explainers are a big concern, and that there's significant barrier to implement use cases.**
- When asked "How satisfied are you with the current state of the smart contract ecosystem?", the median satisfaction score was 7 with a tight interquartile range (6–8), **suggesting writing smart contracts themselves is not perfect but acceptable, and that the DevX issues are likely elsewhere (e.g., testing, debugging, and transaction ergonomics, etc.)**
- Answers to "It would be nice if there were a CLI for... ", show that requests for new CLI tooling in 2025 consistently point toward higher-level, end-to-end workflows rather than additional low-level primitives.
- Answers to "On average, how satisfied are you with the technical answers/details you find in documentation and within the community?", provide a median score of 7 with a notably tight interquartile range (6–7). **This suggests moderate satisfaction coupled with broad agreement, indicating that most developers converge on a “good enough, but not great” assessment of technical answers.** The narrow spread also implies that frustrations around documentation quality and answer depth are widely shared rather than isolated to specific subgroups. **It's impotant to highlight that this question bundles documentation and community answers, making it hard to know if one is doing most of the work for the other**.
- When asked "What do you think is the biggest pain point of Cardano's developer ecosystem?", we get a lot of insights, but for this brief, we'll limit ourselves with the final comment: **"The dominant pain points expressed in 2025 cluster around developer experience rather than protocol capability, with fragmentation of tooling, weak off-chain/on-chain integration, and the absence of mature transaction-building abstractions recurring across responses. Compared to 2024, the emphasis shifts from documentation alone toward a broader critique of ecosystem cohesion: duplicated efforts, unclear “blessed paths,” and insufficiently maintained libraries amplify the already steep eUTxO learning curve. In contrast to ecosystems like Ethereum—where complexity is often hidden behind opinionated frameworks—Cardano developers still shoulder much of the architectural burden directly, slowing onboarding and experimentation despite strong underlying primitives".**

### Conclusion

By taking into account all the previously discussed insights, it's safe to conclude that Cardano's DevX needs to improve if we want to increase the amount and retention of developers in the ecosystem. This is specially true if we want to help adoption by newcommers and developers from ther ecosystems.

</details>

<details>

<summary>An ecosystem-wide strategy that aligns the efforts of the different actors in the ecosystem is needed</summary>

Based on what we discussed in the previous point, we know the bigges issues with DevX are:

- Lack of tooling integration and ecosystem cohesion paired with insufficient coordination.
- Fragmented, immature, and unmaintained tooling, libraries, and documentation.
- Lack of plug-and-play libraries, friendly abstractions, reference implementations, and LLM support.

If the problem were localized on a specific tool, documentation, or library, it'd make sense to invest most of our work into improving those. However, the developer ecosystem is so varied and constantly changing, that our best bet is to embrace and be prepared for that. 

That's why we need an ecosystem-wide strategy, because there's no single entity, tool, or website with enough developer share, and we need to work together to have a real shot at improving the overall DevX of Cardano.

</details>

## Target Audience

Our target audience will eventually be all developers. However, we should focus on increasing the number of developers as much as possible at first. So, our priority should be to favor new, less experienced developers over existing, more experienced ones.


| Description | Why them? | They need to.. | Today, they struggle with.. | Success for them means | 
|-------------|-----------|----------------|-----------------------------|------------------------|
| Junior EVM developers | They are the easiest to onboard. They just need to learn the differences between building on EVM and eUTxO, and the practical details of our tooling. | Get a job. Integrate (or replicate) their existing DApp in Cardano. | The initial steps of the development cycle. Adapting EVM architecture to eUTxO. | Being able to implement any EVM protocol in Cardano. |
| Junior Web developers | They are the most cost-effective segment. They need to learn blockchain in general and Cardano in particular, but their existing web development skills and knowledge speed up the rest of the process, and they are a large enough group to warrant our efforts. | Get a job | Virtually every step of the development cycle. | Being able to build simple DApps to add to their portfolio. Being able to prove they can build on Cardano. |
| Technical entrepreneurs | They are the ones starting new projects and hiring developers. | Evaluate the advantages, disadvantages, and cost of building on Cardano. | Creating an MVP, identifying advantages of Cardano over other ecosystems, and onboarding developers. | Being able to build their MVP in approximately the same time it would take in any other ecosystem. |


The overlapp in needs between these segments are so high that most of the works doesn't need to be targeted to one or the other.

## Deliverables

This is the list of proposed deliverables. All of them require multiple outputs and workstreams described on their respective files, this table prvodies only a short overview.


| Item                                                                   | Overview                                                                                                                                                                                                                                                                                                                                                                                          | Why                                                    | Expected Outcome                                                                                           |
| -----------------------------------------------------------------------| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------- |
| [Community Alignment and Collaboration](./deliverables/alignment.md)      | The most important item: Aligning the ecosystem with this strategy. Map all ecosystem tooling, creating a baseline for the "New Tooling" Epic. Contributing to community tooling (with an emphasis on off-chain/integration). Improving existing DApp development tooling (LSPs, extensions, TUIs, etc.).                                                                                         | See [why is this needed](#why-is-this-strategy-needed) | A clear roadmap of the ecosystem's developer experience with a list of companies/projects that support it. |
| [Setup CLI](./deliverables/setup-cli.md)                               | Create a Setup CLI/TUI to easily start dapp projects. A "create-react-app" for Cardano, where users can pick any desired stack combination. This high-level umbrella tool will leverage all identified tooling, provide AI/LLM-native commands, and use algorithmic ranking to select tools.                                                                                                      | TODO                                                   | TODO                                                                                                       |
| [Developer HUB](./deliverables/developer-hub.md)                       | Create (or adapt) the entry point HUB. Our first option is to align with the CF to use developers.cardano.org. The objective is to have a single entry point for developers new to Cardano. Define and organize onboarding content for three key user paths: EVM/Blockchain developer, Web2 developer, and Non-technical interested user. Add a CI/CD pipeline to maintain working code snippets. | TODO                                                   | TODO                                                                                                       |
| [Developer Outreach](./deliverables/outreach.md)                       | Multi-channel developer outreach program covering Discord community management, hackathons and build clubs, and educational live streams and video content to grow the Cardano developer community.                                                                                                                                                                                               | TODO                                                   | TODO                                                                                                       |
| [AI/LLM native](./deliverables/llms.md)                                   | Make the Cardano developer ecosystem AI/LLM-native by adding LLM.txt files to all documentation resources, creating an MCP server for integrated documentation access, and building agent skills for common development actions.                                                                                                                                                                  | TODO                                                   | TODO                                                                                                       |
| [OpenZeppelin-like library](./deliverables/openzeppelin.md)            | Design and implement standardized and reusable smart contracts (on- and off-chain, emphasis on DeFi) with related tooling/platform. Create the infrastructure, website, and add at least 5 ready-to-audit smart contracts.                                                                                                                                                                        | TODO                                                   | TODO                                                                                                       |
| [CIP and Pentad Integration support](./deliverables/cip-and-pentad.md) | Push for community agreement and resolution of key DevX and DeFi CIPs: standardization of CBOR objects, Account Address Enhancement (CIP-159), nested transactions (CIP-118), and programmable tokens (CIP-113). Propagate changes post-acceptance. Includes supporting Pentad integrations (Stablecoins, Bridges, Oracles).                                                                      | TODO                                                   | TODO                                                                                                       |


## How we will measure success

Developer experience is a complex and abstract concept and there's no single metric that can be used to measure it. However, we can combine several metrics to get a good approximation of it. That's why we'll measure success by combining and interpreting the next metrics.

### Proxy metrics

#### Metrics relative to the blockchain ecosystem

We use metrics relative to the overall blockchain ecosystem and direct competitors (Ethereum and Solana) to control for industry-wide trends. This is important to avoid attributing success or failure to the strategy when it's actually due to changes in blockchain regulations, market conditions, or other unrelated industry-wide factors.

- Relative growth rate of new developers increases by at least 30% compared to baseline.
- Relative growth rate of new DApps/projects increases by at least 30% compared to baseline.
- Relative growth rate of new contracts deployed on Cardano Mainnet increases by at least 30% compared to baseline.

#### Metrics relative to past years

We use the performance of past years to set the baseline for the metrics.

- Results of the Cardano Foundation's Developer Survey indicate that the developer experience has improved.

### Direct metric

The main metric to measure success is how hard is it to onboard a new developer to Cardano. We propose to measure it directly by delivering two hackathons with these characteristics (one before and one after the strategy is implemented):

- Online event (to cut costs and reach a wider audience)
- Two weeks to build the project.
- We'll promote the hackathon in other ecosystems without revealing that it's a Cardano hackathon.
- We'll offer an economic incentive (a prize of e.g. $10,000) and help to go from MVP to real product to the winner.
- We'll vet the candidates (they have to be unfamiliar with Cardano and have a solid understanding of web development and/or blockchain development).
- We won't provide any documentation, tooling, or any other support. They have to figure it out on their own.
- The project will be:
    - Secret until they start building it.
    - Something necessary for the ecosystem to grow.
    - Something that could be built by a single developer familiar with Cardano in one week of full-time work. That leaves one week for the developer to learn Cardano and the ecosystem.
    - Smart contract design and on-chain + off-chain implementation.
- We'll interview all participants to get feedback on the experience and to gather insights on the developer experience.
- We'll evaluate the projects to see how far they got and how much they learned.

We'll use the interviews, code reviews, and feedback to estimate the time and effort it takes to onboard a new developer to Cardano. Then, we'll compare the results of the two hackathons to see if the developer experience has improved.
