# Developer Experience Strategy for 2026/27

This repository contains an ecosystem-wide strategy to improve DevX (developer experience) in Cardano. It is not an official statement from any entity but a document used to gather feedback from and align with the companies of the ecosystem that work on tooling, libraries, documentation, and other aspects that affects the DevX in Cardano.

The structure is as follows:

1. [Vision](#vision)
1. [Executive Summary](#executive-summary)
1. [Why is this strategy needed?](#why-is-this-strategy-needed)
    1. Builders are fundamental for the success of the ecosystem.
    2. Cardano has a DevX issue
    3. An ecosystem-wide strategy is needed
1. [Strategy](#strategy)
1. [Deliverables](#deliverables)
1. [How we will measure success](#how-we-will-measure-success)
1. [Teams on board with this strategy](#teams-on-board-with-this-strategy)
1. [Conclusion](#conclusion)

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

The difference in developer is not **_only_** a matter of "token go up, developer activity goes up". As we can see in the following chart (number of new developers vs token price for all three ecosystems), even if there is a clear correlation, it's far from being a 1:1 relationship.

![New developers vs token price](./assets/new-devs_vs_price.png)

One thing to notice is that there's a delay between token price and developer activity. Both going up and going down. And that the ecosystem that manages to retain developers after the token price drops, might carry significant advantage over the rest.

### Developer survey results

The developer survey results are an even stronger indicator of the DevX issue. It's worth reviewing the survey results in detail to understand the full picture, but here I'll present the most relevant points:

- "Over 60% of respondents report more than seven years of software engineering experience, with another 25% in the 2–7 year range. Early-career developers remain a minority at roughly 15%, consistent with 2024. Compared with broader industry benchmarks such as the Stack Overflow Developer Survey, **the Cardano ecosystem remains significantly more senior than average**". This suggests that Cardano is more appealing to seasoned engineers rather than newcomers. Or, to give a better framing, that Cardano **is not appealing** to newcomers.
- For question 12: "What should be the biggest priority on the Cardano technical roadmap?", the option with the second and third highest rankings (behind higher-throughput) were "Better documentation and explainers" and "Accessibility & use cases enablers". Suggesting that lack of proper documentation and explainers are a big concern, and that there's significant barrier to implement use cases.
- For question 15: "How satisfied are you with the current state of the smart contract ecosystem?", the median satisfaction score was 7 with a tight interquartile range (6–8), suggesting writing smart contracts themselves is not perfect but acceptable, and that the DevX issues are likely elsewhere (e.g., testing, debugging, and transaction ergonomics, etc.)
- For question 24: "It would be nice if there were a CLI for... ", shows that requests for new CLI tooling in 2025 consistently point toward higher-level, end-to-end workflows rather than additional low-level primitives.
- For question 28: "What do you think is the biggest pain point of Cardano's developer ecosystem?", we get a lot of insights, but for this brief, we'll limit ourselves with the final comment: "The dominant pain points expressed in 2025 cluster around developer experience rather than protocol capability, with fragmentation of tooling, weak off-chain/on-chain integration, and the absence of mature transaction-building abstractions recurring across responses. Compared to 2024, the emphasis shifts from documentation alone toward a broader critique of ecosystem cohesion: duplicated efforts, unclear “blessed paths,” and insufficiently maintained libraries amplify the already steep eUTxO learning curve. In contrast to ecosystems like Ethereum—where complexity is often hidden behind opinionated frameworks—Cardano developers still shoulder much of the architectural burden directly, slowing onboarding and experimentation despite strong underlying primitives".
- For question 31: "On average, how satisfied are you with the technical answers/details you find in documentation and within the community?", provides a median score of 7 with a notably tight interquartile range (6–7). This suggests moderate satisfaction coupled with broad agreement, indicating that most developers converge on a “good enough, but not great” assessment of technical answers. The narrow spread also implies that frustrations around documentation quality and answer depth are widely shared rather than isolated to specific subgroups. We don't have data if it's the documentation or the community the resource that provides more value.

### Conclusion

By taking into account all the previously discussed insights, it's safe to conclude that Cardano's DevX needs to improve if we want to increase the amount and retention of developers in the ecosystem.

</details>

<details>

<summary>An ecosystem-wide strategy that aligns the efforts of the different actors in the ecosystem is needed</summary>

Based on what we discussed in the previous point and the Cardano Developer Survey, we know there's:

- Lack of tooling integration and ecosystem cohesion paired with insufficient coordination.
- Fragmented, immature, and unmaintained tooling, libraries, and documentation.
- Lack of plug-and-play libraries, friendly abstractions, reference implementations, and LLM support.

If the problem were localized on a specific tool, documentation, or library, it'd make sense to invest most of our work into improving those. However, the developer ecosystem is so varied and constantly changing, that our best bet is to embrace and be prepared for that. That's why this strategy is needed, because there's no single entity, tool, or website with enough developer share, and we need to work together to have a real shot at improving the overall DevX of Cardano.

</details>

## Strategy

To execute this strategy, we'll have a dedicated team to deliver the next items (sometimes in collaboration with other teams).

## Deliverables

Primary items are the ones that have the highest impact. Secondary items are the ones that support or build on top of primary items. 

| Item | Primary | Overview | Why | Expected Outcome |
| --- | ---| --- | --- | --- |
| [Community Alignment and Collaboration](./deliverables/alignment.md) | Yes | The most important item: Aligning the ecosystem with this strategy. Map all ecosystem tooling, creating a baseline for the "New Tooling" Epic. Contributing to community tooling (with an emphasis on off-chain/integration). Improving existing DApp development tooling (LSPs, extensions, TUIs, etc.). | See [why is this needed](#why-is-this-strategy-needed) | A clear roadmap of the ecosystem's developer experience with a list of companies/projects that support it. |
| 🔴 [Setup CLI](./deliverables/starter-cli.md) | Yes | Create a Setup CLI/TUI to easily start dapp projects. A "create-react-app" for Cardano, where users can pick any desired stack combination. This high-level umbrella tool will leverage all identified tooling, provide AI/LLM-native commands, and use algorithmic ranking to select tools. | TODO | TODO |
| 🔴 [Developer HUB](./deliverables/developer-hub.md) | Yes | Create (or adapt) the entry point HUB. Our first option is to align with the CF to use developers.cardano.org. The objective is to have a single entry point for developers new to Cardano. Define and organize onboarding content for three key user paths: EVM/Blockchain developer, Web2 developer, and Non-technical interested user. Add a CI/CD pipeline to maintain working code snippets. | TODO | TODO |
| 🔴 [Developer Outreach](./deliverables/outreach.md) - Discord | No | Maintain a healthy Discord channel and respond to every message within a day, at most. | TODO | TODO |
| [UTxO Design Patterns and best practices]( | Yes | Add explanations and examples of common UTxO design patterns (including composability) to the HUB. | TODO | TODO |
| [AI/LLM native](./deliverables/llms.md) - LLM.txt for all docs | Yes | Add an LLM.txt file to all documentation resources. | TODO | TODO |
| 🔴 [OpenZeppelin-like library](./deliverables/openzeppelin.md) | Yes | Design and implement standardized and reusable smart contracts (on- and off-chain, emphasis on DeFi) with related tooling/platform. Create the infrastructure, website, and add at least 5 ready-to-audit smart contracts. | TODO | TODO |
| 🔴 [CIP and Pentad Integration support](./deliverables/cip-and-pentad.md) | No | Push for community agreement and resolution of key DevX and DeFi CIPs: standardization of CBOR objects, Account Address Enhancement (CIP-159), nested transactions (CIP-118), and programmable tokens (CIP-113). Propagate changes post-acceptance (e.g., help the community update tooling). | TODO | TODO |
| New Tooling - Extend Setup CLI/TUI (continuation) | Merge | Extend the Setup CLI/TUI to support Docker and Nix, and add more on-chain and off-chain options. Tasks include adding missing popular tools, implementing infrastructure for tool health checks, and containerizing and resolving dependencies. | TODO | TODO |
| IDE/VSCode Plugin(s) | No | Develop tooling to manage canonical representation friction. Includes a CBOR analyzer/interpreter (VSCode/TUI) and an Error translation layer to improve node error messaging for developers. | TODO | TODO |
| Documentation - Pushing Plutus' limits | No | Add explanations and examples of experimental and "hacky" ways to increase smart contract throughput and possibilities to the HUB. | TODO | TODO |
| LLMs - MCP Server for integrated docs | Merge | Create an MCP server to integrate and access all documentation deliverables. | TODO | TODO |
| Developer Outreach - Hackathons + Build Club | No | Host hackathon(s) (ideally at cross-chain events, with an emphasis on DeFi, alternative, online) to identify candidates for a subsequent build club. Provide pre-hackathon support and offer as a prize technical support and help securing external funding. | TODO | TODO |
| Exploratory | No | R&D of potential low-hanging fruit DevX improvements. Tasks could include: integrating a no-code tool with a daemon to sync Tx3 code/diagrams; generating off-chain types from CIP-57 + extending blueprints; using an embedded UPLC interpreter for error-driven off-chain development. | TODO | TODO |
| Documentation - Update Patterns & Best Practices | Yes | Update best practices, examples, and patterns for CIP-159, CIP-118, and CIP-113, dependent on the completion of the "CIPs Implementations" deliverable. | TODO | TODO |
| LLMs - Agent Skills for Common Actions | Merge | Create a set of Claude skills for common development actions (e.g., testing contracts, updating dependencies, etc.) and integrate them with Starter CLI. | TODO | TODO |
| Developer Outreach - Live Streams & Videos | No | Host live streams tailored to new developers, covering coding and Q&A. Clip and edit live streams into bite-sized content, and create short video tutorials (<5min). | TODO | TODO |
| Pentad Integrations | No | Support integrations (Stablecoins, Bridges, Oracles), focusing on exposing features and defining the ideal UX/onboarding flow for developers. | TODO | TODO |


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
