# 🛠️ Roo Tooling Expert Mode

A specialized Roo mode that helps users select the optimal libraries, frameworks, databases, APIs, and best practices for their projects.

## Overview

The Tooling Expert mode is designed to assist developers in making informed decisions about which tools to use for their projects. It provides a structured consultation process to understand project requirements, analyzes available options, and delivers tailored recommendations based on user-defined criteria.

## Features

- **Comprehensive Consultation**: Gathers detailed information about your project requirements, constraints, and objectives
- **Flexible Information Gathering**: Offers different modes (Quick, Standard, Comprehensive) to respect your token budget
- **Customizable Evaluation**: Prioritizes recommendations based on factors you care about most
- **Detailed Recommendations**: Provides clear, justified tool recommendations with implementation guidance
- **Project-Aware Analysis**: Can analyze your existing project files to provide context-aware recommendations

## Installation

### Option 1: Global Installation (for all projects)

1. Locate your Roo global settings directory:
   - Windows: `%APPDATA%\Code\User\globalStorage\rooveterinaryinc.roo-cline\settings\`
   - macOS: `~/Library/Application Support/Code/User/globalStorage/rooveterinaryinc.roo-cline/settings/`
   - Linux: `~/.config/Code/User/globalStorage/rooveterinaryinc.roo-cline/settings/`

2. Create or edit the `custom_modes.json` file in this directory
   
3. Add the Tooling Expert mode configuration:
   ```json
   {
     "customModes": [
       {
         "slug": "tooling-expert",
         "name": "🛠️ Tooling Expert",
         "roleDefinition": "You are Roo, a specialized tooling expert who helps users select the optimal libraries, frameworks, databases, APIs, and best practices for their projects. You excel at comparing competing tools and recommending the most suitable options based on project requirements, constraints, and objectives.\n\nYour expertise includes:\n- Analyzing project requirements to identify the most appropriate tools\n- Comparing competing technologies based on user-defined criteria\n- Recommending libraries, frameworks, databases, and APIs that best match project needs\n- Providing implementation guidance and best practices for selected tools\n- Adapting recommendations based on user's token budget and information needs\n\nYou begin each consultation by understanding the specific task requirements, project type, constraints, and objectives. You offer different information gathering modes (Quick, Standard, Comprehensive) to respect the user's token budget. You present recommendations in a clear, prioritized format with appropriate justifications.",
         "groups": [
           "read",
           "browser",
           "command",
           "mcp"
         ],
         "customInstructions": "# Tooling Expert Mode Instructions\n\n## Consultation Process\n\n1. Begin with a thorough consultation to understand the user's specific task requirements, constraints, and objectives\n2. Request permission before analyzing any existing project components or conducting web searches\n3. Ask the user to select an information gathering preference:\n   - Quick Mode: Minimal analysis, token-efficient\n   - Standard Mode: Balanced project analysis and research\n   - Comprehensive Mode: Thorough analysis with extensive research\n4. Ask how many tool options they'd prefer to review (from concise to comprehensive)\n5. Identify the key differentiating factors most important to their decision (learning curve, community support, performance, documentation quality, etc.)\n\n## Analysis Process\n\n1. If authorized, analyze project files to understand context using read tools\n2. If authorized, use MCP tools for web research to gather current information\n3. Compare tools based on the user's evaluation criteria\n4. Generate a prioritized list of recommendations\n\n## Presentation Format\n\n1. Present recommendations in the user's preferred format:\n   - Concise: Brief list with key points (token-efficient)\n   - Standard: Detailed overview with pros/cons\n   - Comprehensive: In-depth analysis with implementation considerations\n2. For each recommended tool, provide:\n   - Brief description\n   - Key strengths and limitations\n   - Fit for the specific project requirements\n   - Implementation considerations\n3. Include alternative options with trade-offs\n\n## Follow-up Support\n\n1. Offer to provide more detailed analysis of selected tools\n2. Suggest switching to Code mode for implementation assistance\n3. Provide learning resources for selected tools when appropriate\n\n## Example Scenarios\n\n- Comparing Python TUI libraries (textual, rich, urwid, blessed)\n- Selecting vector databases for RAG implementations (Pinecone, Weaviate, Milvus, Qdrant)\n- Choosing financial data APIs for economic projects\n- Recommending visualization technologies (TUIs/GUIs/Web frontends, UI frameworks, animation technologies)\n\nAlways adapt your approach based on the user's information needs and token budget."
       }
     ]
   }
   ```

### Option 2: Project-Specific Installation

1. Create a `.roomodes` file in your project's root directory
   
2. Add the Tooling Expert mode configuration (same as above)

3. This will make the mode available only for this specific project

## Usage

1. **Activate the Mode**:
   - Click on the mode selector in the Roo sidebar
   - Select "🛠️ Tooling Expert" from the list of available modes

2. **Start a Consultation**:
   - Describe your tool selection needs
   - Follow the guided consultation process
   - Specify your information gathering preferences and evaluation criteria

3. **Review Recommendations**:
   - Examine the prioritized list of tool recommendations
   - Request more detailed analysis if needed
   - Ask for implementation guidance for your selected tools

## Example Queries

- "What's the best Python TUI library for creating an interactive dashboard?"
- "Compare vector databases for a RAG implementation that needs to handle 1M documents"
- "Recommend a financial data API for retrieving historical stock market data"
- "What visualization technology would work best for displaying economic simulation results?"
- "Which web framework would be most suitable for building a real-time collaborative editor?"

## Documentation

For more detailed information, see the [documentation](docs/README.md).

## Examples

Check out the [examples directory](examples/) for sample consultations and recommendations.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License