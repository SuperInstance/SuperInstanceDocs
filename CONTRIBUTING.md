# Contributing to SuperInstance Documentation

Thank you for your interest in contributing to the SuperInstance documentation! This site is built with Next.js and serves as the official documentation for the SuperInstance ecosystem.

## Table of Contents

- [Quick Start](#quick-start)
- [Development Environment Setup](#development-environment-setup)
- [Development Workflow](#development-workflow)
- [Documentation Guidelines](#documentation-guidelines)
- [Content Standards](#content-standards)
- [Submitting Changes](#submitting-changes)
- [Getting Help](#getting-help)

---

## Quick Start

```bash
# Clone the repository
git clone https://github.com/SuperInstance/superinstance-docs.git
cd superinstance-docs

# Install dependencies
npm install

# Start the development server
npm run dev

# Make your changes
# ... edit files ...

# Test your changes
# Visit http://localhost:3000

# Submit a pull request
```

---

## Development Environment Setup

### Prerequisites

**Required:**
- Node.js 18+ (20+ recommended)
- npm 9+ or pnpm 8+
- Git 2.30+

**Recommended:**
- 4GB+ RAM
- Modern web browser
- VS Code with recommended extensions

### Installation

```bash
# Fork the repository on GitHub first
# Then clone your fork
git clone https://github.com/YOUR_USERNAME/superinstance-docs.git
cd superinstance-docs

# Install dependencies
npm install

# Start the development server
npm run dev

# Verify setup
# Open http://localhost:3000 in your browser
```

### Project Structure

```
superinstance-docs/
├── app/                    # Next.js app directory
│   ├── docs/              # Documentation pages
│   ├── layout.tsx         # Root layout
│   └── page.tsx           # Homepage
├── components/            # React components
├── lib/                   # Utility functions
├── public/               # Static assets
├── styles/               # Global styles
├── next.config.js        # Next.js configuration
├── package.json          # Dependencies
└── tsconfig.json         # TypeScript configuration
```

### IDE Configuration

**VS Code (Recommended):**

Install these extensions:
- ESLint
- Prettier
- TypeScript and JavaScript Language Features

---

## Development Workflow

### Finding Something to Work On

- Check [GitHub Issues](https://github.com/SuperInstance/superinstance-docs/issues) for open tasks
- Look for labels: `documentation`, `good first issue`, `content`
- Review documentation gaps by browsing the site
- Comment on the issue to claim it

### Creating a Branch

```bash
# Ensure you're on main and up to date
git checkout main
git pull origin main

# Create a documentation branch
git checkout -b docs/your-changes

# Branch naming conventions:
# docs/ - Documentation content changes
# fix/ - Bug fixes
# feat/ - New features
# chore/ - Maintenance tasks
```

### Making Changes

**Types of Contributions:**
- Writing new documentation pages
- Improving existing content
- Fixing typos and errors
- Adding code examples
- Translating documentation
- Improving site structure/navigation

### Commit Messages

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```
type(scope): description

[optional body]
```

**Types:**
- `docs` - Documentation content changes
- `fix` - Bug fixes
- `feat` - New features
- `style` - Visual/styling changes
- `refactor` - Code refactoring
- `chore` - Maintenance tasks

**Examples:**
```bash
git commit -m "docs(api): add authentication guide"
git commit -m "docs(intro): clarify getting started steps"
git commit -m "fix(routing): resolve broken navigation link"
```

---

## Documentation Guidelines

### Writing Style

**Principles:**
- **Clear and Concise**: Use simple language, avoid jargon
- **Active Voice**: "Click the button" not "The button should be clicked"
- **Inclusive**: Use gender-neutral language
- **Scannable**: Use headings, lists, and formatting effectively

### Content Structure

**Documentation Page Structure:**
```markdown
# Title

Brief introduction (1-2 sentences).

## Overview

Detailed explanation of the topic.

## Prerequisites

What users need before starting.

## Steps/Content

Main content with clear sections.

### Sub-section

More detailed information.

## Examples

Code examples with explanations.

## See Also

Links to related documentation.
```

### Markdown Formatting

```markdown
# Use ATX-style headings (don't close them)

## Subheading

### Sub-subheading

- Use hyphens for lists
- Keep lists to 7 +/- 2 items

1. Number lists for sequential steps
2. Each step should be actionable
3. Include expected outcomes

> Use blockquotes for important notes

**Bold** for emphasis
*Italic* for terminology

`code` for inline code

```language
// Code blocks with language hint
function example() {
  return true;
}
```

[Descriptive link text](url)
```

### Code Examples

**Guidelines:**
1. **Language Labels**: Always specify the language
2. **Comments**: Add helpful comments
3. **Completeness**: Examples should be runnable
4. **Context**: Explain what the code does
5. **Output**: Show expected output when helpful

````markdown
```javascript
// Create a new SuperInstance client
const client = new SuperInstance({
  apiKey: process.env.SUPERINSTANCE_API_KEY,
});

// Connect to the service
await client.connect();
console.log('Connected successfully!');
```
````

### Images and Diagrams

**Guidelines:**
- **Format**: PNG for screenshots, SVG for diagrams
- **Size**: Keep under 300KB
- **Alt Text**: Always include descriptive alt text
- **Light/Dark**: Consider both themes

```markdown
![Screenshot of the dashboard interface](/images/dashboard.png)

*Figure 1: The main dashboard shows recent activity*
```

### Links

**Internal Links:**
```markdown
[Getting Started](/docs/getting-started)
[API Reference](/docs/api/reference)
```

**External Links:**
```markdown
[Next.js Documentation](https://nextjs.org/docs)
[React Hooks](https://react.dev/reference/react)
```

**Link Text:**
- Use descriptive text, not "click here"
- Keep link text concise
- Match link text to page title when possible

---

## Content Standards

### Documentation Types

We have several types of documentation:

1. **Tutorials**: Step-by-step learning guides
2. **How-to Guides**: Practical instructions for specific tasks
3. **Reference**: Technical specifications and APIs
4. **Explanation**: Conceptual background and context

### Quality Checklist

Before submitting, ensure:

- [ ] Content is accurate and up-to-date
- [ ] Code examples are tested and working
- [ ] Links are valid and not broken
- [ ] Images have alt text
- [ ] Spelling and grammar are correct
- [ ] Markdown formatting is proper
- [ ] Content is inclusive and welcoming
- [ ] Page has a clear purpose
- [ ] Title is descriptive and concise

### SEO Best Practices

- **Titles**: Clear, descriptive, include relevant keywords
- **Descriptions**: Add meta descriptions for important pages
- **URLs**: Use clean, descriptive URLs
- **Headings**: Use proper heading hierarchy (h1 > h2 > h3)

### Accessibility

- **Alt Text**: All images have descriptive alt text
- **Headings**: Proper heading hierarchy
- **Links**: Descriptive link text
- **Color**: Sufficient contrast ratios
- **Language**: Clear, simple language

---

## Submitting Changes

### Before Submitting

- [ ] Build succeeds (`npm run build`)
- [ ] No linting errors (`npm run lint`)
- [ ] All links work
- [ ] Images load correctly
- [ ] Content is proofread
- [ ] Code examples tested

### Testing Your Changes

```bash
# Start development server
npm run dev

# Visit http://localhost:3000

# Check:
# - Your new/modified pages render correctly
# - Navigation works
# - No console errors
# - Links are valid
# - Images load
# - Mobile responsive (use browser dev tools)
```

### Creating the Pull Request

1. **Push your branch**:
   ```bash
   git push origin docs/your-changes
   ```

2. **Create PR on GitHub**:
   - Go to https://github.com/SuperInstance/superinstance-docs
   - Click "New Pull Request"
   - Select your branch
   - Fill out the PR template

3. **PR Template**:
   ```markdown
   ## Description
   Brief description of documentation changes

   ## Type of Change
   - [ ] New documentation
   - [ ] Documentation update
   - [ ] Bug fix
   - [ ] Translation
   - [ ] Site improvement

   ## Content Changes
   - What pages were added/modified
   - What topics are covered
   - Any breaking changes to documentation structure

   ## Testing
   - [ ] Build succeeds locally
   - [ ] All links verified
   - [ ] Images load correctly
   - [ ] Tested on mobile (if applicable)

   ## Screenshots
   (If applicable) Add screenshots

   ## Checklist
   - [ ] Content follows style guide
   - [ ] Code examples tested
   - [ ] Proofread for errors
   - [ ] Accessibility considered
   ```

### During Review

- Respond to feedback promptly
- Make requested changes
- Push updates to the same branch
- Ask questions if anything is unclear

---

## Getting Help

### Documentation

- [README.md](README.md) - Project overview
- [Next.js Docs](https://nextjs.org/docs) - Framework documentation
- [Content Guide](./CONTENT_GUIDE.md) - Detailed content guidelines

### Community Resources

- **GitHub Issues**: Bug reports and documentation issues
- **GitHub Discussions**: Questions and ideas
- **Email**: dev@superinstance.ai

### Asking Good Questions

Before asking, please:

1. **Search first**: Check existing issues and docs
2. **Be specific**: Describe what you're documenting
3. **Provide context**: What users need to know
4. **Share examples**: Show what you've tried
5. **Be patient**: Maintainers are volunteers

---

## Documentation Needs

Looking for something to contribute? Here are some areas that need attention:

### High Priority
- [ ] API reference documentation
- [ ] Getting started improvements
- [ ] More code examples
- [ ] Error handling documentation

### Medium Priority
- [ ] Integration guides
- [ ] Troubleshooting guides
- [ ] Performance best practices
- [ ] Migration guides

### Low Priority
- [ ] Video tutorials (embed or link)
- [ ] Interactive examples
- [ ] Community contributions showcase
- [ ] Translating to other languages

---

## Recognition

We value all contributions! Contributors will be:

- Listed in CONTRIBUTORS.md
- Mentioned in relevant documentation
- Recognized in community communications

Thank you for contributing to SuperInstance Documentation!

---

*Last Updated: 2026-01-10*
