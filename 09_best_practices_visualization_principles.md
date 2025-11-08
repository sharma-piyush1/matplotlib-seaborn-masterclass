# Data Visualization Best Practices

This document summarizes core principles for designing clear, meaningful, and professional visualizations. The goal of visualization is to communicate insight, not decorate a report.

---

## 1. Choose the Right Chart Type
Use each plot with purpose:

| Goal | Recommended Plot |
|-----|------------------|
| Compare categories | Bar, Grouped Bar |
| Show distribution shape | Histogram, KDE, Box, Violin |
| Show relationship between two variables | Scatter, Regression |
| Compare multiple numeric features | Pairplot, Heatmap |
| Track change over time | Line Plot |

Avoid using a chart because it "looks good." Always choose based on analytical purpose.

---

## 2. Limit Color Usage
- Use a **single palette** across the project for consistency.
- Use **one accent color** to highlight key data.
- Avoid neon and high-saturation colors.
- For most work, a palette like `deep`, `muted`, or `colorblind` is appropriate.

Color is for meaning, not decoration.

---

## 3. Maintain Readability
- Ensure text sizes are large enough to read.
- Label axes clearly and professionally.
- Avoid unnecessary text, patterns, or heavy gridlines.
- Remove chartjunk (3D effects, shadows, glow effects).

Clarity beats aesthetics.

---

## 4. Use Annotation to Communicate Insight
Mark points of interest using `annotate()`:
- Peaks
- Troughs
- Sudden changes
- Outliers
- Threshold breaches

A chart with no highlighted insight forces the viewer to do analytical guesswork.

---

## 5. Compare Using Shared Axes When Possible
When plotting multiple related charts:
- Share axes to create intuitive comparisons.
- Use consistent scaling.
- Align layouts with `subplots()` instead of separate figures.

This improves interpretability with minimal effort.

---

## 6. Show Distribution and Variation, Not Just Averages
Averages can hide important differences.

Prefer:
- Box plots (spread + outliers)
- Violin plots (distribution density)
- Scatter plots (sample-level variation)

Use bar plots only when variation is **not analytically relevant**.

---

## 7. Use Clean Legends and Titles
- Titles describe *what the viewer should notice*, not just what is plotted.
- Legends should not overlap data.
- Removing legend frame usually improves visual cleanliness.

Example good title:
> Tip Percentage Increases with Total Bill Size

Example bad title:
> Scatter Plot of Tip vs Total Bill

---

## 8. Avoid Over-plotting
If a scatter plot is too dense:
- Reduce alpha (transparency)
- Use hexbin or KDE plots
- Summarize via grouping first

More points ≠ more clarity.

---

## 9. Use Consistent Styling Across Entire Repo
- `style="whitegrid"`, `context="notebook"`, `palette="deep"` is a strong baseline.
- Set global rcParams once and avoid per-plot styling variations unless intentional.

Consistency communicates discipline and intentionality.

---

## Summary
A professional visualization:
- Has a clear purpose
- Uses appropriate chart type
- Minimizes unnecessary styling
- Highlights key insight directly
- Maintains aesthetic and structural consistency

If your visual does not **immediately answer a question or reveal an insight**, it needs to be improved.
