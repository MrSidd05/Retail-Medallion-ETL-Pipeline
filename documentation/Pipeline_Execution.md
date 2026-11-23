# Pipeline Execution and Job Orchestration

## Databricks Job
The project uses a Databricks Job to sequence three notebook tasks:

1. `Bronze_Ingestion`
2. `Silver_Layer_Validation`
3. `Gold_Layer_Optimization_And_Final_Table` (Gold notebook task)

The dependency chain is sequential: Bronze → Silver → Gold.

The tasks use Serverless compute in the project workspace.

## Execution and recovery
A job execution was attempted; Bronze completed successfully while Silver failed. The Silver issue was corrected and repair/rerun behavior was explored to avoid rerunning successful upstream work where supported.

## Roadmap
- Reusable automated validation and audit logging.
- More comprehensive monitoring and alerting.
- Incremental processing.
- Retry/recovery strategies.
- Apache Airflow orchestration.
- Simulated streaming ingestion.
- Performance and cost optimization.
