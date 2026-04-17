# Nashik Grape Belt Retrospective Crop-Stress Analysis

## Case framing
- Crop: `grapes`
- Region: `Nashik vineyard belt, Maharashtra, India`
- AOI (west, south, east, north): `(73.94, 20.12, 74.03, 20.21)`
- Target season year: `2023`
- Baseline seasons: `[2020, 2021, 2022]`

## Key findings
- By 2023-10-09, the target-season crop-health trajectory had already diverged from baseline by at least 10.0% across 2 consecutive valid weekly bins.
- That early divergence signal appeared 158 days before harvest.
- By 2024-03-25, the anomaly had strengthened enough to satisfy the stricter confirmed-stress rule (2 consecutive weekly bins above the 1.25 z-score threshold).
- That confirmed stress signal appeared 10 days after harvest.
- The final pre-harvest vegetation underperformance proxy was 13.3% below baseline, based on satellite-derived canopy trajectories.
- This pipeline does not infer labeled yield; it reports a defensible vegetation-stress proxy that should be validated against harvest records or field observations when available.

## Signal timing
- Early divergence started on `2023-10-09`
- Early divergence persistence was satisfied by `2023-10-16`
- Early divergence lead time to nominal harvest: `158 days before harvest`
- Confirmed stress started on `2024-03-25`
- Confirmed stress persistence was satisfied by `2024-04-01`
- Confirmed stress lead time to nominal harvest: `10 days after harvest`
- Early divergence rule: `10.0%` below baseline for `2` consecutive valid weeks
- Confirmed stress rule: `1.25` composite z-score for `2` consecutive valid weeks

## Underperformance proxy
- Yield-stress proxy: `13.3%`
- Severity label: `moderate`
- Peak stress score: `2.16`
- Proxy definition: Composite negative vegetation deviation versus baseline in the final pre-harvest window. This is an underperformance proxy, not a labeled yield estimate.

## Data sufficiency
- Well-covered target-season weeks (`>=2` usable observations): 2023-09-04, 2023-09-11, 2023-09-25, 2023-10-02, 2023-10-09, 2023-10-16, 2023-10-23, 2023-11-13, 2023-11-20, 2023-11-27, 2023-12-11, 2024-01-01, 2024-01-22, 2024-02-05, 2024-02-26, 2024-03-11
- Sparse target-season weeks (`1` usable observation): 2023-10-30, 2023-11-06, 2023-12-18, 2023-12-25, 2024-01-08, 2024-01-15, 2024-02-19, 2024-03-04, 2024-03-18, 2024-03-25, 2024-04-01, 2024-04-08, 2024-04-15, 2024-04-22, 2024-04-29
- Missing target-season weeks (`0` usable observations): 2023-09-18, 2023-12-04, 2024-01-29, 2024-02-12
- Baseline-supported weeks (`>= 2` historical observations): 2023-09-04, 2023-10-02, 2023-10-09, 2023-10-16, 2023-10-23, 2023-10-30, 2023-11-06, 2023-11-13, 2023-11-20, 2023-11-27, 2023-12-04, 2023-12-11, 2023-12-18, 2023-12-25, 2024-01-01, 2024-01-08, 2024-01-15, 2024-01-22, 2024-01-29, 2024-02-05, 2024-02-12, 2024-02-19, 2024-02-26, 2024-03-04, 2024-03-11, 2024-03-18, 2024-03-25, 2024-04-01, 2024-04-08, 2024-04-15, 2024-04-22
- Conclusion confidence: `medium`
- Confidence rationale: The conclusion is supported by a usable core of target and baseline weeks, but some weeks are sparse.

## Caveats
- This is a retrospective, satellite-only crop-health assessment.
- The reported proxy is not a labeled yield estimate.
- Adding harvest records, parcel boundaries, or field scouting notes would materially improve confidence.

## Artifacts
- `scene_metrics_csv`: `/Users/harshitgajjar/Downloads/College/VIGIL - Earth/teesta /configs/outputs/nashik_grapes_retrospective/tables/scene_metrics.csv`
- `weekly_metrics_csv`: `/Users/harshitgajjar/Downloads/College/VIGIL - Earth/teesta /configs/outputs/nashik_grapes_retrospective/tables/weekly_metrics.csv`
- `target_vs_baseline_csv`: `/Users/harshitgajjar/Downloads/College/VIGIL - Earth/teesta /configs/outputs/nashik_grapes_retrospective/tables/target_vs_baseline.csv`
- `ndvi_figure`: `/Users/harshitgajjar/Downloads/College/VIGIL - Earth/teesta /configs/outputs/nashik_grapes_retrospective/figures/ndvi_baseline_vs_target.png`
- `evi_figure`: `/Users/harshitgajjar/Downloads/College/VIGIL - Earth/teesta /configs/outputs/nashik_grapes_retrospective/figures/evi_baseline_vs_target.png`
- `ndre_figure`: `/Users/harshitgajjar/Downloads/College/VIGIL - Earth/teesta /configs/outputs/nashik_grapes_retrospective/figures/ndre_baseline_vs_target.png`
- `composite_stress_figure`: `/Users/harshitgajjar/Downloads/College/VIGIL - Earth/teesta /configs/outputs/nashik_grapes_retrospective/figures/composite_stress_signal.png`
- `warning_map_figure`: `/Users/harshitgajjar/Downloads/College/VIGIL - Earth/teesta /configs/outputs/nashik_grapes_retrospective/figures/ndvi_warning_map.png`
- `summary_json`: `/Users/harshitgajjar/Downloads/College/VIGIL - Earth/teesta /configs/outputs/nashik_grapes_retrospective/reports/summary.json`
- `report_markdown`: `/Users/harshitgajjar/Downloads/College/VIGIL - Earth/teesta /configs/outputs/nashik_grapes_retrospective/reports/forensic_report.md`
- `findings_summary_markdown`: `/Users/harshitgajjar/Downloads/College/VIGIL - Earth/teesta /configs/outputs/nashik_grapes_retrospective/reports/findings_summary.md`
