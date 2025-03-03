# BEPRC Database Schema Data Dictionary

## Table: beprc_lab_development_application_summary

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| REVISION | int | Revision number of the record, defaults to 0 |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| APPLICATION_DETAILS_ID | varchar(36) | Foreign key reference to beprc_application_details table |
| COVER_PAGE_ID | varchar(36) | Foreign key reference to beprc_attachment table for cover page |
| EXECUTIVE_SUMMARY_ID | varchar(36) | Foreign key reference to beprc_attachment table for executive summary |
| INTRODUCTION_BACKGROUND_ID | varchar(36) | Foreign key reference to beprc_attachment table for introduction background |
| OBJECTIVE_ID | varchar(36) | Foreign key reference to beprc_attachment table for objectives |
| DESCRIPTION_OF_THE_PROPOSED_HARDWARE_SOFTWARE_ID | varchar(36) | Foreign key reference to beprc_attachment table for hardware/software description |
| DESCRIPTION_OF_ASSESSMENT_CRITERIA_ID | varchar(36) | Foreign key reference to beprc_attachment table for assessment criteria |
| LAB_LOCATION_DETAILS_ID | varchar(36) | Foreign key reference to beprc_attachment table for lab location details |
| PROJECT_MANAGEMENT_TEAM_ID | varchar(36) | Foreign key reference to beprc_attachment table for project management team |
| OPERATION_OF_THE_LAB_ID | varchar(36) | Foreign key reference to beprc_attachment table for lab operation details |
| MASTER_SCHEDULE_ID | varchar(36) | Foreign key reference to beprc_attachment table for master schedule |
| BUDGET_AND_BUDGET_JUSTIFICATION_ID | varchar(36) | Foreign key reference to beprc_attachment table for budget justification |
| REMARKS_ID | varchar(36) | Foreign key reference to beprc_attachment table for remarks |
| ATTACHMENT_DECLARATION_ID | varchar(36) | Foreign key reference to beprc_attachment table for attachment declarations |
| ORGANIZATION_PDF_ID | varchar(36) | Foreign key reference to beprc_attachment table for organization PDF |
| PROPOSAL_PDF_ID | varchar(36) | Foreign key reference to beprc_attachment table for proposal PDF |
| CREATED_BY | varchar(64) | Username of the user who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the user who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_lab_program

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| LAB_PROGRAM_CODE | varchar(64) | Code identifier for the lab program |
| LAB_PROJECT_DURATION | int | Duration of the lab project in months/years |
| LAB_PROJECT_AMOUNT | double | Budget amount allocated for the lab project |
| LAB_PROGRAM_TITLE | text | Title of the lab program |
| SYNOPSIS_OF_PROGRAM | text | Brief summary or overview of the program |
| IS_OPEN_DEADLINE | tinyint(1) | Flag indicating if the program has an open deadline |
| DEADLINE | date | Application deadline date for the program |
| PUBLISHED_DATE | date | Date when the program was published |
| ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for program documents |
| THUMBNAIL_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for thumbnail image |
| CREATED_BY | varchar(64) | Username of the user who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the user who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_member_role

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| TAG | varchar(64) | Role tag (e.g., PI, CO-PI, Other) |
| TITLE | varchar(64) | Title of the role (e.g., Principal Investigator, Co-Principal Investigator) |
| CREATED_BY | varchar(64) | Username of the user who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the user who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_message

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for attachments |
| SERIAL_NUMBER | int | Sequential number identifier for the message |
| TITLE | varchar(255) | Title or subject of the message |
| DESIGNATION | varchar(128) | Designation of the sender or recipient |
| DETAILS | text | Content of the message |
| CREATED_BY | varchar(64) | Username of the user who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the user who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_news_notice

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| TYPE | varchar(16) | Type of the entry (NEWS, NOTICE, ARTICLE, FUNDING) |
| TITLE | varchar(255) | Title of the news or notice |
| SERIAL_NUMBER | int | Sequential number identifier for the news/notice |
| DETAILS | text | Content of the news or notice |
| PUBLISH_DATE | datetime | Date and time when the news/notice was published |
| EXPIRY_DATE | datetime | Date and time when the news/notice expires |
| IS_PUBLISHED | tinyint(1) | Flag indicating if the news/notice is published |
| ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for attachments |
| CREATED_BY | varchar(64) | Username of the user who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the user who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_notification

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| USER_ID | varchar(36) | Foreign key reference to beprc_user table for recipient |
| TITLE | varchar(128) | Title or subject of the notification |
| DESCRIPTION | varchar(255) | Description or content of the notification |
| ACTION | varchar(255) | Action URL or identifier related to the notification |
| IS_READ | tinyint(1) | Flag indicating if the notification has been read, defaults to 0 |
| CREATED_BY | varchar(64) | Username of the user who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the user who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_notification_config

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| INFO_ID | varchar(36) | Foreign key reference to beprc_notification_info table |
| TYPE | varchar(16) | Notification type (EMAIL, SMS, PUSH) |
| TEMPLATE | text | Template content for the notification |
| CREATED_BY | varchar(64) | Username of the user who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the user who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_notification_history

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| CONFIG_ID | varchar(36) | Foreign key reference to beprc_notification_config table |
| DESTINATION | varchar(64) | Destination address (email, phone number, device ID) |
| USER_TYPE | varchar(128) | Type of user receiving the notification |
| CONTENT | text | Content of the notification |
| RELATIVE_PATH | varchar(255) | Relative path for any action or attachment |
| IS_READ | tinyint(1) | Flag indicating if the notification has been read, defaults to 0 |
| CREATED_BY | varchar(64) | Username of the user who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the user who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_notification_info

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| TAG | varchar(128) | Unique tag identifier for the notification type |
| DESCRIPTION | varchar(255) | Description of the notification type |
| CREATED_BY | varchar(64) | Username of the user who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the user who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_other_details

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| APPLICATION_DETAILS_ID | varchar(36) | Foreign key reference to beprc_application_details table |
| DETAILS | text | Additional details content |
| TYPE | varchar(64) | Type of details |
| CREATED_BY | varchar(64) | Username of the user who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the user who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_other_details_history

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| REVISION | int | Revision number of the record, defaults to 0 |
| APPLICATION_DETAILS_ID | varchar(36) | Foreign key reference to beprc_application_details table |
| DETAILS | text | Additional details content |
| TYPE | varchar(64) | Type of details |
| CREATED_BY | varchar(64) | Username of the user who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the user who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_pm_agreement

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| PM_INFO_ID | varchar(36) | Foreign key reference to beprc_pm_info table |
| DOC_ID | varchar(36) | Foreign key reference to beprc_attachment table for agreement documents |
| IS_READONLY | tinyint(1) | Flag indicating if the agreement is read-only, defaults to 0 |
| PROCESS_STATUS | varchar(36) | Status of the agreement process (PENDING, REJECTED, ACCEPTED) |
| REVISION | int | Revision number of the record, defaults to 0 |
| CREATED_BY | varchar(64) | Username of the user who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the user who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |
| ADMIN_REMARK | text | Administrative remarks on the agreement |
| ADMIN_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for admin documents |

## Table: beprc_pm_allocation

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| PM_DETAILS_ID | varchar(36) | Foreign key reference to beprc_pm_details table |
| PM_BUDGET_TYPE_ID | varchar(36) | Foreign key reference to beprc_budget_type table |
| PM_QUARTER_ID | varchar(36) | Foreign key reference to beprc_pm_quarter table |
| ALLOCATION_AMOUNT | double | Amount allocated for the budget item |
| DETAILS | text | Details about the allocation |
| PROCESS_STATUS | varchar(36) | Status of the allocation process (PENDING, REJECTED, ACCEPTED), defaults to ACCEPTED |
| REVISION | int | Revision number of the record, defaults to 0 |
| ADMIN_REMARK | text | Administrative remarks on the allocation |
| ADMIN_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for admin documents |
| CREATED_BY | varchar(64) | Username of the user who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the user who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |
