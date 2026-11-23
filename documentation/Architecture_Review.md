# Architecture Asset Review

- `pipeline_architecture.png` is the recommended primary diagram for the README. It reflects the implemented Bronze/Silver/Gold batch workflow and sequential Databricks Job orchestration.
- `notebook_diagram_architecture.png` is a useful layer-by-layer supplementary diagram.
- `job_orachestration.png` is an actual Databricks Job screenshot showing the dependency chain. It documents configuration, not a successful run.
- `medallion_workflow.png` illustrates future direction (Airflow, streaming, monitoring/retry/backfill). Treat it as a roadmap illustration, not the current implementation.
- `Retail Medallion ETL Pipeline Infographic.png` is a visually rich overview but contains an embedded job view showing a failed Silver task and blends roadmap items with implemented features. It is not recommended as the primary architecture image in the repository or README; use it only as a historical/overview visual if desired.

The README uses the replacement diagram and keeps roadmap features clearly identified as planned.


## Animated architecture added

`architecture/pipeline_architecture.gif` is now the primary animated visual and is embedded at the top of the repository README. It provides a visual flow overview. Scheduling times, retries, and notifications appearing in the animation are illustrative and should not be interpreted as confirmed Job configuration. The verified Job task dependency is Bronze → Silver → Gold.
