# MaskFeat Training Analysis - GitHub Pages Deployment

This repository contains interactive visualizations of MaskFeat model training performance across different configurations.

## 🌐 Live Demo

Please visit:
```
[https://musicamatics.github.io/maskfeat-analysis/]
```

## 📁 Files Included

### HTML Pages
- `index.html` - Main dashboard landing page
- `1_old_run_20warmup_bs128_interactive.html` - Chart 1: Old run baseline
- `2_old_run_20warmup_bs128_extended_ep100_interactive.html` - Chart 2: Old run extended to epoch 100
- `3_new_run_5warmup_bs512_interactive.html` - Chart 3: New optimized run
- `4_comparison_old_vs_new_runs_interactive.html` - Chart 4: Side-by-side comparison

### High-Resolution Exports
- PNG files (2800×1800 pixels) for all 4 charts
- SVG files (vector graphics) for all 4 charts
- Embed HTML files for integrating charts into other websites

### Python Scripts
- `training-validation-chart.py` - Generates Chart 1
- `training_validation_chart_updated.py` - Generates Chart 2
- `training_validation_chart_5epoch.py` - Generates Chart 3
- `training_validation_chart_comparison.py` - Generates Chart 4

## 🚀 Quick Deployment to GitHub Pages

### Step 1: Create a New GitHub Repository

1. Go to https://github.com/new
2. Create a new repository (e.g., `maskfeat-analysis`)
3. Make it **public** (required for free GitHub Pages)
4. Don't initialize with README (we'll push existing files)

### Step 2: Initialize Git and Push Files

```bash
cd /Users/matthew/Downloads/MaskFeat

# Initialize git repository
git init

# Add all necessary files
git add index.html
git add *_interactive.html
git add *.png
git add *.svg
git add *_embed.html
git add *.py
git add README.md

# Create first commit
git commit -m "Initial commit: MaskFeat training analysis dashboard"

# Add your GitHub repository as remote (replace with your URL)
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top menu)
3. Scroll down to **Pages** (left sidebar)
4. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click **Save**
6. Wait 1-2 minutes for deployment

Your site will be live at: `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`

## 🎯 Alternative: Using GitHub Desktop (No Command Line)

1. Download [GitHub Desktop](https://desktop.github.com/)
2. Create a new repository in GitHub Desktop
3. Copy all HTML, PNG, SVG files to the repository folder
4. Commit changes in GitHub Desktop
5. Click "Publish repository" to push to GitHub
6. Follow Step 3 above to enable GitHub Pages

## 📊 What's Included in the Dashboard

### Chart 1: Old Run (Baseline)
- Configuration: 20 warmup epochs, batch size 128
- Data through epoch 75
- Mean gap: 1.15%

### Chart 2: Old Run Extended
- Same configuration extended to epoch 100
- Complete training trajectory
- Mean gap: 3.78%

### Chart 3: New Run (Optimized)
- Configuration: 5 warmup epochs, batch size 512
- Improved generalization performance
- Mean gap: 1.24%

### Chart 4: Side-by-Side Comparison
- Direct comparison of old vs new configurations
- Color-coded traces for easy distinction
- Configuration details in top-right boxes

## 🎨 Features

- **Interactive Charts**: Hover for exact values, zoom, pan, and toggle traces
- **Responsive Design**: Works on desktop, tablet, and mobile
- **High-Resolution Exports**: Download PNG (2800×1800) or SVG versions
- **Embed Code**: Use provided HTML divs to embed charts elsewhere
- **Legend Groups**: Click legend items to show/hide related projections

## 🔧 Regenerating Charts

If you need to update the data and regenerate the charts:

```bash
# Activate virtual environment
source venv/bin/activate

# Run individual scripts
python training-validation-chart.py
python training_validation_chart_updated.py
python training_validation_chart_5epoch.py
python training_validation_chart_comparison.py

# Commit and push updates
git add *.html *.png *.svg
git commit -m "Update charts with new data"
git push
```

Changes will appear on GitHub Pages within 1-2 minutes.

## 📦 Dependencies

The Python scripts require:
- Python 3.13+
- plotly 6.4.0
- numpy 2.3.4
- kaleido 1.2.0

Install with:
```bash
python -m venv venv
source venv/bin/activate
pip install plotly numpy kaleido
```

## 📝 Customization

### Updating the Landing Page

Edit `index.html` to customize:
- Header text and styling
- Introduction text
- Chart descriptions
- Color scheme (CSS variables in `<style>` section)

### Chart Settings

Each Python script has configurable parameters:
- Image dimensions: `width=1400, height=900`
- Export scale: `scale=2` (for high-res output)
- Colors, fonts, legend position
- Projection bands and labels

## 🌟 Tips

1. **Custom Domain**: In GitHub Pages settings, you can add a custom domain
2. **Analytics**: Add Google Analytics by inserting tracking code in `index.html`
3. **SEO**: Update meta tags in `<head>` section for better search visibility
4. **Social Sharing**: Add Open Graph tags for better social media previews

## 📄 License

Feel free to use and modify these visualizations for your research and presentations.

## 🤝 Contributing

To update the charts:
1. Modify the Python scripts with new data
2. Run the scripts to regenerate HTML/PNG/SVG files
3. Commit and push changes
4. GitHub Pages will auto-update within minutes

---

**Questions?** Open an issue on the GitHub repository!
