# Workflows

This directory contains workflow files that define step-by-step processes for common tasks.

## How to Run a Workflow

1. Open the workflow `.md` file to understand what it does
2. Ask the AI assistant: "Run the [workflow-name] workflow"
3. Provide any required inputs (file paths, URLs, etc.)
4. Follow the steps and approve changes when prompted

## Available Workflows

- `create-accessibility-issues.md` - Creates accessibility issues from Fable test results
- `update-existing-accessibility-issues.md` - Updates existing GitHub accessibility issues with new test results

## Testing Workflow Changes

1. Read the updated workflow
2. Ask the AI to run it with test data
3. Verify each step executes correctly
4. Check expected outputs

## Important Notes

- Workflows are conservative - they prefer creating new issues over modifying existing ones
- Some workflows require user approval before making changes
- Check prerequisites for required tools (e.g., GitHub CLI)
- Review proposal documents before approving changes
