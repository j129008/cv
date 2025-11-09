# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a personal CV/resume repository containing bilingual (Chinese/English) HTML-based resumes with shared CSS styling. The project generates both web viewable HTML files and PDFs for distribution.

## File Structure

### Resume Files
- **Chinese versions**: `cv_tw.html`, `cv_tw_google.html`
- **English versions**: `cv_en.html`, `en_ver.html`, `en_eda_ver.html`
- **PDFs**: Pre-generated PDF versions with `.pdf` extension
- **Styling**: `style.css` - shared stylesheet for all resume versions

### Resume Variants
- `cv_tw.html` / `cv_en.html`: Standard resume versions
- `cv_tw_google.html`: Google-specific version with condensed summary and modified skills section
- `en_eda_ver.html`: EDA (Electronics Design Automation) focused version
- `en_ver.html`: Alternative English version with different formatting

## Architecture

### HTML Structure
All resume files follow a consistent Bootstrap 4-based layout:
- **Header section**: Name, title, contact info, education
- **Summary section**: Key highlights and achievements
- **Experience section**: Chronological work history with period subsections
- **Skills section**: Categorized technical skills

### Styling System
The `style.css` file uses a component-based approach with:
- Semantic class naming (`.header-section`, `.experience-content`, `.skill-category`)
- Responsive design with mobile breakpoints at 768px
- Print-optimized styles for PDF generation
- Color scheme: Primary blue (#0d47a1) for headers and highlights
- Typography: Microsoft JhengHei for Chinese, sans-serif fallback

### CSS Class Patterns
- `.section-title`: Main section headers with bottom border
- `.experience-highlight`: Blue background-highlighted important text
- `.experience-tech`: Gray technical stack tags
- `.skill-category`: Flexbox-based skill groupings

## Development Guidelines

### Editing Resumes
When updating resume content:
1. Maintain consistent HTML structure across all versions
2. Use existing CSS classes rather than inline styles
3. Keep Chinese and English versions synchronized in structure
4. Update both HTML and PDF versions when making changes

### Generating PDFs
PDF versions are generated from HTML files. When updating:
1. Open the HTML file in a browser
2. Use browser print function with appropriate settings
3. Save as PDF with matching filename (e.g., `cv_tw.html` → `cv_tw.html.pdf`)

### Version Control
According to `.cursorrules`:
- Commit messages should be in Chinese (zh-TW)
- Documentation and comments should be in Chinese
- Follow HTML, CSS, and JavaScript style guides

### Common Updates
- **Work experience**: Add new entries in `.experience-content` blocks
- **Skills**: Update `.skill-category` sections with new technologies
- **Styling**: Modify `style.css` to affect all resume versions simultaneously

## Important Notes

### Bilingual Consistency
When making content changes, ensure both Chinese and English versions reflect the same information:
- Work dates and company names must match
- Skills sections should list equivalent technologies
- Achievements should be translated, not omitted

### Bootstrap Dependencies
All HTML files use Bootstrap 4.3.1 from CDN:
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.3.1/dist/css/bootstrap.min.css">
```
Changes to layout should respect Bootstrap's grid system.

### Recent Changes Pattern
Based on git history, common updates include:
- Adjusting work experience dates (e.g., Riversoft date corrections)
- Removing/adding specific project details to emphasize different skills
- Refining skills section to highlight most relevant technologies

### File Encoding
All HTML files use UTF-8 encoding with appropriate meta tags for Chinese character support.
