# cardano-init

## Dependencies

[Community alignment](/deliverables/alignment.md)

## Description 

We'll create a Setup CLI/TUI to easily start DApp projects. A [Create T3 Stack](https://create.t3.gg/)/[TanStack Builder](https://tanstack.com/builder) for Cardano. Users can pick any desired stack combination from the available on-chain, off-chain, and other tooling, and we create a project ready to start working on it. This high-level umbrella tool will serve as the primary entry point for new developers setting up their first Cardano project, dramatically reducing the time from "I want to build on Cardano" to "I have a running project."

### Key aspects of this tool

- **It doesn't replace existing tooling:** The tool will leverage all identified ecosystem tooling. We don't intend this tool to replace other tools but to facilitate their adoption and usage. Hence, we won't do anything else besides setting up the project. For example, if you choose Aiken for the on-chain part and MeshJS for the off-chain, you'll still use Aiken's CLI and a JavaScript runtime to interact with them.
- **It reduces the time needed to research tooling:** The tool will provide a way for the user to easily compare and choose which tools they want to use. We'll show a combination of public signals (GitHub stars, number of contributors, commit activity, etc.) to help the user choose which tool to use or learn more about before choosing.
- **It makes it easy for newcomers:** Since it's likely that newcomers don't know which tool they want to use, we'll use an algorithmic ranking to recommend the most appropriate tools based on the developer's context and goals. We'll work with the developer community to make it as fair and objective as possible. For example, the ranking will be based on external public signals independent of this tool. That way, tooling developers don't need to optimize for anything other than the usefulness and popularity of their tool.
- **It creates an AI/LLM native project:** When creating the project, we'll add `AGENT.md` files, Agent Skills, MCPs, and other components that help developers leverage their LLMs. The contents of these files will change depending on the chosen stack.
- **It provides next steps:** To help onboard new developers, we'll provide links to the documentation, Discord servers, and other relevant/helpful links based on the chosen tech stack. We'll also include links to educational resources and examples.
- **It installs everything for you (if needed):** In the case the user doesn't have the tools installed in their environment, we'll offer installing them or using an isolated developer environment (Docker) if possible. Since, in most cases, this can be used by the standalone tool, we'll try to upstream these (and other) improvements to the underlying tool whenever possible.

## Outcome

The outcomes are:
- A developer new to Cardano has a single entrypoint independent of which tool they want to use.
- LLMs and search engines don't get confused recommending and using old and deprecated tooling (e.g., Lucid) because, if at any point, a tool stops being maintained (or a new tool is created), it will be removed (or added) to the list of available tools in this CLI.
- By checking the tool's anonymous statistics (if accepted by the developer), we can have a clearer idea of the number of developers building on Cardano and their preferences.

