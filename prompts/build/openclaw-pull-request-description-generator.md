---
title: "OpenClaw: Pull Request Description Generator"
slug: openclaw-pull-request-description-generator
stage: Build
category: "OpenClaw"
grade: B
score: 76
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/openclaw-pull-request-description-generator
---
# OpenClaw: Pull Request Description Generator

Pull Request Description Generator Generate a pull request description using the provided text.

## Prompt

# Pull Request Description Generator

Generate a pull request description using the provided text. Ensure output is formatted in raw Markdown suitable for direct copy and paste into GitHub.

## Steps
- Analyze the input text to identify key changes made in the pull request
- Summarize the main objectives including any relevant background information
- Include specific sections in Markdown format:

### Required Sections
- **Title**: Clear title summarizing the pull request
- **Description**: Detailed description of what was changed and why
- **Related Issues**: Reference any related issue numbers if applicable
- **Checklist**: A checklist of tasks that have been completed

## Output Format
Complete Markdown formatted string, ready for use in a GitHub pull request description. Use appropriate Markdown syntax for headers, lists, and links.

## Example Output
```markdown
## Add User Profile Image Upload

### Description
Implements image upload functionality for user profiles. Users can now
upload, crop, and save profile images directly from the settings page.

### Changes
- Added `ImageUpload` component with drag-and-drop support
- Integrated with S3 for image storage
- Added image processing pipeline (resize, compress, convert to WebP)

### Related Issues
Closes #142, Relates to #98

### Checklist
- [x] Image upload component
- [x] S3 integration
- [x] Image processing
- [x] Unit tests
- [x] Mobile responsive
```

## Tips

Generates structured PR descriptions in Markdown format. From DocsBot's technical prompts collection.
