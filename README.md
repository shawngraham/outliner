# Note Cards Outliner - Setup Instructions

## Using with Multiple Markdown Files

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
Edit the `MARKDOWN_FILES` array in the HTML file to list your files:

```javascript
const MARKDOWN_FILES = [
    { name: 'Introduction', file: 'notes-intro.md' },
    { name: 'Chapter 1', file: 'notes-chapter1.md' },
    { name: 'Chapter 2', file: 'notes-chapter2.md' },
    { name: 'Example Notes', file: 'notes.md' }
];
```

- **name**: Display name shown in the dropdown
- **file**: Actual filename (must be in same folder)

### Markdown Format
Separate each note card with `#-------` on its own line:

```markdown
# Card Title
Card content goes here.
You can use multiple lines.
#-------
# Another Card
More content for the second card.
#-------
# Third Card
And so on...
```

### How It Works
1. **File Selection**: Use the dropdown at the top to switch between files
2. **Separate Storage**: Each file has its own localStorage - work is saved independently
3. **Auto-Save**: Changes are automatically saved as you work
4. **File Switching**: Switching files prompts you that your work is saved
5. **Reload**: "Reload from File" resets the current file to original markdown
6. **Reset**: "Reset Canvas" clears all work for the current file

### Use Cases for Multiple Files
- **Different lessons/chapters** in a course
- **Multiple assignments** or projects
- **Various topics** students can explore
- **Progressive complexity** - start simple, advance to complex

### For Your Course Website
When hosted on a web server:
1. Upload the HTML and all markdown files to the same directory
2. Students can switch between different topics/chapters using the dropdown
3. Their work on each file is saved separately in their browser
4. Perfect for courses with multiple modules or topics

### Testing Locally
To test with markdown files:
1. Save HTML and markdown files in the same folder
2. Open `note-cards-canvas.html` in a web browser (or use local server)
3. Use dropdown to switch between files
4. Each file loads independently with its own saved state

### CORS Note
If loading from file:// URLs locally, you may need to use a local web server due to browser security restrictions. Python's built-in server works well:
```bash
python -m http.server 8000
```
Then visit: http://localhost:8000/note-cards-canvas.html

