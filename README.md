# Claude Code Excalidraw Skill

Claude Code skill to generates Excalidraw diagrams from `.claude/skills/`. This also works with OpenCode as well.

## Installation

Clone or download this repo, then copy it into your project's `.claude/skills/` directory:

```bash
git clone https://github.com/sandeepsriv/ai-claude-excalidraw-skill
cp -r excalidraw-diagram-skill .claude/skills/excalidraw-diagram
```

## Setup


**Ask your coding agent**

Ask your coding agent: *"Set up the Excalidraw skill by following the instructions in SKILL.md."*.

**You can also run**

```bash
cd .claude/skills/excalidraw-diagram/references
uv sync
uv run playwright install chromium
```

## Usage

Ask your coding agent to create a diagram:

*"Create an Excalidraw diagram showing how [your topic] works"*  
   
Example:
    
*"Create an Excalidraw diagram showing how Kafka Stream API works"*  
*"Create an Excalidraw diagram showing how Web Socket protocol works"*  
*"Create an Excalidraw diagram showing how the AG-UI protocol streams events from an AI agent to a frontend UI"*

## Outout

Output PNGs will be next to any .excalidraw file generated.

## Colors

Edit `references/color-palette.md` to match your likings.

## File Structure

```
excalidraw-diagram/
  SKILL.md                          # Design
  references/
    color-palette.md                # Colors
    element-templates.md            # Templates for each element type
    json-schema.md                  # Excalidraw JSON format reference
    render_excalidraw.py            # Render .excalidraw to PNG
    render_template.html            # Browser template for rendering
    pyproject.toml                  # Python dependencies (playwright)
```