# AWS DataLake Solutions

**Data Lake** - an architectural approach that you can use to store all your data in a centralized repository, typically object storage. Allowing for centralized access, management, quality controls, and governance.

Key features include:

- Scalability of S3
- Discoverability with AWS Glue crawling, cataloging, and indexing
- Shareability across roles in an organization
- Agility with managed provisioning and automated DevOps tools

## Setting Up Storage

A common data lake storage set up may involve multiple buckets or multiple prefixes within a bucket that segments data into the following zones / layers.

1. Raw Storage - stores data as-received, in its "raw" state from original source.
2. Clean Storage - storing data transformed into a standardized format or schema which may involve normalization.
3. Curated Storage - stores cleaned data that may be joined or transformed with other cleaned data for the purpose of specific analytical processes.

This is similar to the medallion architecture in data engineering, commonly referred to as bronze, silver, and gold level datasets.

Depending on the use case, a data lake may also have one of the following storage layers.

- Landing Zone - Often used when data received contains PII/PHI that needs to be masked before proceeding to raw storage.
- Log Zone - This is the landing for all system log files, allowing for a centralized store of system activity.
- Archived Zone - A specific Zone for historical or compliance related data which is minimally accessed.
- Sandbox Zone - Used for experimental or exploratory data analysis.

See [AWS Prescriptive Guidance](https://docs.aws.amazon.com/prescriptive-guidance/latest/defining-bucket-names-data-lakes/naming-structure-data-layers.html) for S3 bucket naming conventions.

### S3 Lifecycle Management

Amazon S3 Lifecycle Rules are used in conjunction with bucket storage, automating offload of infrequently accessed data to cold storage classes like S3 Glacier in order to optimize storage costs. For example, once data is added to raw storage and processed into clean storage, the raw data artifact is rarely accessed again. Thus is can be offloaded to a cheaper storage class with infrequent access. An example set of rules may appear as follows:

1. `object_age > 1 year`, then S3-standard --> S3-IA (Infrequent Access)
2. `object_age > 2 year`, then S3-IA --> Glacier Deep Archive
3. `object_age > 7 year`, then delete / expire data object

Different Storage Classes available are as follows:

- S3 Intelligence Tiering - automatically moves data to the most cost-effective storage tier based on how frequently it is accessed.
- S3 Standard
- S3 Express One Zone
- S3 Standard Infrequent Access
- S3 One Zone Infrequent Access
- S3 Glacier Instant Retrieval
- S3 Glacier Flexible Retrieval
- S3 Glacier Deep Archive

Other considerations include:

- If multipart uploads are common in your data workflow, set a lifecycle rule to automatically clean up or expire incomplete segments that may have failed to upload.
- You can set a lifecycle rule at the prefix level for fine grained controls.
- Lifecycle costs are proportional to the number of data objects being transitioned across tiers. Consider aggregating objects by zipping or compressing prior to transition.
- S3 object tagging enables further access controls, analysis, and lifecycle policy controls on a granular level, e.g. tag by business unit to analyze relative costs.
- S3 **Storage Lens** gives admins a snapshot view of storage across the organization, view metric, insights, and optimizations all the way down to the prefix level.

## DataLake Ingest

