# Note Cards Outliner - Setup Instructions

## Using with Markdown Files (One File = One Card)

### Concept
Each markdown file you configure becomes ONE card on the canvas. This is perfect for organizing different topics, chapters, or concepts as individual cards that you can then arrange and connect visually.

### File Structure
Place all your markdown files in the same folder as the HTML file:
```
your-folder/
├── note-cards-canvas.html
├── notes-intro.md
├── notes-chapter1.md
├── notes-chapter2.md
└── notes.md
```

### Configuration
Edit the `MARKDOWN_FILES` array in the HTML file to list your markdown files:

```javascript
const MARKDOWN_FILES = [
    { name: 'Introduction', file: 'notes-intro.md' },
    { name: 'Chapter 1', file: 'notes-chapter1.md' },
    { name: 'Chapter 2', file: 'notes-chapter2.md' },
    { name: 'Example Notes', file: 'notes.md' }
];
```

- **name**: Display name for the card (used as fallback title if no heading in file)
- **file**: Actual filename (must be in same folder)

### Markdown File Format
Each file represents one card. The first `#` heading becomes the card title, and the rest is the content:

```markdown
# My Card Title
This is the content of the card.

You can use markdown formatting:
- Bullet points
- **Bold text**
- Multiple paragraphs

Everything in this file becomes the content of one card.
```

If no heading is present, the `name` from the configuration is used as the title.

### How It Works
1. **Initial Load**: Each markdown file is loaded as one card on the canvas
2. **Auto-Save**: All changes (positions, edits, connections) are saved to localStorage
3. **Subsequent Loads**: Your edited state is restored automatically
4. **Reload from Files**: Button resets all cards to their original markdown file content
5. **Reset Canvas**: Button clears everything and reloads from files

### Use Cases
- **Course chapters**: Each chapter as a separate card
- **Topic overview**: Different topics as individual cards students can arrange
- **Concept mapping**: Pre-loaded concepts that students connect and organize
- **Essay outline**: Different sections (intro, body, conclusion) as cards to arrange

### Adding or Removing Cards
To add a new card:
1. Create a new `.md` file in the folder
2. Add it to the `MARKDOWN_FILES` array
3. Reload the page

To remove a card:
1. Remove it from the `MARKDOWN_FILES` array
2. Reload the page

### For Your Course Website
1. Upload the HTML and all markdown files to the same directory
2. Students load the page and see all configured cards
3. Students can rearrange, connect, and edit cards
4. Their work persists in their browser between sessions
5. They can reset to start fresh anytime

### Testing Locally
Due to browser security (CORS), testing locally requires a web server:

```bash
# Using Python
python -m http.server 8000

# Then visit
http://localhost:8000/note-cards-canvas.html
```

### Tips
- Keep markdown files focused and concise for better card readability
- Use descriptive filenames
- Start with 4-8 cards for best user experience
- Students can always create additional cards by double-clicking the canvas


