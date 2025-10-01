# Copilot Instructions for Phitron AI/ML Course

## Project Overview
This is a structured AI/ML learning project organized by daily lessons. The project uses Python 3.14+ with modern tooling including `uv` for dependency management and supports both Jupyter notebooks and Marimo reactive notebooks.

## Project Structure
- `Day_XX/` directories contain daily lesson materials
- Each day includes both `.ipynb` (Jupyter) and `.py` (Marimo) versions of exercises
- `main.py` serves as the project entry point
- Dependencies managed via `pyproject.toml` and `uv.lock`

## Development Environment
- **Python Version**: 3.14+ (specified in `.python-version`)
- **Package Manager**: `uv` (modern pip replacement)
- **Notebook Frameworks**: 
  - Jupyter notebooks (`.ipynb`) for interactive learning
  - Marimo notebooks (`.py` with `marimo.App`) for reactive programming

## Key Dependencies
- `marimo>=0.16.2` - Reactive notebook framework
- `numpy>=2.3.3` - Numerical computing
- `pandas>=2.3.2` - Data manipulation
- `uvicorn==0.35.0` - ASGI server (likely for web apps)

## Coding Patterns

### Daily Lesson Structure
Each `Day_XX/` directory follows this pattern:
```
Day_01/
├── 01_Basic.ipynb  # Jupyter notebook version
└── 01_Basic.py     # Marimo reactive version
```

### Marimo Notebook Pattern
Marimo files use this structure:
```python
import marimo
app = marimo.App(width="full")

@app.cell
def _():
    # Cell content here
    return

if __name__ == "__main__":
    app.run()
```

### Learning Content Style
- Extensive comments explaining concepts (see `Day_01/01_Basic.ipynb`)
- Summary sections with numbered points for key concepts
- Practical examples demonstrating Python fundamentals
- Focus on beginner-friendly explanations with real-world applications

## Development Workflow
1. **Running Marimo notebooks**: `python Day_XX/filename.py` or `marimo run Day_XX/filename.py`
2. **Jupyter notebooks**: Use VS Code's built-in Jupyter support
3. **Dependencies**: Install with `uv sync` (auto-reads `pyproject.toml`)
4. **Adding packages**: Update `pyproject.toml` dependencies array

## AI Agent Guidelines
- When creating new lessons, follow the `Day_XX/` naming convention
- Always provide both `.ipynb` and `.py` (Marimo) versions for consistency
- Include comprehensive comments explaining concepts for learning purposes
- Use practical examples that demonstrate real-world applications
- Structure code with clear sections and educational summaries
- Prefer `uv` commands over `pip` for package management
- When working with notebooks, ensure proper cell organization and execution flow

## Educational Focus
This project emphasizes learning fundamentals with clear explanations. When adding content:
- Explain concepts thoroughly with comments
- Provide multiple examples for complex topics
- Include summary sections to reinforce key points
- Use progressive complexity (basic to advanced)
- Demonstrate practical applications of theoretical concepts