# BEPRC Database Schema Documentation

## Table: BEPRC_APPLICATION_MILESTONE

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_ID | VARCHAR(36) | Foreign key to beprc_application_info table |
| APPLICATION_DETAILS_ID | VARCHAR(36) | Foreign key to beprc_application_details table |
| NAME | VARCHAR(255) | Name of the milestone |
| WEIGHT | DOUBLE | Weight/importance of the milestone |
| START_DATE | DATE | Start date of the milestone |
| END_DATE | DATE | End date of the milestone |
| DESCRIPTION | TEXT | Detailed description of the milestone |
| STATUS | VARCHAR(64) | Current status of the milestone |
| CREATED_BY | VARCHAR(64) | User who created the record |
| CREATED_ON | DATETIME | Timestamp when the record was created |
| UPDATED_BY | VARCHAR(64) | User who last updated the record |
| UPDATED_ON | DATETIME | Timestamp when the record was last updated |
| START_MONTH | INT | Start month of the milestone |
| END_MONTH | INT | End month of the milestone |

## Table: BEPRC_APPLICATION_MILESTONE_HISTORY

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the record is deleted (1) or not (0) |
| REVISION | INT | Revision number for tracking history |
| APPLICATION_ID | VARCHAR(36) | Foreign key to beprc_application_info table |
| APPLICATION_DETAILS_ID | VARCHAR(36) | Foreign key to beprc_application_details table |
| NAME | VARCHAR(255) | Name of the milestone |
| WEIGHT | DOUBLE | Weight/importance of the milestone |
| START_DATE | DATE | Start date of the milestone |
| END_DATE | DATE | End date of the milestone |
| START_MONTH | INT | Start month of the milestone |
| END_MONTH | INT | End month of the milestone |
| DESCRIPTION | TEXT | Detailed description of the milestone |
| STATUS | VARCHAR(64) | Status of the milestone |
| CREATED_BY | VARCHAR(64) | User who created the record |
| CREATED_ON | DATETIME | Timestamp when the record was created |
| UPDATED_BY | VARCHAR(64) | User who last updated the record |
| UPDATED_ON | DATETIME | Timestamp when the record was last updated |

## Table: BEPRC_APPLICATION_PCR_STEP_1_ANSWER

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_ID | VARCHAR(36) | Foreign key to beprc_application_info table |
| APPLICATION_PCR_STEP_1_QUESTION_ID | VARCHAR(36) | Foreign key to beprc_application_pcr_step_1_question table |
| ANSWER | TINYINT(1) | Boolean answer for PCR question |
| CREATED_BY | VARCHAR(64) | User who created the record |
| CREATED_ON | DATETIME | Timestamp when the record was created |
| UPDATED_BY | VARCHAR(64) | User who last updated the record |
| UPDATED_ON | DATETIME | Timestamp when the record was last updated |

## Table: BEPRC_APPLICATION_PCR_STEP_1_QUESTION

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_TYPE_ID | VARCHAR(36) | Foreign key to beprc_application_type table |
| SERIAL_NUMBER | INT | Sequence number of the question |
| CRITERIA | TEXT | Question criteria for PCR |
| CREATED_BY | VARCHAR(64) | User who created the record |
| CREATED_ON | DATETIME | Timestamp when the record was created |
| UPDATED_BY | VARCHAR(64) | User who last updated the record |
| UPDATED_ON | DATETIME | Timestamp when the record was last updated |

## Table: BEPRC_APPLICATION_PCR_STEP_2_ANSWER

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_ID | VARCHAR(36) | Foreign key to beprc_application_info table |
| REMARK | TEXT | Remark for PCR step 2 |
| PCR_STEP_2_ATTACHMENT_ID | VARCHAR(36) | Foreign key to beprc_attachment table |
| CREATED_BY | VARCHAR(64) | User who created the record |
| CREATED_ON | DATETIME | Timestamp when the record was created |
| UPDATED_BY | VARCHAR(64) | User who last updated the record |
| UPDATED_ON | DATETIME | Timestamp when the record was last updated |

## Table: BEPRC_APPLICATION_PCR_TOR

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_ID | VARCHAR(36) | Foreign key to beprc_application_info table |
| FUND_FROM_BEPRC | VARCHAR(64) | Funding amount from BEPRC |
| PROJECT_START_DATE | DATE | Project start date |
| PROJECT_END_DATE | DATE | Project end date |
| DESCRIPTION | TEXT | Project description |
| CREATED_BY | VARCHAR(64) | User who created the record |
| CREATED_ON | DATETIME | Timestamp when the record was created |
| UPDATED_BY | VARCHAR(64) | User who last updated the record |
| UPDATED_ON | DATETIME | Timestamp when the record was last updated |

