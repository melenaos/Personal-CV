Personal CV Template
====================

A developer-centric CV builder that uses **Markdown** for content and **CSS** for styling. This project converts your professional history into a clean, print-ready PDF using md-to-pdf.

Quick Start
--------------

1. Clone this project and download locally

2. `npm run build`
    

How It Works
---------------

This project separates your **content** from your **design**:

*   **resume.md**: Update this file with your experience and skills.
    
*   **style.css**: This controls the layout (colors, fonts, margins).
    
*   **package.json**: Contains the build scripts to generate the PDF.
    

### Real-time Preview (Watch Mode)

While editing your Markdown or CSS, you can run:

`npm run watch`

The PDF will automatically regenerate every time you save your changes.

Choosing a Style
-------------------

The project includes several pre-defined "flavors" of design. To switch styles, simply rename one of the flavor files to style.css:


**To apply a style:**

```
cp style.executive.css style.css
npm run build
```

Project Structure
--------------------

Plaintext

```
├── resume.md           # Your CV content
├── package.json        # Build scripts and dependencies
├── resume.pdf          # The generated output (ignored by git)
├── style.css           # The active stylesheet used for builds
├── style.executive.css # Alternative flavor: Professional Navy
├── style.delta.css     # Alternative flavor: Professional minimalistic
...
└── style.studio.css    # Alternative flavor: Bold and colorful

```

Tips for a Better CV
-----------------------

### PDF Page Breaks

If you need to force a page break in your CV, insert this HTML tag into your resume.md:

HTML

`<div class="page-break"></div>`

### Adjusting Margins

If your content is slightly too long for one page, open your style.css and adjust the @page margin or the line-height:

```
@page {
  margin: 15mm; /* Reduce this to 10mm to fit more content */
}

body {
  line-height: 1.4; /* Tighten line spacing */
}
```

### Publishing to GitHub Pages

You can host your PDF online so that recruiters can access it via a direct link (e.g., https://yourname.github.io/cv/resume.pdf).
1. Configure GitHub Settings

   - Push your code to GitHub.

   - Go to your repository Settings tab.

   - On the left sidebar, click Pages.

   - Under Build and deployment > Branch, select:

        - Branch: main (or master)

        - Folder: /docs

    - Click Save.

2. Update and Sync

    Whenever you make changes to your CV, run:

    `npm run build`

    and commit to GitHub

Your live PDF link will update automatically within a few minutes.

Requirements
---------------

*   [Node.js](https://nodejs.org/) (Version 16 or higher recommended)
    
*   NPM (comes with Node)