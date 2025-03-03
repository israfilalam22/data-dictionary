# BEPRC Database Data Dictionary

## Table: beprc_application_status_description

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number with default value of 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1=active, 0=inactive), default is 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1=deleted, 0=not deleted), default is 0 |
| APPLICATION_STATUS_ID | varchar(36) | Foreign key referencing beprc_application_status.OID |
| APPLICATION_TYPE_ID | varchar(36) | Foreign key referencing beprc_application_type.OID |
| TITLE | varchar(512) | Description of application status (INNV, INC, ENT status description) |
| CREATED_BY | varchar(64) | Username of the creator |
| CREATED_ON | datetime | Timestamp when record was created |
| UPDATED_BY | varchar(64) | Username of the last updater |
| UPDATED_ON | datetime | Timestamp when record was last updated |

## Table: beprc_application_status_user_description

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number with default value of 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1=active, 0=inactive), default is 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1=deleted, 0=not deleted), default is 0 |
| APPLICATION_TYPE_ID | varchar(36) | Foreign key referencing beprc_application_type.OID |
| APPLICATION_STATUS_ID | varchar(36) | Foreign key referencing beprc_application_status.OID |
| TITLE | varchar(512) | Application status description for users (INNV, INC, ENT application status) |
| CREATED_BY | varchar(64) | Username of the creator |
| CREATED_ON | datetime | Timestamp when record was created |
| UPDATED_BY | varchar(64) | Username of the last updater |
| UPDATED_ON | datetime | Timestamp when record was last updated |

## Table: beprc_application_sub_task

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number with default value of 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1=active, 0=inactive), default is 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1=deleted, 0=not deleted), default is 0 |
| APPLICATION_TASK_ID | varchar(36) | Foreign key referencing beprc_application_task.OID |
| ATTACHMENT_ID | varchar(36) | Foreign key referencing beprc_attachment.OID |
| NAME | varchar(255) | Name of the sub-task |
| START_DATE | date | Start date of the sub-task |
| END_DATE | date | End date of the sub-task |
| DURATION | int | Duration of the sub-task |
| DURATION_TYPE | varchar(4) | Type of duration (Month (M), Day (D)) |
| COMMENT | varchar(767) | Comment for each sub-task |
| STATUS | varchar(64) | Status of each sub-task |
| CREATED_BY | varchar(64) | Username of the creator |
| CREATED_ON | datetime | Timestamp when record was created |
| UPDATED_BY | varchar(64) | Username of the last updater |
| UPDATED_ON | datetime | Timestamp when record was last updated |
| START_MONTH | int | Starting month number |
| END_MONTH | int | Ending month number |
| SERIAL_NUMBER | int | Order/sequence number, default is 0 |

## Table: beprc_application_sub_task_history

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number with default value of 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1=active, 0=inactive), default is 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1=deleted, 0=not deleted), default is 0 |
| APPLICATION_TASK_HISTORY_ID | varchar(36) | Foreign key referencing beprc_application_task_history.OID |
| ATTACHMENT_ID | varchar(36) | Foreign key referencing beprc_attachment.OID |
| NAME | varchar(255) | Name of the sub-task |
| START_DATE | date | Start date of the sub-task |
| END_DATE | date | End date of the sub-task |
| COMMENT | varchar(767) | Comment for each sub-task |
| STATUS | varchar(64) | Status of each sub-task |
| CREATED_BY | varchar(64) | Username of the creator |
| CREATED_ON | datetime | Timestamp when record was created |
| UPDATED_BY | varchar(64) | Username of the last updater |
| UPDATED_ON | datetime | Timestamp when record was last updated |
| START_MONTH | int | Starting month number |
| END_MONTH | int | Ending month number |
| SERIAL_NUMBER | int | Order/sequence number, default is 0 |

## Table: beprc_application_submission_info

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number with default value of 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1=active, 0=inactive), default is 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1=deleted, 0=not deleted), default is 0 |
| APPLICATION_ID | varchar(36) | Foreign key referencing beprc_application_info.OID |
| SUBMITTED_ON | datetime | Timestamp when application was submitted |
| REVISION | int | Revision number of the submission, default is 0 |
| CREATED_BY | varchar(64) | Username of the creator |
| CREATED_ON | datetime | Timestamp when record was created |
| UPDATED_BY | varchar(64) | Username of the last updater |
| UPDATED_ON | datetime | Timestamp when record was last updated |

