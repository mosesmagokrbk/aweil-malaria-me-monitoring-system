# Data Quality Assessment Methodology

## 1. Purpose

The Aweil Malaria M&E Monitoring and Data Quality System applies a structured data-quality assessment process to facility-level malaria reporting data.

The objective is to identify data-quality issues before the data are used for monitoring, analysis, reporting, or management decisions.

## 2. Data Quality Workflow

The system follows this workflow:

1. Facility reporting
2. Data standardization
3. Duplicate detection
4. Reporting-period validation
5. Logical consistency checks
6. Facility/period DQA assessment
7. Monthly DQA aggregation
8. Management review

## 3. Data Standardization

Facility names and reporting periods are standardized to create consistent identifiers for analysis.

Standardized facility names and facility IDs allow records originating from the same facility to be reliably grouped and compared.

## 4. Duplicate Detection

Duplicate records are investigated using facility and reporting-period combinations.

Records with the same facility and reporting period are flagged for review rather than automatically deleted. This preserves the original evidence and supports investigation.

## 5. Reporting-Period Validation

Each record is checked against the expected reporting period.

Records with incorrect or inconsistent reporting periods are flagged for review.

## 6. Logical DQA Checks

The system performs logical consistency checks across key malaria indicators, including:

* Testing
* Negative results
* Treatment
* Severe malaria
* Deaths

Each check produces an interpretable status such as:

* PASS
* FAIL
* Cannot Assess

"Cannot Assess" is retained as a review condition and is not automatically treated as a failure.

## 7. Monthly DQA Aggregation

The Monthly DQA Summary groups records by `reporting_period_std`.

The following indicators are calculated:

| Indicator                  | Definition                                                       |
| -------------------------- | ---------------------------------------------------------------- |
| `records_assessed`         | Number of records assessed during the reporting period           |
| `logical_failures`         | Number of records failing the logical testing check              |
| `treatment_anomalies`      | Number of records failing the treatment consistency check        |
| `testing_anomalies`        | Number of records failing the testing/negative consistency check |
| `severe_anomalies`         | Number of records failing the severe-malaria consistency check   |
| `death_anomalies`          | Number of records failing the deaths consistency check           |
| `total_anomalies`          | Sum of the five anomaly categories                               |
| `anomaly_rate`             | Total anomalies divided by records assessed                      |
| `records_requiring_review` | Records requiring additional DQA review                          |
| `monthly_dqa_status`       | Overall monthly interpretation                                   |

## 8. Management Status Rule

The monthly status is assigned using the following rule:

* `PASS` — no detected anomalies across the assessed DQA categories.
* `REVIEW` — at least one anomaly requires investigation.

The status is intended as a management signal and does not replace investigation of individual records.

## 9. Current Demonstration Results

For the current demonstration dataset:

* July 2026: 1 record assessed and 1 treatment anomaly identified.
* August 2026: 7 records assessed and 2 treatment anomalies identified.
* No testing, severe-malaria, or death anomalies were identified in the current sample.
* Records marked "Cannot Assess" remain visible for review rather than being classified automatically as failures.

## 10. Data Governance

The repository should contain only synthetic, aggregated, or appropriately de-identified information suitable for public portfolio demonstration.

Individual-level or otherwise sensitive health information should not be published to a public repository.

## 11. Intended Use

This workflow demonstrates practical M&E competencies in:

* Data management
* Data quality assessment
* Excel-based analysis
* Data validation
* Duplicate investigation
* Indicator consistency checking
* Monthly reporting
* Management-oriented interpretation
* Documentation
