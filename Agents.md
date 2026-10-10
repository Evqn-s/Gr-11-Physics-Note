```
# Environment Context: Obsidian Vault

You are operating directly within an **Obsidian Vault** (a local directory of Markdown files). Every task you perform, file you read, or file you modify must conform to Obsidian syntax and knowledge management conventions.

## 1. Internal Linking & Architecture
- **Use WikiLinks:** Always link to other internal notes using double square brackets: `[[Note Title]]` or `[[Note Title|Custom Display Text]]`. Never use standard Markdown relative URLs like `[Note Title](./Note%20Title.md)`.
- **Atomic Notes:** Prefer creating small, topic-focused notes rather than giant monolithic files. Link concepts together as you discover connections.
- **Uncreated Notes:** It is acceptable to link to concepts that do not have dedicated notes yet using `[[Future Concept]]` if it represents a distinct topic worth creating later.

## 2. File Metadata & Frontmatter
- **YAML Frontmatter:** Every new note created must begin with valid YAML frontmatter between `---` fences at the top of the file:
  ```yaml
  ---
  created: YYYY-MM-DD
  tags:
    - topic/subtopic
  aliases: []
  ---
```

- **Preserve Existing Metadata:** When updating existing notes, never delete or overwrite existing frontmatter fields unless explicitly instructed. Append new tags or aliases cleanly.
    

## 3. Formatting Rules

- **Math & LaTeX:** Render inline math using by enclosing latex inside two dollar signs

- **Embedded Media & Attachments:** Use Obsidian embed syntax `![[Image Name.png]]` for local attachments.
    
- **Callouts:** Use Obsidian callout syntax for key takeaways, warnings, or definitions:
    
    > [!info] Key Takeaway
    > 
    > Highlight important rules or principles here.
    

## 4. Editing Principles

- **Non-Destructive Refactoring:** When editing existing notes, preserve existing user commentary, formatting styles, and custom plugin syntax (e.g., Dataview queries, Kanban boards, or tasks).
    
- **Structure:** Organize long notes with hierarchical headers (`##`, `###`), bold terms for readability, and concise bullet points.
## 5 . Tags
Markdown

````
## Tagging Taxonomy & Metadata Rules

Every new or updated note in this vault must contain valid YAML frontmatter between `---` fences at the top of the file. Use the exact nested tags below based on the note type and subject content:

### Frontmatter Structure
```yaml
---
type: roadmap | video-directory | teaching-guide | summary-note
subject: 1 | 2 | 3 | 4
tags:
  - SPH3U/tag-name
---
````

### Required Tag Assignment Matrix

1. **Master Roadmap File:**
    
    - Tag: `tags: [SPH3U/roadmap]`
        
2. **Video Directory File:**
    
    - Tag: `tags: [SPH3U/videos]`
        
3. **Deep-Dive Teaching Guides:**
    
    - Subject 1 (Math Foundations & Measurement): `tags: [SPH3U/intro-skills/math]`
        
    - Subject 2 (1D Vectors & Motion Foundations): `tags: [SPH3U/kinematics/vectors]`
        
    - Subject 3 (Motion Graphs & Transition Graphs): `tags: [SPH3U/kinematics/graphs]`
        
    - Subject 4 (Kinematic Equations & Advanced Kinematics): `tags: [SPH3U/kinematics/equations]`
        
4. **1-Page Summary Notes:**
    
    - Tag: `tags: [SPH3U/summary]`