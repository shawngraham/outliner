# Note Cards Outliner - User Guide

## No Configuration Required!

This tool lets you organize markdown files visually as note cards on a canvas. Simply load your files and start organizing - no code editing needed.

## Quick Start

1. **Load Your Files**: Click the "Load Files" button and select one or more `.md` or `.markdown` files
2. **Organize**: Each file becomes a card - drag them around, create connections between related ideas
3. **Edit**: Double-click cards to edit their content
4. **Export**: Click "Export to Markdown" to download an ordered outline based on your connections

## How It Works

### Loading Files
- Click "Load Files" button (top of screen)
- Select multiple markdown files from your computer
- Each file becomes one card on the canvas
- Files are saved in your browser - they'll be there when you return

### File Format

The app supports **two markdown file formats** and automatically detects which one you're using:

#### Format 1: One File = One Card

```markdown
# My Card Title
This is the content of the card.

You can use markdown formatting:
- Bullet points
- **Bold text**
- Multiple paragraphs

Everything in this file becomes one card.
```

#### Format 2: One File = Multiple Cards

Use `#-------` as a separator to create multiple cards from a single file:

```markdown
# First Card
Content for the first card...

#-------

# Second Card
Content for the second card...

#-------

# Third Card
Content for the third card...
```

**Both formats work!** The app detects the presence of `#-------` separators and parses accordingly.

- **First heading** (line starting with `#`) becomes the card title
- **Rest of content** (or section) becomes the card content
- **No heading?** The filename (without .md) is used as the title

### Working with Cards
- **Position cards**: Drag them anywhere on the canvas
- **Pan the canvas**: Drag empty space to move around
- **Create new cards**: Double-click empty space
- **Edit cards**: Double-click a card to edit title and content
- **Expand/collapse**: Click card header to show/hide content
- **Connect cards**: Drag from one card onto another to create a connection arrow
- **Delete connections**: Double-click a connection line to remove it
6. **Export to Markdown**: Generates an ordered outline following your connection structure

### Export Functionality
The export feature creates a single markdown file that captures your outline structure **following your connections**:

**How Export Ordering Works:**
1. Finds the **topmost card** on the canvas (highest position - starting point)
2. **Follows connection arrows** from that card to determine the sequence
3. **Only exports connected cards** - unconnected cards are excluded
4. If multiple cards connect from one card, they're exported in top-to-bottom order
5. Formats titles as `[Title]` in markdown link format
6. Separates cards with `---` dividers
7. Downloads as `outline-export.md`

**Important:** Only cards that are part of a connected path starting from the topmost card will be exported. This lets you work on multiple outlines simultaneously - only export the connected path you're ready to write.

**Example Export:**
```markdown
[Introduction]

This is the intro content...

---

[Main Argument]

Following the connection from intro...

---

[Conclusion]

Final thoughts...
```

This creates a linear document that reflects the logical flow you've established through connections on the canvas.

### Buttons

- **Load Files**: Select markdown files from your computer to load as cards
- **Export to Markdown**: Download your organized outline as a single markdown file
- **Reset Canvas**: Clear all cards and connections, start fresh

### Data Persistence

Your work is automatically saved in your browser:
- **Loaded files**: Saved so they're available next time
- **Card positions**: Remember where you placed each card
- **Connections**: All arrows between cards are saved
- **Edits**: Changes to titles and content are saved
- **Canvas position**: Your pan/zoom state is saved

Everything persists between sessions until you click "Reset Canvas" or clear browser data.

## Use Cases

- **Essay planning**: Load your research notes, organize them, create an outline
- **Chapter organization**: Arrange sections of a longer work
- **Lecture notes**: Organize notes from different sources into a coherent structure
- **Research synthesis**: Connect ideas from multiple papers or sources
- **Content strategy**: Plan blog posts, articles, or documentation
- **Study guides**: Organize topics and create connections between concepts

## Tips for Best Results

### File Organization
- Break your content into focused, single-topic files
- Use descriptive filenames (they're used as fallback titles)
- Start with 4-10 files for manageable organization
- You can always create more cards by double-clicking the canvas

### Visual Organization
- **Position matters**: Place your starting point at the top of the canvas
- **Use connections**: Draw arrows to show the flow - ONLY connected cards are exported!
- **Create a complete path**: Connect all cards you want in your export
- **Multiple outlines**: You can have unconnected groups - only the path from the top card exports
- **Branch and merge**: Multiple cards can connect to one (converging ideas)

### Export Workflow
1. Organize your cards visually
2. **Connect all cards** you want in the export (starting from the topmost)
3. Leave unconnected any cards you're not ready to include
4. Click "Export to Markdown"
5. Review the exported file
6. Adjust connections if needed
7. Export again

The exported markdown is ready to expand into a full document or can be further edited in any text editor.

## Technical Notes

- **Browser compatibility**: Works in all modern browsers (Chrome, Firefox, Safari, Edge)
- **No internet required**: After initial load, works completely offline
- **Privacy**: All data stays in your browser - nothing is sent to any server
- **File size**: Can handle hundreds of cards, though 10-30 is optimal for usability
- **Export format**: Standard markdown that works with any markdown editor



