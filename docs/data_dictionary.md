# Data Dictionary

## M&E DQA Summary

| Field                    | Description                                                                                  |
| ------------------------ | -------------------------------------------------------------------------------------------- |
| `standard_facility_name` | Standardized name used for consistent facility reporting                                     |
| `facility_id`            | Unique identifier assigned to the health facility                                            |
| `reporting_period_std`   | Standardized reporting month in YYYY-MM format                                               |
| `period_dqa_flag`        | Indicates whether the record has a valid reporting period                                    |
| `duplicate_dqa_flag`     | Indicates whether the facility/reporting-period combination requires duplicate review        |
| `logical_test_u5`        | Logical consistency assessment related to malaria testing among children under five          |
| `logical_negative_u5`    | Logical consistency assessment related to negative malaria results among children under five |
| `logical_treatment_u5`   | Logical consistency assessment related to malaria treatment among children under five        |
| `logical_severe_u5`      | Logical consistency assessment related to severe malaria among children under five           |
| `logical_deaths_u5`      | Logical consistency assessment related to malaria-related deaths among children under five   |
| `dqa_logical_status`     | Overall logical DQA status for the record                                                    |

## Monthly DQA Summary

| Field                      | Description                                           |
| -------------------------- | ----------------------------------------------------- |
| `reporting_period_std`     | Reporting month used for aggregation                  |
| `records_assessed`         | Number of records assessed                            |
| `logical_failures`         | Count of logical testing failures                     |
| `treatment_anomalies`      | Count of treatment consistency failures               |
| `testing_anomalies`        | Count of testing/negative-result consistency failures |
| `severe_anomalies`         | Count of severe-malaria consistency failures          |
| `death_anomalies`          | Count of death consistency failures                   |
| `monthly_dqa_status`       | Overall monthly DQA status                            |
| `total_anomalies`          | Total detected anomalies across the DQA categories    |
| `anomaly_rate`             | Total anomalies divided by assessed records           |
| `records_requiring_review` | Number of records requiring additional review         |

## DQA Status Values

### PASS

No detected anomaly in the applicable DQA checks.

### FAIL

A logical consistency rule has identified an anomaly.

### Cannot Assess

The available data are insufficient to evaluate the applicable logical rule. This is retained as a review condition rather than automatically classified as a failure.

### REVIEW

The record or reporting period requires further investigation.
