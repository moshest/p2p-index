# P2P Projects Index

P2P Projects Index is a curated documentation repository containing a
comprehensive list of peer-to-peer decentralized projects organized by category.
This is a documentation-only repository focused on maintaining an up-to-date
index of P2P technologies.

Always reference these instructions first and fallback to search or bash
commands only when you encounter unexpected information that does not match the
info here.

## Working Effectively

This is a documentation-only repository - there are no source code files,
build systems, or application components to compile or run.

### Repository Setup

- No dependencies to install
- No build process required
- No application to run
- No tests to execute

### Essential Tools for Validation

Install markdown validation tools:

- `npm install -g markdownlint-cli` -- installs in 10 seconds
- `npm install -g markdown-link-check` -- installs in 8 seconds

### Core Validation Commands

Always run these validation commands before committing changes:

- `markdownlint README.md` -- validates markdown formatting (completes in 2 seconds)
- `markdown-link-check README.md` -- checks all links for availability (takes
  60-120 seconds, NEVER CANCEL)

## Validation

### Required Validation Steps

ALWAYS perform these validations when making changes:

1. **Markdown Formatting Validation**
   - Run `markdownlint README.md`
   - Fix any formatting issues identified
   - Common issues: line length, multiple blank lines, bare URLs

2. **Link Validation**
   - Run `markdown-link-check README.md` with timeout of 180 seconds minimum
   - NEVER CANCEL this command - link checking can take 60-120 seconds
   - Note: Some links may appear broken due to network restrictions but should
     be verified manually
   - GitHub repository links (github.com URLs) are typically reliable

3. **Content Structure Validation**
   - Ensure new projects are added to the correct category section
   - Maintain consistent formatting: `* [**ProjectName**](URL)\nProject description.`
   - Preserve alphabetical ordering within categories when possible

### Manual Testing Scenarios

When adding or modifying project entries:

- Verify the project link opens to the correct homepage
- Confirm the project description accurately reflects its purpose
- Ensure the project fits the intended category
- Check that the project is genuinely peer-to-peer/decentralized

## Common Tasks

### Adding a New P2P Project

1. Identify the correct category section in README.md
2. Add entry using format: `* [**ProjectName**](URL)\nProject description.`
3. Run validation commands: `markdownlint README.md && markdown-link-check README.md`
4. Fix any formatting issues identified

### Updating Project Information

1. Locate the project entry in README.md
2. Update the URL or description as needed
3. Run validation commands to ensure changes don't break formatting
4. Verify the updated link works correctly

### Reorganizing Categories

1. Move project entries between sections as needed
2. Update the index section if adding new categories
3. Ensure internal links in the index section match category headers
4. Run full validation suite

### Repository Structure Reference

```text
.
├── README.md           # Main curated list of P2P projects
├── LICENSE            # GNU GPLv3 license
└── .github/
    └── copilot-instructions.md  # This file
```

### README.md Structure

The README.md follows this organization:

- Header with description and license info
- Index section with category links
- Category sections:
  - Web
  - Communication  
  - Platforms & Frameworks
  - Finance
  - Data Transfer & Streaming
  - Storage
  - In Progress..

### Key Commands Reference

```bash
# Validate markdown formatting
markdownlint README.md

# Check all links (NEVER CANCEL - takes 60-120 seconds)
markdown-link-check README.md

# View current markdown linting issues
markdownlint README.md --output

# Install validation tools if missing
npm install -g markdownlint-cli markdown-link-check
```

### Working with Categories

Each category section follows this pattern:

- Section header (e.g., `### Web`)
- Bulleted list of projects
- Each project: `* [**ProjectName**](URL)` followed by description
- Blank line before next category

### Link Formatting Requirements

- Use `[**ProjectName**](URL)` format for all project links
- Include project description on the line immediately following the link
- Avoid bare URLs (markdownlint will flag these)
- Ensure URLs are complete and valid

### Troubleshooting

- If markdownlint reports line length issues, break long descriptions across
  multiple lines
- If markdownlint reports multiple blank lines, reduce to single blank line
  between sections
- Link checker may report false positives due to network restrictions -
  manually verify questionable links
- GitHub repository links are generally reliable for validation purposes
