# MySQL Database Schema Data Dictionary

## Table: beprc_pm_milestone_history

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| PROCESS_STATUS | varchar(36) | Current process status (PENDING, REJECTED, ACCEPTED) |
| REVISION | int | Revision number of the record |
| PM_INFO_ID | varchar(36) | Foreign key to beprc_pm_info table (PM Info Id) |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| PM_MILESTONE_ID | varchar(36) | Foreign key to beprc_pm_milestone table |
| NAME | varchar(255) | Name of the milestone |
| WEIGHT | double | Weight value for the milestone |
| START_MONTH | int | Start month number |
| END_MONTH | int | End month number |
| START_DATE | date | Start date of the milestone |
| END_DATE | date | End date of the milestone |
| DESCRIPTION | text | Description of the milestone |
| APPROVAL_DOC_ID | varchar(36) | Foreign key to beprc_attachment table for approval document |
| STATUS | varchar(64) | Status of the milestone |
| ADMIN_INFO_REMARK | text | Administrative information remarks |
| ADMIN_INFO_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for admin info attachment |
| ADMIN_PROGRESS_REMARK | text | Administrative progress remarks |
| ADMIN_PROGRESS_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for admin progress attachment |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Timestamp of creation |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Timestamp of last update |

## Table: beprc_pm_period

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| TYPE | varchar(48) | Type of period |
| SERIAL_NUMBER | int | Serial number for ordering |
| START_DATE | date | Start date of the period |
| START_MONTH | int | Start month number |
| END_DATE | date | End date of the period |
| END_MONTH | int | End month number |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Timestamp of creation |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Timestamp of last update |

## Table: beprc_pm_permission

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| PERMISSION_TYPE | varchar(127) | Type of permission |
| HAS_PERMISSION | tinyint(1) | Flag indicating if permission is granted (1) or not (0) |
| APPROVAL_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for approval document |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Timestamp of creation |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Timestamp of last update |

## Table: beprc_pm_procurement

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| DOC_ID | varchar(36) | Foreign key to beprc_attachment table for document |
| PROCESS_STATUS | varchar(36) | Current process status (PENDING, REJECTED, ACCEPTED) |
| REVISION | int | Revision number of the record |
| SERIAL_NUMBER | int | Serial number for ordering |
| ADMIN_REMARK | text | Administrative remarks |
| ADMIN_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for admin attachment |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Timestamp of creation |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Timestamp of last update |

## Table: beprc_pm_quarter

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| SERIAL_NUMBER | int | Serial number for ordering |
| START_DATE | date | Start date of the quarter |
| START_MONTH | int | Start month number |
| END_DATE | date | End date of the quarter |
| END_MONTH | int | End month number |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Timestamp of creation |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Timestamp of last update |

## Table: beprc_pm_report

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| PM_INFO_ID | varchar(36) | Foreign key to beprc_pm_info table (PM Info Id) |
| REPORT_TYPE_ID | varchar(36) | Foreign key to beprc_pm_report_type table |
| SUBMISSION_END_ON | date | Deadline for submission |
| SUBMITTED_ON | date | Date when report was submitted |
| SUBMISSION_STATUS | varchar(64) | Status of submission |
| PROCESS_STATUS | varchar(36) | Current process status (PENDING, REJECTED, ACCEPTED) |
| DESCRIPTION | text | Description of the report |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Timestamp of creation |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Timestamp of last update |

## Table: beprc_pm_report_type

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| NAME | varchar(128) | Name of the report type |
| TAG | varchar(128) | Tag/code for the report type |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Timestamp of creation |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Timestamp of last update |

## Table: beprc_pm_sub_task

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| PROCESS_STATUS | varchar(36) | Current process status (PENDING, REJECTED, ACCEPTED) |
| REVISION | int | Revision number of the record |
| PM_TASK_ID | varchar(36) | Foreign key to beprc_pm_task table (PM TASK Id) |
| SERIAL_NUMBER | int | Serial number for ordering |
| ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table |
| NAME | varchar(255) | Name of the sub-task |
| START_MONTH | int | Start month number |
| END_MONTH | int | End month number |
| START_DATE | date | Start date of the sub-task |
| END_DATE | date | End date of the sub-task |
| COMMENT | varchar(767) | Comments about the sub-task |
| IS_DONE | tinyint(1) | Flag indicating if the sub-task is completed (1) or not (0) |
| PREV_IS_DONE | tinyint(1) | Previous completion status |
| STATUS | varchar(64) | Status of the sub-task |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Timestamp of creation |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Timestamp of last update |

## Table: beprc_pm_task

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| PROCESS_STATUS | varchar(36) | Current process status (PENDING, REJECTED, ACCEPTED) |
| REVISION | int | Revision number of the record |
| PM_MILESTONE_ID | varchar(36) | Foreign key to beprc_pm_milestone table (PM MILESTONE Id) |
| SERIAL_NUMBER | int | Serial number for ordering |
| ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table |
| NAME | varchar(255) | Name of the task |
| START_MONTH | int | Start month number |
| END_MONTH | int | End month number |
| START_DATE | date | Start date of the task |
| END_DATE | date | End date of the task |
| COMMENT | varchar(767) | Comments about the task |
| IS_DONE | tinyint(1) | Flag indicating if the task is completed (1) or not (0) |
| HAS_SUBTASK | tinyint(1) | Flag indicating if the task has sub-tasks (1) or not (0) |
| PREV_IS_DONE | tinyint(1) | Previous completion status |
| STATUS | varchar(64) | Status of the task |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Timestamp of creation |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Timestamp of last update |

## Table: beprc_report_info

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| PM_INFO_ID | varchar(36) | Foreign key to beprc_pm_info table (PM Info Id) |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| SERIAL_NUMBER | int | Serial number for ordering |
| REPORT_TYPE | varchar(64) | Type of report |
| QUARTER_ID | varchar(36) | Foreign key to beprc_pm_quarter table (Quarter Id) |
| HALF_YEAR_ID | varchar(36) | Foreign key to beprc_pm_half_year table (Half Year Id) |
| ANNUAL_YEAR_ID | varchar(36) | Foreign key to beprc_pm_annual_year table (Annual Year Id) |
| CREATOR | varchar(36) | Creator type (SYSTEM, ADMIN) |
| ADMIN_REPORT_SAMPLE_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for report sample |
| NAME | varchar(255) | Name of the report |
| DUE_ON | date | Due date for the report |
| REPORT_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for report |
| SUBMITTED_ON | date | Date when report was submitted |
| DESCRIPTION | text | Description of the report |
| PROCESS_STATUS | varchar(36) | Current process status (PENDING, REJECTED, ACCEPTED) |
| REVISION | int | Revision number of the record |
| ADMIN_REMARK | text | Administrative remarks |
| ADMIN_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for admin attachment |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Timestamp of creation |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Timestamp of last update |
