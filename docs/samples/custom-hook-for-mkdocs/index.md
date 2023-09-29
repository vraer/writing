---
title: Custom Hook for Page Link Queries by Tags
---

## Overview

This document outlines a custom Python script I developed for MkDocs. The script dynamically generates lists of page links based on tags defined in Markdown files. This functionality is particularly useful for large documentation projects that require efficient navigation.

!!! info "Check out the full python script on [GitHub](https://gist.github.com/vraer/d114b37932b855b66d6731c975342b0f)"

## Pre-Setup Requirements

- Python 3.x installed
- Familiarity with YAML and Markdown syntax

## Functionality

### Core Operations

The `page_links_by_tag.py` script performs four main tasks:

1. **Scan Files**: Utilizes the `glob` library to scan Markdown files in the `docs` directory.
2. **Read Content**: Reads the content of each Markdown file into a string.
3. **Identify Placeholders**: Searches for placeholder comments using regular expressions.
4. **Replace Placeholders**: Replaces found placeholders with corresponding page links based on tags.

### Usage Steps

1. Store `page_links_by_tag.py` in your MkDocs project root.
2. Insert placeholder comments like `<!-- TAGS=tag1, tag2 -->` in Markdown files.
3. Execute the script prior to building your MkDocs website.

## Example

Consider a Markdown file containing:

```markdown
<!-- TAGS=python, tutorial -->
```

Post-execution, the script replaces the placeholder with a list of links to pages tagged with `python` and `tutorial`.

## Use Case: Decision Records

### Context

Decision records document the rationale behind key project decisions. Automating the listing of these records can simplify navigation and improve team communication.

### Adaptation

In a Markdown file like `decision-records.md`, use:

```markdown
<!-- TAGS='role: dev', 'adopted' -->
```

The script replaces this placeholder with links to decision records carrying these tags.

### Advantages

- **Automatic Updates**: Eliminates the need for manual list updates.
- **Ease of Navigation**: Facilitates quicker access to relevant records.
- **Transparency**: Aids in tracking decisions and their current status.
