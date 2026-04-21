# Contributing to Documentation

Thank you for your interest in improving our documentation! This guide will help you contribute effectively.

## How to Contribute

### Reporting Issues

If you find errors or have suggestions:

1. Check existing issues first
2. Create a new issue with:
   - Clear description of the problem
   - Location in documentation (file and section)
   - Suggested improvement (if applicable)

### Suggesting New Content

For new documentation requests:

1. Open an issue describing:
   - What topic needs documentation
   - Why it's important
   - Who would benefit from it

### Making Changes

1. **Fork the repository**
2. **Create a branch** for your changes:
   ```bash
   git checkout -b improve-installation-docs
   ```
3. **Make your changes** following our style guide
4. **Test your changes** (check formatting, links)
5. **Commit with clear messages**:
   ```bash
   git commit -m "Update installation steps for macOS"
   ```
6. **Push to your fork**:
   ```bash
   git push origin improve-installation-docs
   ```
7. **Create a Pull Request**

## Style Guide

### Writing Style

- Use clear, simple language
- Write in present tense
- Use active voice
- Keep sentences short
- Define technical terms on first use

### Formatting

- Use `code blocks` for commands and code
- Use **bold** for UI elements to click
- Use *italics* for emphasis (sparingly)
- Use headers to organize content hierarchically

### Examples

**Good:**
```markdown
Click **Settings** to open the configuration menu.
```

**Avoid:**
```markdown
You should click on the Settings button which will open up the configuration menu.
```

### Code Examples

- Include working code examples
- Add comments to explain complex parts
- Test all code before submitting

### Screenshots

- Use screenshots sparingly
- Ensure they're current and accurate
- Optimize file size
- Add alt text for accessibility

## Pull Request Guidelines

### Before Submitting

- [ ] Changes are focused and related
- [ ] Spelling and grammar checked
- [ ] All links tested and working
- [ ] Follows style guide
- [ ] No broken formatting

### PR Description

Include in your PR description:

- What changed and why
- Which issue it addresses (if applicable)
- Any additional context

**Example:**
```markdown
## Description
Updated the macOS installation instructions to include ARM (Apple Silicon) steps.

## Related Issue
Fixes #42

## Changes Made
- Added separate section for Intel vs ARM Macs
- Updated system requirements
- Added troubleshooting for Rosetta
```

## Review Process

1. Maintainers will review your PR
2. May request changes or clarifications
3. Address feedback and update PR
4. Once approved, it will be merged

## Questions?

- Open an issue for questions
- Join our community forum
- Email: docs-team@example.com

Thank you for contributing!
