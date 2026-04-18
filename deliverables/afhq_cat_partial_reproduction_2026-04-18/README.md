# AFHQ-Cat Partial Reproduction Package

This folder collects the already reproduced benchmark outputs for `afhq_cat` and the documentation generated from them.

## Scope

- Status: paused immediately after `afhq_cat / sr_bicubic / flowchef` finished
- Completed benchmark groups: 5
- Dataset-level progress: `5 / 12` groups (`41.7%`)
- Public benchmark default-plan progress: `5 / 36` groups (`13.9%`)

## Included Contents

- `docs/afhq_cat_partial_report.md`
  - Main write-up with metric tables, progress summary, and qualitative comparison figures.
- `figures/afhq_cat_metric_overview.png`
  - Metric visualization across the completed groups.
- `figures/afhq_cat_sr_avgpool_qualitative.png`
  - Visual comparison for `sr_avgpool`.
- `figures/afhq_cat_sr_bicubic_qualitative.png`
  - Visual comparison for `sr_bicubic`.
- `tables/afhq_cat_completed_only.csv`
  - Clean table containing only the completed `afhq_cat` rows.
- `tables/full_summary_snapshot.csv`
  - Snapshot of the full benchmark summary file at the moment of packaging.
- `results/afhq_cat/<task>/<method>/run_meta.json`
  - Per-run metadata and final metrics for each completed group.

## Completed Groups

- `afhq_cat / sr_avgpool / flowchef`
- `afhq_cat / sr_avgpool / flowdps`
- `afhq_cat / sr_avgpool / psld`
- `afhq_cat / sr_bicubic / flowchef`
- `afhq_cat / sr_bicubic / flowdps`

## Quick Metric Snapshot

| Task | Method | PSNR | SSIM | FID | LPIPS | Runtime (hr) |
|---|---:|---:|---:|---:|---:|---:|
| sr_avgpool | flowdps | 24.830 | 0.6329 | 20.775 | 0.2083 | 3.91 |
| sr_avgpool | flowchef | 24.738 | 0.6848 | 58.340 | 0.2665 | 2.21 |
| sr_avgpool | psld | 11.809 | 0.4346 | 321.913 | 0.6564 | 3.74 |
| sr_bicubic | flowdps | 24.936 | 0.6322 | 19.261 | 0.1989 | 4.67 |
| sr_bicubic | flowchef | 24.909 | 0.6816 | 55.649 | 0.2658 | 2.11 |

## Notes

- The benchmark controller was paused after the requested `flowchef` run completed, so no later groups were started.
- The `sr_bicubic / flowchef` metrics were backfilled after pausing, then synchronized into the summary snapshot and report.
- The main benchmark outputs still remain in `workdir/public_sd3_benchmark/` if you want to inspect original directories directly.

## Resume Point

If you want to continue later, the next unfinished `afhq_cat` groups start from:

- `afhq_cat / sr_bicubic / psld`
- `afhq_cat / deblur_gauss / flowdps`
- `afhq_cat / deblur_gauss / flowchef`
- `afhq_cat / deblur_gauss / psld`
- `afhq_cat / deblur_motion / flowdps`
- `afhq_cat / deblur_motion / flowchef`
- `afhq_cat / deblur_motion / psld`
