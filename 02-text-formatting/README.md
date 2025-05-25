# Text Formatting 📝

Learn how to structure and format text content in HTML, from basic headings to complex lists.

## Topics Covered

### 1. Headings (h1-h6)
- Hierarchy and semantic meaning
- SEO implications
- Best practices for heading structure

### 2. Paragraphs and Text Elements
- Paragraphs, line breaks, and horizontal rules
- Inline text formatting (bold, italic, underline)
- Semantic vs presentational elements

### 3. Lists
- Ordered lists (numbered)
- Unordered lists (bulleted)
- Description lists (definition lists)
- Nested lists

## Files in This Section

- **[headings.html](./headings.html)** - Working with HTML headings
- **[paragraphs-and-text.html](./paragraphs-and-text.html)** - Text formatting elements
- **[lists.html](./lists.html)** - Creating and styling lists

## Key Concepts

### Semantic vs Presentational
HTML should describe the **meaning** of content, not just its appearance:
- ✅ `<strong>` for important text
- ❌ `<b>` for bold styling (use CSS instead)
- ✅ `<em>` for emphasized text
- ❌ `<i>` for italic styling (use CSS instead)

### Heading Hierarchy
Proper heading structure helps with:
- **Accessibility**: Screen readers use headings for navigation
- **SEO**: Search engines use headings to understand content structure
- **Maintenance**: Logical document outline makes editing easier

### White Space Handling
HTML collapses multiple spaces and line breaks into single spaces. Use appropriate elements for spacing:
- `<p>` for paragraphs
- `<br>` for line breaks
- CSS for precise spacing control

## Common Mistakes

1. **Skipping heading levels** - Don't jump from h1 to h3
2. **Using headings for styling** - Use headings for structure, CSS for appearance
3. **Multiple h1 elements** - Typically use only one h1 per page
4. **Overusing line breaks** - Use paragraphs instead of multiple `<br>` tags

## Next Steps

After mastering text formatting, proceed to [Links and Media](../03-links-and-media/) to learn about hyperlinks and multimedia content.
