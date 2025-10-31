# GitHub Pages Setup Instructions

This document explains how to enable GitHub Pages for the PrimitiveRoots repository.

## Automatic Deployment (Recommended)

The repository includes a GitHub Actions workflow (`.github/workflows/pages.yml`) that automatically deploys the site to GitHub Pages when changes are pushed to the main branch.

### Steps to Enable:

1. Go to your repository on GitHub: `https://github.com/BolongTang/PrimitiveRoots`

2. Click on **Settings** (top right of the repository page)

3. In the left sidebar, click on **Pages** (under "Code and automation")

4. Under "Build and deployment":
   - **Source**: Select "GitHub Actions"
   
5. Save the settings

6. Once this PR is merged to main, the workflow will automatically deploy the site

7. The site will be available at: `https://BolongTang.github.io/PrimitiveRoots/`

## Manual Deployment (Alternative)

If you prefer manual deployment without GitHub Actions:

1. Go to **Settings** > **Pages**

2. Under "Build and deployment":
   - **Source**: Select "Deploy from a branch"
   - **Branch**: Select `main` and folder `/ (root)`
   
3. Click **Save**

4. Wait a few minutes for GitHub to build and deploy the site

5. The site will be available at: `https://BolongTang.github.io/PrimitiveRoots/`

## Verifying the Deployment

After deployment, visit your GitHub Pages URL. You should see:
- A clean, professional web interface
- Form fields for Quotient, Modulus, Primitive Roots, and Search Cap
- Pre-filled example values (6, 7, 3 5, 3000)
- A "Calculate" button

## Using the Web Interface

The web interface provides the same functionality as running `python PrimitiveRoots.py` in a shell:

1. Enter your **Quotient** (e.g., 6)
2. Enter your **Modulus** (e.g., 7)
3. Enter **Primitive Roots** as space-separated numbers (e.g., 3 5)
4. Enter a **Search Cap** (e.g., 3000)
5. Click **Calculate**

The results will appear below the form, showing all valid root-power pairs.

## How It Works

The web interface uses [Pyodide](https://pyodide.org/), which runs Python code directly in the browser using WebAssembly. This means:
- No server-side processing required
- All computation happens in the user's browser
- The Python implementation is identical to `PrimitiveRoots.py`
- No installation or setup required for users

## Troubleshooting

### Page not loading
- Ensure GitHub Pages is enabled in repository settings
- Check that the workflow has completed successfully (Actions tab)
- Clear your browser cache and try again

### Python environment not loading
- The page requires internet access to load Pyodide from a CDN
- Check your browser console for any blocked resources
- Try a different browser or disable browser extensions that block CDN content

### No results appearing
- Increase the "Search Cap" value
- Verify the primitive roots are correct for your modulus
- Check browser console for any JavaScript errors

## Repository Structure

```
PrimitiveRoots/
├── .github/
│   └── workflows/
│       └── pages.yml          # GitHub Actions workflow
├── index.html                  # Web interface
├── PrimitiveRoots.py          # Original Python script
├── TestPrimitiveRoots.py      # Unit tests
├── README.md                   # Main documentation
├── SETUP.md                    # This file
└── sampleRun.txt              # Example shell run
```
