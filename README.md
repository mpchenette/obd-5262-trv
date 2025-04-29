# obd-5262-trv

## Demo
### Basic Prompt Engineering
1. Comments
1. Suggestion Selector
1. Completions Panel
   - Ctrl + Enter
1. Editor Inline Chat
   - Cmd + I
1. Chat Commands
   - /help
   - /tests
      - calculator.py
      - @workspace /tests (Sonnet)
      - pytest tests/ <!-- (remove add max float if it appears) -->
   - @vscode
      - "where can I find the setting to enable Next Edit Suggestions?"

### Next Edit Suggestions
- classic Point to Point3D example
   - (remember print method and list points in comment. add z as the trigger)

### Custom Instructions
- show using to specify unit test framework
- "Prepend all suggested comments with 'Comment:'"
- "Whenever I ask a generic, non-language specific question and you want to show me code, always show me Rust."

Examples:

- Specify packages or frameworks you want Copilot to suggest
  - "Always write my Python unit tests using pytest, not unittest."
- Specify (older) versions of languages or frameworks to use
  - "When suggesting .NET code, only suggest code compatible with .NET 8."
  - Note this will not work for versions beyond the model "cut-off" date.
- Repo-wide standards or expectations for all involved developers
  - "Whenever possible, use recursion."

### Vision
   - also generating mermaid diagrams
### Agent Mode
### Copilot Code Review
- While we could ask for review in the Chat window, dedicated review is better.
1. Highlight + Right Click
   - `sql.py`
1. Code Review
   - At the end

### Public Code Block
When Public Code Block is enabled, it means, if Copilot generates code that closely matches licensed code in the public domain, the response will be blocked. However, there are ways of helping Copilot avoid suggesting public code.

- Refactor / Reframe your prompt
- Ask Copilot to break suggested code into different blocks in its response
- Ask Copilot to only show changed lines of code
- Ask Copilot to just show pseudocode
- Ask Copilot to comment out the code it suggests
- Break your problem into smaller problems

Generally speaking, when we work with our own large, complex, unique codebases, we won't run into this much. This will mostly come into play when we are starting from scratch or asking Copilot for generic examples. The alternative to the Public Code Block is Code Referencing, where Copilot will show the public code anyway and let you know what type of license applies to the repo it is sourced from.

### Content Exclusions

