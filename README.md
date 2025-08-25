# Claude Code Refactor Agents

A comprehensive set of AI agents designed to systematically analyze, plan, execute, and report on code refactoring tasks within Claude Code environments.

## 🎯 Project Background

When using Claude Code for large-scale software development, projects often face rapid architectural complexity growth. Common issues include:

- **Code Duplication**: Similar logic scattered across multiple files
- **Large Files**: Monolithic files that are difficult to maintain
- **Scattered Functionality**: Related features spread across different modules
- **Mixed File Types**: Test files, documentation, and source code intermingled
- **AI-Generated Artifacts**: Small tests and documentation files that need consolidation

These issues compound over time, making codebases increasingly difficult to maintain and extend.

## 🚀 Solution Overview

This project provides a **4-phase structured approach** to code refactoring using specialized Claude Code agents:

### Phase 1: Assessment (Judgment Agent)
- Analyzes codebase health using quantitative metrics
- Identifies code smells and architectural issues
- Provides a 5-tier recommendation system:
  - **Strongly Recommend** - Critical issues requiring immediate attention
  - **Highly Recommend** - Significant issues affecting maintainability
  - **Recommend** - Moderate issues worth addressing
  - **Can Wait** - Minor issues that can be deferred
  - **Not Needed** - Codebase is in good condition

### Phase 2: Planning (Planning Agent)  
- Creates detailed refactoring strategy based on assessment
- Ensures comprehensive test coverage before refactoring
- Plans step-by-step execution with safety checkpoints
- Prioritizes maintaining functional consistency throughout the process

### Phase 3: Execution (Execution Agent)
- Implements refactoring plan with strict adherence to the strategy
- Runs automated tests after each modification step
- Maintains system stability through continuous validation
- Stops immediately if any tests fail

### Phase 4: Reporting (Reporting Agent)
- Generates comprehensive before/after analysis
- Quantifies improvements in code metrics
- Documents consolidated files and removed duplications
- Provides actionable insights for future development

## 📁 Repository Structure

```
CCRefactorAgents/
├── README.md                 # This file
├── judgment-agent.md         # Phase 1: Code health assessment agent
├── planning-agent.md         # Phase 2: Refactoring strategy planning agent  
├── execution-agent.md        # Phase 3: Safe refactoring execution agent
└── reporting-agent.md        # Phase 4: Results analysis and reporting agent
```

## ⚙️ Configuration

### Option 1: Using Claude Code `/agents` Command (Recommended)

1. **Add Agents to Claude Code**:
   ```bash
   /agents
   ```

2. **Manual Configuration for Each Agent**:
   - Select "Manual Configuration"
   - Copy the content from the respective `.md` files:
     - `judgment-agent.md` for assessment
     - `planning-agent.md` for planning
     - `execution-agent.md` for execution
     - `reporting-agent.md` for reporting
   - Paste into the System Prompt field
   - **Tool Selection**: Select **ALL available tools** for maximum effectiveness

### Option 2: Model Selection Recommendations

#### For Maximum Quality:
- **Assessment & Planning**: Use **Claude Opus** for deeper analysis and strategic thinking
- **Execution & Reporting**: Use **Claude Sonnet** for efficient implementation and documentation

#### For Cost-Effectiveness:
- **All Phases**: Use **Claude Sonnet** for balanced performance and cost
- **Alternative**: Use **Gemini CLI** for assessment and planning phases

### Option 3: Direct Integration

Copy the agent prompts directly into your Claude Code session when needed:

```bash
# Assessment Phase - paste judgment-agent.md content
# Planning Phase - paste planning-agent.md content  
# Execution Phase - paste execution-agent.md content
# Reporting Phase - paste reporting-agent.md content
```

## 🛠 Usage Instructions

Each agent is designed to be used sequentially within Claude Code:

### 1. Assessment Phase
```bash
# Use the judgment-agent.md prompt with your codebase
# Input: Your entire codebase
# Output: Health assessment with 5-tier recommendation
```

### 2. Planning Phase  
```bash
# Use the planning-agent.md prompt if refactoring is recommended
# Input: Assessment report + codebase
# Output: Detailed refactoring plan with test requirements
```

### 3. Execution Phase
```bash
# Use the execution-agent.md prompt after plan approval
# Input: Refactoring plan + codebase + test runner
# Output: Step-by-step execution with test validation
```

### 4. Reporting Phase
```bash
# Use the reporting-agent.md prompt after successful execution
# Input: Before/after codebase snapshots + initial assessment
# Output: Quantified improvement report
```

## 🔧 Key Features

- **Safety-First Approach**: Every refactoring step includes test validation
- **Quantitative Analysis**: Data-driven decisions based on concrete metrics
- **Incremental Progress**: Small, verifiable steps prevent system breakage
- **Comprehensive Documentation**: Clear planning and reporting for accountability
- **Claude Code Optimized**: Designed specifically for Claude Code workflows

## 📊 Metrics Tracked

The agents monitor and improve:
- Code duplication percentage
- Average file length
- Function complexity
- Module cohesion
- Test coverage
- Documentation consolidation
- File organization

## 🤝 Contributing

This is an open-source project. Contributions are welcome through:
- Bug reports and feature requests
- Agent prompt improvements
- Additional metrics and analysis capabilities
- Documentation enhancements

## 📄 License

MIT License - Feel free to use, modify, and distribute these agents for your projects.

## 🏗 Architecture

Each agent follows a structured prompt format with:
- **Role Definition**: Clear agent responsibility
- **Task Context**: Background and objectives
- **Input/Output Specifications**: Defined data formats
- **Rules and Constraints**: Safety and quality guidelines
- **Step-by-Step Thinking**: Logical processing flow
- **Example Interactions**: Usage demonstrations

This systematic approach ensures consistent, reliable refactoring outcomes across different codebases and project types.