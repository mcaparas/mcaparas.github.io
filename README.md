# [mcaparas.github.io](https://mcaparas.github.io)

[![Netlify Status](https://api.netlify.com/api/v1/badges/7f3b3b7b-1b7e-4b7b-8b7b-1b7b7b7b7b7b/deploy-status)](https://app.netlify.com/sites/mcaparas/deploys)

A **Hugo-based** static portfolio website showcasing performances and scientific projects.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Running the Development Server](#running-the-development-server)
- [Adding New Content](#adding-new-content)
  - [Adding a Performance](#adding-a-performance)
  - [Adding a Science Project](#adding-a-science-project)
- [Internationalization (i18n)](#internationalization-i18n)
- [Building the Site](#building-the-site)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Prerequisites

This guide assumes you are using **macOS** as your development environment.

### Install Homebrew (if not installed)

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Required Software

1. **Hugo:**

   ```bash
   brew install hugo
   ```

2. **Node.js and Dependencies:**

   ```bash
   brew install npm
   npm install --save-dev postcss postcss-cli autoprefixer
   ```

## Installation

Clone the repository:

```bash
git clone https://github.com/mcaparas/mcaparas.github.io.git
cd mcaparas.github.io
git submodule add https://github.com/zetxek/adritian-free-hugo-theme.git themes/adritian-free-hugo-theme
git submodule update --init --recursive
```

## Running the Development Server

Start the Hugo development server:

```bash
hugo server -D
```

## Adding New Content

### Adding a Performance

To add a performance:

1. Navigate to `content/performance`.
2. Create a new Markdown file:

   ```markdown
   ---
   date: 'YYYY-MM-DDTHH:MM:SS+TIMEZONE'
   title: 'Performance Title'
   draft: false
   params:
     video: "VideoID"
     videoProvider: "youtube"  # or "vimeo"
   ---

   Description of the performance.
   ```

### Adding a Science Project

To add a science project:

1. Navigate to `content/science`.
2. Create a new Markdown file:

   ```markdown
   ---
   date: YYYY-MM-DDTHH:MM:SS+TIMEZONE
   draft: false
   title: "Project Title"
   jobTitle: "Job Title"
   company: "Company Name"
   location: "Location"
   duration: "Duration"
   ---

   ### Project Description

   Details about the project.
   ```

## Internationalization (i18n)

To update static text on the website:

1. Edit `i18n/en.yaml`.
2. Add or modify text strings:

   ```yaml
   example_key: "Your text here"
   ```

## Building the Site

Generate the static files:

```bash
hugo
```

The output will be in the `public` directory.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

This project uses the [Adritian Free Hugo Theme](https://github.com/adritian/adritian-free-hugo-theme) by Radity and Adrián Moreno Peña.
