# SEAL's TPRO Training Program Website

[Link to the original Google Doc](https://docs.google.com/document/d/1BiK__w_-F3xfQgRa23Kx10FHiZPz8gGIw98JXF5dyig/edit?tab=t.0)

This website was created from a downloaded version of the initial Google Doc and then pruned into separate HTML and CSS files. 

The primary purpose of the website is to help with the new member onboarding process, allowing members with questions to paste the link to this website into ChatGPT and ask their questions there, with ChatGPT serving as an expert on the training program contents.

## Website Structure

```
tpro-website/
├── index.html           # Main HTML file
├── styles.css           # Main stylesheet
├── list-styles.css      # List-specific styles
├── class_mapping.json   # CSS class name mappings
└── README.md
```

## Requesting Changes

1. **Highlight Specific Changes**: Either within the main TPRO document or within a new document,
   - Use the comment feature within Google Docs to mark specific changes, with the new change being highlighted in the Google Doc and the old text in the comment box
   - Make sure to note the specific section within the original document that has the changes for easy navigaton when editing the HTML code

2. **Preserve Structure**: 
   - Maintain the existing HTML structure and class names
   - Don't modify CSS classes unless absolutely necessary
   - Keep the anchor tag structure intact for navigation

## Editing the Website

#### 1. Use Search/Find (Ctrl+F / Cmd+F)
- **Always use your editor's search function** to navigate to specific sections easily
- Search for section titles, unique IDs, or specific text content
- Consider adding HTML comments in the code where changes have been made: `<!-- Updated: [date] - [description] -->`


#### 2. Section Identification
- **Table of Contents**: Search for `id="table-of-contents"`
- **Section Headings**: Search for the section title or its slug-based ID
  - Example: Search for `"Part I - SEAL Life"` or `id="part-i-seal-life-onboarding"`
- **Anchor Tags**: All table of contents links use title-based slugs (e.g., `#instructions-on-using-kanban-boards`)

#### 3. Common Edit Locations
- **Table of Contents**: Lines ~33-1033 (search for `id="table-of-contents"`)
- **Main Content**: Starts around line 1055
- **Styles**: Edit `styles.css` for general styling, `list-styles.css` for list-specific styles

#### 4. Testing Your Changes
- Open `index.html` in a browser to preview changes
- Test navigation links (especially table of contents links)
- Verify list formatting still works correctly

## Deployment

### GitHub Pages Setup

The website is deployed via **GitHub Pages** from the repository:
- **Repository**: `SEAL-Web-Team/tpro-website`
- **URL**: `https://seal-web-team.github.io/tpro-website/`

### Deployment Process

1. **Make Your Changes**
   - Edit files locally
   - Test changes in browser using Live Server
   - **To access Live Server:** 
      1. ensure that the Live Server extension is downloaded in your IDE
      2. double click anywhere in your HTML file
      3. click "Open with Live Server", the local version of your files will open in your browser

2. **Automatic Deployment**
   - GitHub Pages automatically deploys from the `main` branch
   - Changes typically go live within 1-2 minutes
   - Check the repository's "Actions" tab for deployment status

## Maintenance

### Adding New Sections

1. Add the section heading with a proper ID:
   ```html
   <h2 id="new-section-title">New Section Title</h2>
   ```

2. Add corresponding entry into the table of contents:
   ```html
   <a href="#new-section-title">X.X. New Section Title</a>
   ```

3. The ID will automatically be converted to a slug format (lowercase, hyphens)

### Troubleshooting

- **Lists not formatting correctly**: Check that `list-styles.css` contains the necessary classes
- **Links not working**: Verify anchor IDs match between table of contents links and section headings
- **Styling issues**: Check browser console for missing CSS classes

## Notes

- The website is designed to be ChatGPT-friendly for Q&A purposes
- All content should remain accessible, well-structured, and reflect the changes within the actual Training Program document
- Keep the table of contents updated if/when adding new sections
- Page numbers have been removed from the table of contents for cleaner presentation
