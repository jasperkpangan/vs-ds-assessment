# VoiceScript Data Science Assessment

## Overview

This take-home assignment evaluates your ability to design and implement prompt engineering solutions for analyzing legal transcript data. You'll work with an AI language model to extract structured information from a legal deposition transcript.

## Project Structure

```txt
data-science-assessment/
├── README.md                    # This file
├── prompt_engineering.ipynb     # Main assignment notebook
├── transcript.txt               # Sample legal deposition transcript
├── requirements.txt             # Python dependencies
├── pyproject.toml               # Project configuration
└── uv.lock                      # UV lock file
```

## Prerequisites

- Python 3.10 or higher
- An API key for the Base10 AI model endpoint (provided separately)

## Installation

You can install the dependencies using either `uv` (recommended) or `pip`:

### Option 1: Using UV (Recommended)

```bash
# Install UV if you haven't already
# https://docs.astral.sh/uv/getting-started/installation/

# Install dependencies
uv sync
```

### Option 2: Using pip

```bash
# Create a virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

## Environment Setup

1. Create a `.env` file in the project root:

```bash
touch .env
```

2. Add your API key to the `.env` file:

```sh
BASE10_API_KEY=your_api_key_here
```

## Assignment Tasks

Complete the following tasks in the `prompt_engineering.ipynb` notebook:

### Task 1: System Prompt Design ✅

**Status**: Example provided

- Review the basic system prompt for the legal transcript analyzer
- Consider how to improve it for better performance on legal documents

### Task 2: Transcript Summarization ✅

**Status**: Example provided

- Implement transcript summarization using structured output
- Review the model's reasoning process
- Evaluate the quality of the generated summary

### Task 3: Legal Proceeding Classification 🔄

**Status**: To be completed

- Design a prompt to classify the type of legal proceeding
- Create an appropriate Pydantic model for the classification
- Implement the classification logic
- Test and validate the results

### Task 4: Speaker Identification 🔄

**Status**: To be completed

- Extract and identify all speakers mentioned in the transcript
- Create a structured output format for speaker information
- Include speaker roles and any other relevant metadata

### Task 5: Cross-Talk Detection 🔄

**Status**: To be completed

- Identify sections where speakers talk over each other
- Analyze interruptions and overlapping speech patterns
- Provide timestamps and context for cross-talk incidents

## Key Requirements

### Technical Requirements

- Use the provided `instructor` library for structured outputs
- Implement Pydantic models for each task's output format
- Use appropriate prompt engineering techniques
- Handle the transcript data efficiently

### Evaluation Criteria

- **Prompt Design**: Quality and effectiveness of your prompts
- **Data Modeling**: Appropriate use of Pydantic models for structured outputs
- **Code Quality**: Clean, well-documented, and maintainable code
- **Analysis Quality**: Accuracy and completeness of extracted information
- **Insights**: What you learned from this process

## Getting Started

1. Open the Jupyter notebook:

```bash
jupyter lab prompt_engineering.ipynb
```

or run Jupyter Lab with uv (optional)

```bash
uv run jupyter-lab
```

You can also use any environment configuration which is most comfortable for you to use for this assignment.

2. Run the initial setup cells to:
   - Import required libraries
   - Load environment variables
   - Initialize the OpenAI client with instructor

3. Work through each task section, completing the TODO items

## Data Description

The `transcript.txt` file contains a legal deposition transcript with:

- **Format**: Timestamped dialogue in pipe-separated format
- **Speakers**: Multiple speakers labeled as Speaker A, Speaker B, Speaker C
- **Content**: Environmental law deposition regarding site remediation
- **Duration**: Approximately 8 minutes of recorded dialogue
- **Features**: Includes interruptions, objections, and technical difficulties

## Submission Guidelines

Your submission should include:

1. Completed `prompt_engineering.ipynb` notebook with all tasks implemented
2. Well-documented code with clear explanations
3. Analysis and discussion of your approach for each task
4. Any insights or challenges encountered during implementation

## Tips for Success

1. **Start with the transcript**: Read through the entire transcript to understand the context
2. **Iterate on prompts**: Don't expect perfect results on the first try - refine your prompts
3. **Use structured outputs**: Leverage Pydantic models for consistent, parseable results
4. **Test thoroughly**: Validate your solutions with different parts of the transcript
5. **Document your thinking**: Include markdown cells explaining your approach and decisions

## Dependencies

- `instructor`: For structured LLM outputs with Pydantic models
- `openai`: OpenAI API client for model interactions
- `python-dotenv`: Environment variable management
- `jupyterlab`: Interactive notebook environment

## Support

If you encounter technical issues:

1. Check that your API key is correctly set in the `.env` file
2. Verify all dependencies are installed
3. Ensure you're using Python 3.10 or higher
4. Review the error messages for specific guidance

Good luck with your assessment!
