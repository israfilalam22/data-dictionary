# BEPRC Database Schema Data Dictionary

## Table: beprc_report_info_v2

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key, unique identifier for report |
| VERSION | int | Version tracking number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (1) or not (0), defaults to 0 |
| PM_INFO_ID | varchar(36) | Foreign key reference to beprc_pm_info table, PM Info Id |
| PM_DETAILS_ID | varchar(36) | Foreign key reference to beprc_pm_details table |
| REPORT_TYPE | varchar(64) | Type of report |
| PERIOD_ID | varchar(36) | Foreign key reference to beprc_pm_period table, Period Id |
| CREATOR | varchar(36) | Creator of the report (e.g., SYSTEM, ADMIN) |
| ADMIN_REPORT_SAMPLE_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for sample attachments |
| NAME | varchar(255) | Name of the report |
| DUE_FROM | date | Start date when report is due |
| DUE_ON | date | End date when report is due |
| REPORT_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for report attachments |
| SUBMITTED_ON | date | Date when report was submitted |
| DESCRIPTION | text | Detailed description of the report |
| PROCESS_STATUS | varchar(36) | Status of the report (e.g., PENDING, REJECTED, ACCEPTED) |
| REVISION | int | Revision number, defaults to 0 |
| ADMIN_REMARK | text | Remarks added by administrator |
| ADMIN_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for admin attachments |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Date and time when record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Date and time when record was last updated |

## Table: beprc_research_area

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key, unique identifier for research area |
| VERSION | int | Version tracking number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (1) or not (0), defaults to 0 |
| TITLE | varchar(255) | Title of the research area |
| APPLICATION_TYPE_ID | varchar(36) | Foreign key reference to beprc_application_type table |
| BDG_FOR_HNR_PRC | int | Budget for honorarium percentage, defaults to 0 |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Date and time when record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Date and time when record was last updated |

## Table: beprc_reviewer

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key, unique identifier for reviewer |
| VERSION | int | Version tracking number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (1) or not (0), defaults to 0 |
| USER_ID | varchar(36) | Foreign key reference to beprc_user table |
| APPLICATION_TYPE_ID | varchar(36) | Foreign key reference to beprc_application_type table |
| PHOTO_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for profile photo |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Date and time when record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Date and time when record was last updated |

## Table: beprc_reviewer_answer

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key, unique identifier for reviewer answer |
| VERSION | int | Version tracking number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (1) or not (0), defaults to 0 |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| REVIEWER_QUESTION_ID | varchar(36) | Foreign key reference to beprc_reviewer_question table |
| SERIAL_NUMBER | int | Serial number for ordering |
| CRITERIA | text | Questions for reviewer |
| POINT | int | Maximum marks available |
| STEP_NO | int | Step number in the review process |
| STEP_NAME | varchar(64) | Name of the step in the review process |
| ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table |
| REVIEWER_USER_ID | varchar(36) | Foreign key reference to beprc_user table for reviewer |
| REMARKS | text | Comments or remarks by the reviewer |
| SCORE | double | Marks obtained |
| TOTAL_SCORE | int | Total score for a step |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Date and time when record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Date and time when record was last updated |

## Table: beprc_reviewer_question

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key, unique identifier for reviewer question |
| VERSION | int | Version tracking number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (1) or not (0), defaults to 0 |
| APPLICATION_TYPE_ID | varchar(36) | Foreign key reference to beprc_application_type table |
| SERIAL_NUMBER | int | Serial number for ordering |
| CRITERIA | text | Questions for reviewer |
| POINT | int | Maximum marks available |
| STEP_NO | int | Step number in the review process |
| STEP_NAME | varchar(64) | Name of the step in the review process |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Date and time when record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Date and time when record was last updated |

## Table: beprc_reviewer_research_area

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key, unique identifier for reviewer research area |
| VERSION | int | Version tracking number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (1) or not (0), defaults to 0 |
| REVIEWER_ID | varchar(36) | Foreign key reference to beprc_reviewer table |
| USER_ID | varchar(36) | Foreign key reference to beprc_user table |
| RESEARCH_AREA_TITLE_ID | varchar(36) | Foreign key reference to beprc_research_area table |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Date and time when record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Date and time when record was last updated |