## Table: BEPRC_APPLICATION_PROCESS_INFO

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_ID | VARCHAR(36) | Foreign key to beprc_application_info table |
| TYPE | VARCHAR(36) | Type of process |
| ACTION_ID | VARCHAR(36) | Foreign key to beprc_application_action table |
| REMARKS | TEXT | Comments or remarks on the process |
| ATTACHMENT_ID | VARCHAR(36) | Foreign key to beprc_attachment table |
| CREATED_BY | VARCHAR(64) | User who created the record |
| CREATED_ON | DATETIME | Timestamp when the record was created |
| UPDATED_BY | VARCHAR(64) | User who last updated the record |
| UPDATED_ON | DATETIME | Timestamp when the record was last updated |

## Table: BEPRC_APPLICATION_REPORT

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_ID | VARCHAR(36) | Foreign key to beprc_application_info table |
| NAME | VARCHAR(36) | Report name |
| SERIAL_NUMBER | INT | Sequential number of the report |
| TYPE | VARCHAR(36) | Report type (START, NEXT, END) |
| CREATOR | VARCHAR(36) | Creator of the report (SYSTEM, ADMIN) |
| PROCESS_STATUS | VARCHAR(36) | Process status (DRAFT, SHORTFALL, RE_SUBMIT, APPROVED, PENDING) |
| APPLICANT_REMARK | TEXT | Remarks from the applicant |
| APPLICANT_ATTACHMENT_ID | VARCHAR(36) | Foreign key to beprc_attachment table for applicant's attachment |
| ADMIN_REMARK | TEXT | Remarks from the admin |
| ADMIN_ATTACHMENT_ID | VARCHAR(36) | Foreign key to beprc_attachment table for admin's attachment |
| CREATED_BY | VARCHAR(64) | User who created the record |
| CREATED_ON | DATETIME | Timestamp when the record was created |
| UPDATED_BY | VARCHAR(64) | User who last updated the record |
| UPDATED_ON | DATETIME | Timestamp when the record was last updated |

## Table: BEPRC_APPLICATION_RESEARCH_COMPONENT

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_DETAILS_ID | VARCHAR(36) | Foreign key to beprc_application_details table |
| COMPONENT_TYPE | VARCHAR(64) | Name of sub-section (Research Summary with key word) |
| DOC_TYPE | VARCHAR(8) | Document type |
| DETAILS | LONGTEXT | Detailed information about the research component |
| ATTACHMENT_ID | VARCHAR(36) | Foreign key to beprc_attachment table |
| CREATED_BY | VARCHAR(64) | User who created the record |
| CREATED_ON | DATETIME | Timestamp when the record was created |
| UPDATED_BY | VARCHAR(64) | User who last updated the record |
| UPDATED_ON | DATETIME | Timestamp when the record was last updated |

## Table: BEPRC_APPLICATION_RESEARCH_COMPONENT_HISTORY

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the record is deleted (1) or not (0) |
| REVISION | INT | Revision number for tracking history |
| APPLICATION_DETAILS_ID | VARCHAR(36) | Foreign key to beprc_application_details table |
| COMPONENT_TYPE | VARCHAR(64) | Name of sub-section (Research Summary with key word) |
| DOC_TYPE | VARCHAR(8) | Document type |
| DETAILS | TEXT | Detailed information about the research component |
| ATTACHMENT_ID | VARCHAR(36) | Foreign key to beprc_attachment table |
| CREATED_BY | VARCHAR(64) | User who created the record |
| CREATED_ON | DATETIME | Timestamp when the record was created |
| UPDATED_BY | VARCHAR(64) | User who last updated the record |
| UPDATED_ON | DATETIME | Timestamp when the record was last updated |

## Table: BEPRC_APPLICATION_REVIEWER

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_ID | VARCHAR(36) | Foreign key to beprc_application_info table |
| REVIEWER_USER_ID | VARCHAR(36) | Foreign key to beprc_user table |
| ACCEPTED | INT | Review acceptance status (0-nothing, 1-accepted, 2-denied) |
| CHOICE_ON | DATETIME | Timestamp when choice was made |
| IS_PROCESSED | TINYINT(1) | Flag indicating if the review is processed (1) or not (0) |
| PROCESSED_ON | DATETIME | Timestamp when the review was processed |
| REMARKS | TEXT | Reviewer's comments or remarks |
| ATTACHMENT_ID | VARCHAR(36) | Foreign key to beprc_attachment table |
| CREATED_BY | VARCHAR(64) | User who created the record |
| CREATED_ON | DATETIME | Timestamp when the record was created |
| UPDATED_BY | VARCHAR(64) | User who last updated the record |
| UPDATED_ON | DATETIME | Timestamp when the record was last updated |

## Table: BEPRC_APPLICATION_STATUS

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the record is deleted (1) or not (0) |
| TITLE | VARCHAR(512) | Status title (e.g., Submitted, Completed, Save as draft) |
| TAG | VARCHAR(255) | Status tag (e.g., SUBMITTED, COMPLETED, SAVE_AS_DRAFT) |
| CREATED_BY | VARCHAR(64) | User who created the record |
| CREATED_ON | DATETIME | Timestamp when the record was created |
| UPDATED_BY | VARCHAR(64) | User who last updated the record |
| UPDATED_ON | DATETIME | Timestamp when the record was last updated |
