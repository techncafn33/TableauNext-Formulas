# Tableau Next – Pipeline Risk & Opportunity Metrics

This repository contains representative calculation logic used to define key semantic metrics and composite indicators in a Tableau Next solution built within the Salesforce platform.

The purpose of this repository is to provide transparency into how governed, reusable metrics were modeled in the semantic layer to support pipeline health analysis, opportunity risk assessment, and revenue forecasting.

---

## Repository Structure

- `metrics/`  
  Core semantic metrics reused across Tableau Next dashboards, including:
  - Weighted Pipeline Value
  - Win Rate
  - Sales Cycle (Won)
  - Pipeline Risk Index (PRI)

- `metrics/pri_components/`  
  Discrete, normalized component metrics used to compose the Pipeline Risk Index, such as:
  - Sales Cycle Risk
  - Deal Size Risk
  - Forecast Confidence Risk
  - Recency Risk

- `helpers/`  
  Supporting row-level calculations used as building blocks for semantic metrics (e.g., sales cycle duration, deal age).

---

## Design Approach

- Metrics are defined once in the semantic layer and reused consistently across analytic views.
- Composite metrics (such as the Pipeline Risk Index) are intentionally decomposed into understandable components to ensure explainability and trust.
- Calculations are written in Tableau Next–style expression syntax and are intended to illustrate semantic intent rather than serve as executable code artifacts.

---

## Notes on Scope

- The solution focuses on opportunity-centric analytics, including pipeline value, conversion outcomes, sales cycle performance, and forecast confidence.
- Engagement- and activity-based signals were intentionally excluded due to object availability and sample data constraints within the contest org.

---

## Future Enhancements

With additional time and expanded object availability, engagement events and activity-based signals would be incorporated using proper related-record identifiers. These signals would further enhance opportunity-level risk scoring and enable deeper analysis of sales momentum and responsiveness.
