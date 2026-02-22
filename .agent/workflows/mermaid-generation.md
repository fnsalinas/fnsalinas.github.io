---
description: Generate and export Mermaid.js diagrams
---

# Mermaid Diagram Generation Workflow

1.  **Understand Requirements**:
    - Identify the type of diagram needed (Flowchart, Sequence, Class, etc.).
    - Identify the key components, actors, and relationships.

2.  **Draft Mermaid Code**:
    - Use the `mermaid-expert` agent.
    - Write the Mermaid syntax inside a markdown code block.
    - **Validation**: Check against `mermaid-mastery` syntax guides.

3.  **Execute & Export (MANDATORY)**:
    - You MUST generate an image file for the diagram.
    - Write the code to a `.mmd` file.
    - Command: `npx -y @mermaid-js/mermaid-cli -i input.mmd -o output.png -b transparent`
    - Ensure the `.mmd` file is saved locally first.

4.  **Review & Embed**:
    - Embed the generated `.png` image into your markdown response or document using a **relative path** (e.g., `![Diagram](output.png)`).
    - NEVER leave the raw mermaid code block in the final markdown document; always replace it with the image.

## Example
```bash
# Save code
echo "graph TD; A-->B;" > diagram.mmd
# Convert
npx -y @mermaid-js/mermaid-cli -i diagram.mmd -o diagram.png -b transparent
# In Markdown
![Diagram](diagram.png)
```
