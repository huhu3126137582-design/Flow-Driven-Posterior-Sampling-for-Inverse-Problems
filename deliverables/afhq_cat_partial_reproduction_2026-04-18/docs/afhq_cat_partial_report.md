# afhq_cat Partial Reproduction Report

## Scope

This report summarizes the publicly reproducible benchmark groups that have already finished in the current run.

| Scope | Completed Groups | Total Groups | Progress |
|---|---:|---:|---:|
| afhq_cat only | 5 | 12 | 41.7% |
| Public benchmark default plan | 5 | 36 | 13.9% |

## Metric Comparison

| Task | Method | PSNR | SSIM | FID | LPIPS | Runtime (hr) |
|---|---:|---:|---:|---:|---:|---:|
| sr_avgpool | flowdps | 24.830 | 0.6329 | 20.775 | 0.2083 | 3.91 |
| sr_avgpool | flowchef | 24.738 | 0.6848 | 58.340 | 0.2665 | 2.21 |
| sr_avgpool | psld | 11.809 | 0.4346 | 321.913 | 0.6564 | 3.74 |
| sr_bicubic | flowdps | 24.936 | 0.6322 | 19.261 | 0.1989 | 4.67 |
| sr_bicubic | flowchef | 24.909 | 0.6816 | 55.649 | 0.2658 | 2.11 |

![Metric overview](afhq_cat_metric_overview.png)

## Current Takeaways

- `sr_avgpool`: best PSNR = flowdps (24.830); best FID = flowdps (20.775); best LPIPS = flowdps (0.208)
- `sr_bicubic`: best PSNR = flowdps (24.936); best FID = flowdps (19.261); best LPIPS = flowdps (0.199)

## Qualitative Visualizations

### sr_avgpool

![sr_avgpool](afhq_cat_sr_avgpool_qualitative.png)

### sr_bicubic

![sr_bicubic](afhq_cat_sr_bicubic_qualitative.png)
