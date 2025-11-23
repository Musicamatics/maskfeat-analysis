# MaskFeat Training Analysis

This repository contains interactive visualizations of MaskFeat model training performance across different configurations.

## 🌐 Live Demo

View the dashboard at: [https://musicamatics.github.io/maskfeat-analysis/](https://musicamatics.github.io/maskfeat-analysis/)

## 📁 Files Included

- `index.html` - Main dashboard landing page
- `1_old_run_20warmup_bs128_interactive.html` - Chart 1: Baseline configuration
- `2_old_run_20warmup_bs128_extended_ep100_interactive.html` - Chart 2: Extended training run
- `3_new_run_5warmup_bs512_interactive.html` - Chart 3: Optimized configuration
- `4_comparison_old_vs_new_runs_interactive.html` - Chart 4: Comparative analysis
- `5_vitl_run_5warmup_bs192_interactive.html` - Chart 5: ViT-L performance
- `6_three_way_comparison_vitb_vitl_interactive.html` - Chart 6: ViT-B vs ViT-L comparison

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
- Direct comparison of old vs new ViT-B configurations
- Color-coded traces for easy distinction
- Configuration details in top-right boxes

### Chart 5: ViT-L Performance
- Configuration: 5 warmup epochs, batch size 192
- Trained for 50 epochs
- Achieves 18.44% validation error at epoch 50
- Final training error: 10.00%
- Target: 14.3% top-1 error
- Mean gap: 1.23%

### Chart 6: ViT-B vs ViT-L Comparison
- Three-way comparison: ViT-B baseline, ViT-B optimized, and ViT-L
- ViT-L trained for 50 epochs with 5 warmup epochs, batch size 192
- ViT-B models trained for 100 epochs
- Demonstrates architecture scaling benefits
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
