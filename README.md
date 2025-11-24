# MaskFeat Training Analysis

This repository contains interactive visualizations of MaskFeat model training performance across different configurations.

## 🌐 Live Demo

View the dashboard at: [https://musicamatics.github.io/maskfeat-analysis/](https://musicamatics.github.io/maskfeat-analysis/)

## 📁 Files Included

- `index.html` - Main dashboard landing page
- `1_old_run_20warmup_bs128_interactive.html` - Chart 1: ViT-B Run 1 (old run, epochs 1-75)
- `2_old_run_20warmup_bs128_extended_ep100_interactive.html` - Chart 2: ViT-B Run 1 (old run, complete)
- `3_new_run_5warmup_bs512_interactive.html` - Chart 3: ViT-B Run 2 (new run, epochs 1-50)
- `4_comparison_old_vs_new_runs_interactive.html` - Chart 4: ViT-B Run 1 vs Run 2 comparison
- `5_vitl_run_5warmup_bs192_interactive.html` - Chart 5: ViT-L Run 3 (complete)
- `6_three_way_comparison_vitb_vitl_interactive.html` - Chart 6: Three-run comparison (Run 1, 2, 3)

## 📊 What's Included in the Dashboard

### Chart 1: ViT-B Run 1 (Old Run, Epochs 1-75)
- Configuration: 20 warmup epochs, batch size 128
- Initial training phase showing early convergence patterns
- Mean gap: 1.15%

### Chart 2: ViT-B Run 1 (Old Run, Complete)
- Configuration: 20 warmup epochs, batch size 128
- Full training trajectory through 100 epochs
- Mean gap: 3.78%

### Chart 3: ViT-B Run 2 (New Run, Epochs 1-50)
- Configuration: 5 warmup epochs, batch size 512
- Optimized training showing improved efficiency
- Mean gap: 1.24%

### Chart 4: ViT-B: Run 1 vs Run 2 Comparison
- Side-by-side comparison of both ViT-B configurations
- Run 1 (old) vs Run 2 (new) with complete data through 100 epochs
- Color-coded traces for easy distinction

### Chart 5: ViT-L Run 3 (Complete)
- Configuration: 5 warmup epochs, batch size 192
- Trained for 50 epochs
- Achieves 18.44% validation error at epoch 50
- Final training error: 10.00%
- Target: 14.3% top-1 error
- Mean gap: 1.23%

### Chart 6: Three-Run Comparison (Run 1, 2, 3)
- Complete comparison: ViT-B Run 1 (old), ViT-B Run 2 (new), and ViT-L Run 3
- ViT-B runs trained for 100 epochs, ViT-L trained for 50 epochs
- Demonstrates both configuration optimization and architecture scaling benefits
- Dual target lines: 16% for ViT-B, 14.3% for ViT-L

## 🎨 Features

- **Interactive Charts**: Hover for exact values, zoom, pan, and toggle traces
- **Responsive Design**: Works on desktop, tablet, and mobile
- **High-Resolution Exports**: Download PNG (2800×1800) or SVG versions
- **Embed Code**: Use provided HTML divs to embed charts elsewhere
- **Legend Groups**: Click legend items to show/hide related projections

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
