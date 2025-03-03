# BEPRC Database Data Dictionary

## Table: beprc_application_milestone

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the milestone |
| VERSION | int | Version number for optimistic locking |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| APPLICATION_DETAILS_ID | varchar(36) | Foreign key reference to beprc_application_details table |
| NAME | varchar(255) | Name of the milestone |
| WEIGHT | double | Weight value assigned to the milestone |
| START_DATE | date | Start date of the milestone |
| END_DATE | date | End date of the milestone |
| DESCRIPTION | text | Detailed description of the milestone |
| STATUS | varchar(64) | Current status of the milestone |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |
| START_MONTH | int | Start month as an integer value |
| END_MONTH | int | End month as an integer value |

## Table: beprc_application_milestone_history

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the milestone history record |
| VERSION | int | Version number for optimistic locking |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| REVISION | int | Revision number for the history record |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| APPLICATION_DETAILS_ID | varchar(36) | Foreign key reference to beprc_application_details table |
| NAME | varchar(255) | Name of the milestone |
| WEIGHT | double | Weight value assigned to the milestone |
| START_DATE | date | Start date of the milestone |
| END_DATE | date | End date of the milestone |
| START_MONTH | int | Start month as an integer value |
| END_MONTH | int | End month as an integer value |
| DESCRIPTION | text | Detailed description of the milestone |
| STATUS | varchar(64) | Status of the milestone at this point in history |
| CREATED_BY | varchar(64) | Username of the person who created the original record |
| CREATED_ON | datetime | Timestamp when the original record was created |
| UPDATED_BY | varchar(64) | Username of the person who updated the record |
| UPDATED_ON | datetime | Timestamp when the record was updated |

## Table: beprc_application_pcr_step_1_answer

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the PCR step 1 answer |
| VERSION | int | Version number for optimistic locking |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| APPLICATION_PCR_STEP_1_QUESTION_ID | varchar(36) | Foreign key reference to beprc_application_pcr_step_1_question table |
| ANSWER | tinyint(1) | Boolean answer (true/false) for the PCR question |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_application_pcr_step_1_question

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the PCR step 1 question |
| VERSION | int | Version number for optimistic locking |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_TYPE_ID | varchar(36) | Foreign key reference to beprc_application_type table |
| SERIAL_NUMBER | int | Sequence number for ordering questions |
| CRITERIA | text | Question text or criteria for PCR step 1 |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_application_pcr_step_2_answer

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the PCR step 2 answer |
| VERSION | int | Version number for optimistic locking |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| REMARK | text | Remarks or comments for PCR step 2 |
| PCR_STEP_2_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_application_pcr_tor

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the PCR TOR |
| VERSION | int | Version number for optimistic locking |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| FUND_FROM_BEPRC | varchar(64) | Funding amount from BEPRC |
| PROJECT_START_DATE | date | Start date of the project |
| PROJECT_END_DATE | date | End date of the project |
| DESCRIPTION | text | Detailed description of the TOR |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_application_process_info

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the process info |
| VERSION | int | Version number for optimistic locking |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| TYPE | varchar(36) | Type of process information |
| ACTION_ID | varchar(36) | Foreign key reference to beprc_application_action table |
| REMARKS | text | Remarks or comments about the process |
| ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_application_report

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the report |
| VERSION | int | Version number for optimistic locking |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| NAME | varchar(36) | Name of the report |
| SERIAL_NUMBER | int | Sequence number for ordering reports |
| TYPE | varchar(36) | Type of report (START, NEXT, END) |
| CREATOR | varchar(36) | Creator of the report (SYSTEM, ADMIN) |
| PROCESS_STATUS | varchar(36) | Status of the process (DRAFT, SHORTFALL, RE_SUBMIT, APPROVED, PENDING) |
| APPLICANT_REMARK | text | Remarks from the applicant |
| APPLICANT_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for applicant's attachment |
| ADMIN_REMARK | text | Remarks from the admin |
| ADMIN_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for admin's attachment |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_application_research_component

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the research component |
| VERSION | int | Version number for optimistic locking |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_DETAILS_ID | varchar(36) | Foreign key reference to beprc_application_details table |
| COMPONENT_TYPE | varchar(64) | Type of research component (e.g., Research Summary with keywords) |
| DOC_TYPE | varchar(8) | Document type |
| DETAILS | longtext | Detailed content of the research component |
| ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_application_research_component_history

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the research component history |
| VERSION | int | Version number for optimistic locking |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| REVISION | int | Revision number for the history record |
| APPLICATION_DETAILS_ID | varchar(36) | Foreign key reference to beprc_application_details table |
| COMPONENT_TYPE | varchar(64) | Type of research component |
| DOC_TYPE | varchar(8) | Document type |
| DETAILS | text | Detailed content of the research component at this point in history |
| ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table |
| CREATED_BY | varchar(64) | Username of the person who created the original record |
| CREATED_ON | datetime | Timestamp when the original record was created |
| UPDATED_BY | varchar(64) | Username of the person who updated the record |
| UPDATED_ON | datetime | Timestamp when the record was updated |

## Table: beprc_application_reviewer

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the reviewer assignment |
| VERSION | int | Version number for optimistic locking |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| REVIEWER_USER_ID | varchar(36) | Foreign key reference to beprc_user table identifying the reviewer |
| ACCEPTED | int | Status of reviewer acceptance (0-nothing, 1-accepted, 2-denied) |
| CHOICE_ON | datetime | Timestamp when the reviewer made their choice |
| IS_PROCESSED | tinyint(1) | Flag indicating if the review has been processed |
| PROCESSED_ON | datetime | Timestamp when the review was processed |
| REMARKS | text | Remarks or comments from the reviewer |
| ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_application_status

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the application status |
| VERSION | int | Version number for optimistic locking |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| TITLE | varchar(512) | Display title for the status (e.g., "Submitted", "Completed", "Save as draft") |
| TAG | varchar(255) | Status identifier (e.g., "SUBMITTED", "COMPLETED", "SAVE_AS_DRAFT") |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_application_status_description

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the status description |
| VERSION | int | Version number for optimistic locking |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1