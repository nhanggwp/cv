# CV - Nguyen Trung Nhan

My professional CV built with LaTeX.

## 📋 Features

- **Automatic PDF Compilation**: GitHub Actions automatically compiles the LaTeX file to PDF on every push
- **PDF Artifacts**: Download compiled PDF from GitHub Actions
- **Release Support**: Create releases with PDF attached by tagging commits

## 🚀 Usage

### Local Compilation
```bash
pdflatex cv.tex
```

### GitHub Actions (Automatic)
1. Push changes to `main` or `master` branch
2. GitHub Actions will automatically:
   - Compile `cv.tex` to `cv.pdf`
   - Store PDF as artifact (available for 30 days)
   
### Create Release with PDF
```bash
git tag v1.0.0
git push origin v1.0.0
```

GitHub Actions will automatically create a release with the compiled PDF attached.

## 📁 Project Structure
```
.
├── cv.tex                          # LaTeX source file
├── .github/
│   └── workflows/
│       └── compile-cv.yml          # GitHub Actions workflow
├── .gitignore                      # Git ignore rules
└── README.md                       # This file
```

## 🔧 Requirements

- GitHub repository
- LaTeX packages (xcolor, tikz, fontawesome5, etc.)
- GitHub Actions enabled

## 📝 Notes

- The workflow is triggered on push to `main`/`master` branches
- Only recompiles when `cv.tex` or workflow file changes
- PDF is automatically generated and available for download