## Table: beprc_application_task

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number with default value of 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1=active, 0=inactive), default is 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1=deleted, 0=not deleted), default is 0 |
| APPLICATION_MILESTONE_ID | varchar(36) | Foreign key referencing beprc_application_milestone.OID |
| ATTACHMENT_ID | varchar(36) | Foreign key referencing beprc_attachment.OID |
| NAME | varchar(255) | Name of the task |
| START_DATE | date | Start date of the task |
| END_DATE | date | End date of the task |
| DURATION | int | Duration of the task |
| DURATION_TYPE | varchar(4) | Type of duration (Month (M), Day (D)) |
| COMMENT | varchar(767) | Comment for each task |
| STATUS | varchar(64) | Status for each task |
| CREATED_BY | varchar(64) | Username of the creator |
| CREATED_ON | datetime | Timestamp when record was created |
| UPDATED_BY | varchar(64) | Username of the last updater |
| UPDATED_ON | datetime | Timestamp when record was last updated |
| START_MONTH | int | Starting month number |
| END_MONTH | int | Ending month number |
| SERIAL_NUMBER | int | Order/sequence number, default is 0 |

## Table: beprc_application_task_history

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number with default value of 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1=active, 0=inactive), default is 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1=deleted, 0=not deleted), default is 0 |
| APPLICATION_MILESTONE_HISTORY_ID | varchar(36) | Foreign key referencing beprc_application_milestone_history.OID |
| ATTACHMENT_ID | varchar(36) | Foreign key referencing beprc_attachment.OID |
| NAME | varchar(255) | Name of the task |
| START_DATE | date | Start date of the task |
| END_DATE | date | End date of the task |
| COMMENT | varchar(767) | Comment for each task |
| STATUS | varchar(64) | Status for each task |
| CREATED_BY | varchar(64) | Username of the creator |
| CREATED_ON | datetime | Timestamp when record was created |
| UPDATED_BY | varchar(64) | Username of the last updater |
| UPDATED_ON | datetime | Timestamp when record was last updated |
| START_MONTH | int | Starting month number |
| END_MONTH | int | Ending month number |
| SERIAL_NUMBER | int | Order/sequence number, default is 0 |

## Table: beprc_application_type

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number with default value of 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1=active, 0=inactive), default is 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1=deleted, 0=not deleted), default is 0 |
| SERIAL_NUMBER | int | Order/sequence number |
| TITLE | varchar(255) | Title of the application type |
| TAG | varchar(255) | Tag identifier for the application type |
| DESCRIPTION | text | Detailed description of the application type |
| ATTACHMENT_ID | varchar(36) | Foreign key referencing beprc_attachment.OID for an attachment |
| GUIDELINE_DOC_ID | varchar(36) | Foreign key referencing beprc_attachment.OID for guidelines document |
| CREATED_BY | varchar(64) | Username of the creator |
| CREATED_ON | datetime | Timestamp when record was created |
| UPDATED_BY | varchar(64) | Username of the last updater |
| UPDATED_ON | datetime | Timestamp when record was last updated |

## Table: beprc_attachment

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number with default value of 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1=active, 0=inactive), default is 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1=deleted, 0=not deleted), default is 0 |
| FILE_TYPE | varchar(8) | Type of file (FILE, IMAGE) |
| ORIGINAL_FILE_NAME | varchar(640) | Original file name before upload |
| GIVEN_FILE_NAME | varchar(640) | Assigned file name after upload |
| DIRECTORY_NAME | varchar(36) | Directory where the file is stored |
| FILE_PATH | varchar(255) | Path to the file location |
| CREATED_BY | varchar(64) | Username of the creator |
| CREATED_ON | datetime | Timestamp when record was created |
| UPDATED_BY | varchar(64) | Username of the last updater |
| UPDATED_ON | datetime | Timestamp when record was last updated |
