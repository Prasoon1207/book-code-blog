# Book Code Blog

A minimalist blog for sharing code examples and implementations from various technical books, built with Jupyter notebooks.

## Overview

This project uses [Jupyter Book](https://jupyterbook.org/) to create an elegant, static website from Jupyter notebooks. Each notebook represents a chapter or concept from a book, with executable code, explanations, and visualizations.

## Features

- 📚 **Organized by Book/Chapter**: Clean structure for organizing code from different books
- 💻 **Interactive Code**: Executable Jupyter notebooks with live code examples
- 🎨 **Minimalist Design**: Clean, distraction-free reading experience
- 🚀 **Automatic Deployment**: GitHub Actions automatically builds and deploys to GitHub Pages
- 📱 **Responsive**: Works beautifully on all devices

## Quick Start

### Prerequisites

- Python 3.8 or higher
- pip or conda

### Installation

1. Clone the repository:
```bash
git clone <your-repo-url>
cd book-code-blog
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

### Local Development

Build and preview the blog locally:

```bash
jupyter-book build .
```

Open `_build/html/index.html` in your browser to view the site.

For live development with auto-rebuild:
```bash
jupyter-book build . --builder html
```

### Adding New Content

1. Create a new Jupyter notebook in the `notebooks/` directory
2. Follow the naming convention: `book-name_chapter-number_topic.ipynb`
3. Update `_toc.yml` to include your new notebook
4. Build and test locally

Example notebook structure:
```
notebooks/
├── deep-learning_01_introduction.ipynb
├── deep-learning_02_neural-networks.ipynb
└── algorithms_01_sorting.ipynb
```

## Project Structure

```
book-code-blog/
├── README.md              # This file
├── _config.yml           # Jupyter Book configuration
├── _toc.yml             # Table of contents
├── requirements.txt      # Python dependencies
├── notebooks/           # Your Jupyter notebooks
│   └── example_chapter.ipynb
├── assets/              # Images, CSS, and other assets
└── .github/
    └── workflows/
        └── deploy.yml   # GitHub Actions for deployment
```

## Deployment

This blog automatically deploys to GitHub Pages when you push to the `main` branch.

### Manual Deployment

```bash
# Build the book
jupyter-book build .

# Deploy using ghp-import
ghp-import -n -p -f _build/html
```

## Configuration

Edit `_config.yml` to customize:
- Site title and author
- Theme and styling
- Navigation options
- Analytics (optional)

Edit `_toc.yml` to organize your content structure.

## Writing Tips

- Use markdown cells for explanations and theory
- Include code cells for practical implementations
- Add visualizations using matplotlib, seaborn, or plotly
- Reference the source book at the top of each notebook
- Keep notebooks focused on a single concept or chapter

## Contributing

Feel free to open issues or submit pull requests for improvements!

## License

MIT License - Feel free to use this template for your own book code blog.

## Resources

- [Jupyter Book Documentation](https://jupyterbook.org/)
- [Markdown Guide](https://www.markdownguide.org/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
