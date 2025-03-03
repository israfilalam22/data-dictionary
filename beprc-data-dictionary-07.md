# BEPRC Database Schema Data Dictionary

## Table: beprc_application_status_description

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the record |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0), defaults to 0 |
| APPLICATION_STATUS_ID | varchar(36) | Foreign key reference to beprc_application_status table |
| APPLICATION_TYPE_ID | varchar(36) | Foreign key reference to beprc_application_type table |
| TITLE | varchar(512) | INNV, INC, ENT Status description |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Date and time when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Date and time when the record was last updated |

## Table: beprc_application_status_user_description

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the record |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0), defaults to 0 |
| APPLICATION_TYPE_ID | varchar(36) | Foreign key reference to beprc_application_type table |
| APPLICATION_STATUS_ID | varchar(36) | Foreign key reference to beprc_application_status table |
| TITLE | varchar(512) | INNV, INC, ENT Application Status description for User |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Date and time when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Date and time when the record was last updated |

## Table: beprc_application_sub_task

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the record |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0), defaults to 0 |
| APPLICATION_TASK_ID | varchar(36) | Foreign key reference to beprc_application_task table |
| ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table |
| NAME | varchar(255) | Name of the sub-task |
| START_DATE | date | Start date of the sub-task |
| END_DATE | date | End date of the sub-task |
| DURATION | int | Duration of the sub-task |
| DURATION_TYPE | varchar(4) | Type of duration: Month (M) or Day (D) |
| COMMENT | varchar(767) | Comment for each sub-task |
| STATUS | varchar(64) | Status for each sub-task |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Date and time when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Date and time when the record was last updated |
| START_MONTH | int | Start month of the sub-task |
| END_MONTH | int | End month of the sub-task |
| SERIAL_NUMBER | int | Serial number for ordering sub-tasks, defaults to 0 |

## Table: beprc_application_sub_task_history

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the record |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0), defaults to 0 |
| APPLICATION_TASK_HISTORY_ID | varchar(36) | Foreign key reference to beprc_application_task_history table |
| ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table |
| NAME | varchar(255) | Name of the sub-task |
| START_DATE | date | Start date of the sub-task |
| END_DATE | date | End date of the sub-task |
| COMMENT | varchar(767) | Comment for each sub-task |
| STATUS | varchar(64) | Status for each sub-task |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Date and time when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Date and time when the record was last updated |
| START_MONTH | int | Start month of the sub-task |
| END_MONTH | int | End month of the sub-task |
| SERIAL_NUMBER | int | Serial number for ordering sub-tasks, defaults to 0 |

## Table: beprc_application_submission_info

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the record |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0), defaults to 0 |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| SUBMITTED_ON | datetime | Date and time when the application was submitted |
| REVISION | int | Revision number of the submission, defaults to 0 |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Date and time when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Date and time when the record was last updated |

## Table: beprc_application_task

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the record |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0), defaults to 0 |
| APPLICATION_MILESTONE_ID | varchar(36) | Foreign key reference to beprc_application_milestone table |
| ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table |
| NAME | varchar(255) | Name of the task |
| START_DATE | date | Start date of the task |
| END_DATE | date | End date of the task |
| DURATION | int | Duration of the task |
| DURATION_TYPE | varchar(4) | Type of duration: Month (M) or Day (D) |
| COMMENT | varchar(767) | Comment for each task |
| STATUS | varchar(64) | Status for each task |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Date and time when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Date and time when the record was last updated |
| START_MONTH | int | Start month of the task |
| END_MONTH | int | End month of the task |
| SERIAL_NUMBER | int | Serial number for ordering tasks, defaults to 0 |

## Table: beprc_application_task_history

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the record |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0), defaults to 0 |
| APPLICATION_MILESTONE_HISTORY_ID | varchar(36) | Foreign key reference to beprc_application_milestone_history table |
| ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table |
| NAME | varchar(255) | Name of the task |
| START_DATE | date | Start date of the task |
| END_DATE | date | End date of the task |
| COMMENT | varchar(767) | Comment for each task |
| STATUS | varchar(64) | Status for each task |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Date and time when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Date and time when the record was last updated |
| START_MONTH | int | Start month of the task |
| END_MONTH | int | End month of the task |
| SERIAL_NUMBER | int | Serial number for ordering tasks, defaults to 0 |

## Table: beprc_application_type

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the record |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0), defaults to 0 |
| SERIAL_NUMBER | int | Serial number for ordering application types |
| TITLE | varchar(255) | Title of the application type |
| TAG | varchar(255) | Tag/identifier for the application type |
| DESCRIPTION | text | Detailed description of the application type |
| ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for attached files |
| GUIDELINE_DOC_ID | varchar(36) | Foreign key reference to beprc_attachment table for guideline documents |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Date and time when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Date and time when the record was last updated |

## Table: beprc_attachment

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the record |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0), defaults to 0 |
| FILE_TYPE | varchar(8) | Type of file: FILE or IMAGE |
| ORIGINAL_FILE_NAME | varchar(640) | Original name of the uploaded file |
| GIVEN_FILE_NAME | varchar(640) | Name given to the file in the system |
| DIRECTORY_NAME | varchar(36) | Name of the directory where the file is stored |
| FILE_PATH | varchar(255) | Path to the file in the storage system |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Date and time when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Date and time when the record was last updated |