## Table: beprc_scc_answer

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key, unique identifier for screening committee answer |
| VERSION | int | Version tracking number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (1) or not (0), defaults to 0 |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| SCREENING_COMMITTEE_QUESTION_ID | varchar(36) | Foreign key reference to beprc_scc_question table |
| SERIAL_NUMBER | int | Serial number for ordering |
| CRITERIA | text | Question criteria |
| ANSWER | tinyint(1) | Boolean answer (yes/no) |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Date and time when record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Date and time when record was last updated |

## Table: beprc_scc_question

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key, unique identifier for screening committee question |
| VERSION | int | Version tracking number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (1) or not (0), defaults to 0 |
| APPLICATION_TYPE_ID | varchar(36) | Foreign key reference to beprc_application_type table |
| SERIAL_NUMBER | int | Serial number for ordering |
| CRITERIA | text | Questions for screening committee |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Date and time when record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Date and time when record was last updated |

## Table: beprc_solicitation

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key, unique identifier for solicitation |
| VERSION | int | Version tracking number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (1) or not (0), defaults to 0 |
| SOURCE_TYPE | int | Source type: BEPRC (0) or OTHER (1), defaults to 0 |
| SOURCE_NAME | varchar(255) | Name of the source |
| TYPE | int | Type: SOLICITATION (0), UNSOLICITATION (1), FROM_PI (2) |
| USER_ID | varchar(36) | Foreign key reference to beprc_user table |
| RESEARCH_AREA_TITLE_ID | varchar(36) | Foreign key reference to beprc_research_area table |
| APPLICATION_TYPE_ID | varchar(36) | Foreign key reference to beprc_application_type table |
| SOLICITATION_CODE | varchar(64) | Code for the solicitation |
| SERIAL_NUMBER | int | Serial number for ordering |
| PROJECT_DURATION | int | Duration of the project in months |
| PROJECT_AMOUNT | double | Budget amount for the project |
| PROGRAM_TITLE | text | Title of the program |
| SYNOPSIS_OF_PROGRAM | text | Synopsis or summary of the program |
| RESEARCH_FOCUS_AREA | text | Specific focus area for research |
| IS_OPEN_DEADLINE | tinyint(1) | Flag indicating if deadline is open (1) or fixed (0) |
| DEADLINE | date | Deadline date for submissions |
| PUBLISHED_DATE | date | Date when solicitation was published |
| ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for attachments |
| THUMBNAIL_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for thumbnail |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Date and time when record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Date and time when record was last updated |

## Table: beprc_solicitation_organization

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key, unique identifier for solicitation organization |
| VERSION | int | Version tracking number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (1) or not (0), defaults to 0 |
| SOLICITATION_ID | varchar(36) | Foreign key reference to beprc_solicitation table |
| USER_ID | varchar(36) | Foreign key reference to beprc_user table, organization e-mail address |
| ORGANIZATION_NAME | varchar(128) | Name of the organization |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Date and time when record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Date and time when record was last updated |

## Table: beprc_solicitation_pcr_application

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key, unique identifier for solicitation PCR application |
| VERSION | int | Version tracking number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (1) or not (0), defaults to 0 |
| SOLICITATION_ID | varchar(36) | Foreign key reference to beprc_solicitation table |
| RESEARCH_AREA_TITLE_ID | varchar(36) | Foreign key reference to beprc_research_area table |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Date and time when record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Date and time when record was last updated |

## Table: beprc_system_update_history

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key, unique identifier for system update history |
| VERSION | int | Version tracking number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (1) or not (0), defaults to 0 |
| LAST_UPDATED_ON | datetime | Date and time of last system update |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Date and time when record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Date and time when record was last updated |

## Table: beprc_thana_upazila

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key, unique identifier for thana/upazila |
| VERSION | int | Version tracking number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (1) or not (0), defaults to 0 |
| DISTRICT_ID | varchar(36) | Foreign key reference to beprc_district table |
| THANA_UPAZILA_NAME | varchar(52) | Name of the thana or upazila |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Date and time when record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Date and time when record was last updated |
