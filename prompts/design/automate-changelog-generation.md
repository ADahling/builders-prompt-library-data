---
title: "Automate Changelog Generation"
slug: automate-changelog-generation
stage: Design
category: "Documentation"
grade: C
score: 65
difficulty: Intermediate
hand_reviewed: false
url: https://buildersprompt.com/prompts/automate-changelog-generation
---
# Automate Changelog Generation

Get a script that generates a changelog from a project's Git commit messages, grouping entries as Added, Changed, Deprecated, Removed, and Fixed.

Variables: project_name, repository_url

## Prompt

Develop a script that automatically generates a changelog for {{project_name}} based on commit messages. The changelog should categorize changes into 'Added', 'Changed', 'Deprecated', 'Removed', and 'Fixed'. Use {{repository_url}} for the git repository.

## Tips

Ensure the script filters commits based on specified tags.
