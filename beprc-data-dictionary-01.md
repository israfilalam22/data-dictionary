# BEPRC Database Schema Data Dictionary

## Table: beprc_application_details

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the application details |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0), defaults to 0 |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| AWARDEE_ORGANIZATION_INFO_ID | varchar(36) | Foreign key reference to beprc_awardee_organization_info table |
| RESEARCH_PRIMARY_LOCATION_ID | varchar(36) | Foreign key reference to beprc_address table for research location |
| ORGANIZATION_TYPE | varchar(36) | Type of organization (lead or non-lead) |
| NON_LEAD_ORGANIZATION_SERIAL | int | Serial number for non-lead organizations, defaults to 0 |
| PROPOSED_TITLE | varchar(256) | Title of the proposed research/application |
| TOTAL_DURATION | int | Total duration of the project, defaults to 0 |
| TOTAL_BUDGET | double | Total budget for the project |
| LABORATORY_ORGANIZATION_TYPE | varchar(64) | Type of laboratory organization |
| LABORATORY_TYPE | varchar(48) | Type of laboratory |
| LABORATORY_LOCATION | text | Location description of the laboratory |
| LABORATORY_NAME | varchar(255) | Name of the laboratory |
| CREATED_BY | varchar(64) | Username of person who created the record |
| CREATED_ON | datetime | Date and time when the record was created |
| UPDATED_BY | varchar(64) | Username of person who last updated the record |
| UPDATED_ON | datetime | Date and time when the record was last updated |

## Table: beprc_application_details_history

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the history record |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0), defaults to 0 |
| REVISION | int | Revision number of the history record, defaults to 0 |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| AWARDEE_ORGANIZATION_INFO_HISTORY_ID | varchar(36) | Foreign key reference to beprc_awardee_organization_info_history table |
| RESEARCH_PRIMARY_LOCATION_HISTORY_ID | varchar(36) | Foreign key reference to beprc_address_history table |
| ORGANIZATION_TYPE | varchar(36) | Type of organization (lead or non-lead) |
| NON_LEAD_ORGANIZATION_SERIAL | int | Serial number for non-lead organizations, defaults to 0 |
| PROPOSED_TITLE | varchar(256) | Title of the proposed research/application |
| TOTAL_DURATION | int | Total duration of the project, defaults to 0 |
| TOTAL_BUDGET | double | Total budget for the project |
| LABORATORY_ORGANIZATION_TYPE | varchar(64) | Type of laboratory organization |
| LABORATORY_TYPE | varchar(48) | Type of laboratory |
| LABORATORY_LOCATION | text | Location description of the laboratory |
| LABORATORY_NAME | varchar(255) | Name of the laboratory |
| CREATED_BY | varchar(64) | Username of person who created the record |
| CREATED_ON | datetime | Date and time when the record was created |
| UPDATED_BY | varchar(64) | Username of person who last updated the record |
| UPDATED_ON | datetime | Date and time when the record was last updated |

## Table: beprc_application_info

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the application information |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0), defaults to 0 |
| APPLICATION_TRACKING_NUMBER | varchar(64) | Tracking number for the application |
| APPLICATION_TYPE_ID | varchar(36) | Foreign key reference to beprc_application_type table |
| APPLICATION_STATUS_ID | varchar(36) | Foreign key reference to beprc_application_status table |
| SOLICITATION_ID | varchar(36) | Foreign key reference to beprc_solicitation table |
| LAB_PROGRAM_ID | varchar(36) | Foreign key reference to beprc_lab_program table |
| IS_INDIVIDUAL_PROPOSAL | tinyint(1) | Flag indicating if this is an individual proposal (1) or not (0), defaults to 1 |
| NUMBER_OF_NON_LEAD_ORGANIZATION | int | Number of non-lead organizations involved, defaults to 1 |
| SUBMITTED_ON | datetime | Date and time when the application was submitted |
| SC_SUBMITTED_ON | datetime | Date and time when submitted to SC (possibly Scientific Committee) |
| RVW_SUBMITTED_ON | datetime | Date and time when submitted for review |
| REVISION | int | Revision number of the application, defaults to 0 |
| CREATED_BY | varchar(64) | Username of person who created the record |
| CREATED_ON | datetime | Date and time when the record was created |
| UPDATED_BY | varchar(64) | Username of person who last updated the record |
| UPDATED_ON | datetime | Date and time when the record was last updated |
| AWARDED_ON | date | Date when the application was awarded |
| APPLICATION_STATUS_NAME | varchar(512) | Name of the application status |
| REPORT_ID | varchar(36) | Foreign key reference to beprc_application_report table |
| REPORT_STATUS | varchar(36) | Status of the report (DRAFT, SHORTFALL, RE_SUBMIT, APPROVED, PENDING) |
| REPORT_SUBMITTED_ON | date | Date when the report was submitted |
| PCR_REPORT_STATUS | varchar(36) | Status of the PCR report (DRAFT, SHORTFALL, RE_SUBMIT, APPROVED, PENDING) |
| ALL_PCR_CRITERIA_FULFILLED | tinyint(1) | Flag indicating if all PCR criteria are fulfilled |
| PRC_REPORT_SUBMITTED_ON | date | Date when the PRC report was submitted |
| LAST_REMARK | text | Last remark on the application |
| LAST_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for the last attachment |
| PCR_ADMIN_REMARK | text | Administrative remark for PCR |
| PCR_ADMIN_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for PCR admin attachment |
| AWARDED_REMARK | text | Remark when awarded |
| AWARDED_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for award attachment |
| NUMBER_OF_REVIEWER | int | Number of reviewers assigned, defaults to 0 |
| IS_IMPORTED | tinyint(1) | Flag indicating if the record was imported (1) or not (0), defaults to 0 |

## Table: beprc_application_member_info

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the member information |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0), defaults to 0 |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| APPLICATION_DETAILS_ID | varchar(36) | Foreign key reference to beprc_application_details table |
| MEMBER_ROLE_ID | varchar(36) | Foreign key reference to beprc_member_role table |
| ORGANIZATION_ADDRESS_ID | varchar(36) | Foreign key reference to beprc_address table for organization address |
| PRESENT_ADDRESS_ID | varchar(36) | Foreign key reference to beprc_address table for present address |
| PERMANENT_ADDRESS_ID | varchar(36) | Foreign key reference to beprc_address table for permanent address |
| IS_BANGLADESHI | tinyint(1) | Flag indicating if the member is Bangladeshi (1) or not (0), defaults to 1 |
| COUNTRY_ID | varchar(36) | Foreign key reference to beprc_country table for foreign nationality |
| PHOTO_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for profile photo |
| SIGNATURE_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for signature |
| GENDER_ID | varchar(36) | Foreign key reference to beprc_gender table |
| IS_NRB | tinyint(1) | Flag indicating if the member is a Non-Resident Bangladeshi (1) or not (0), defaults to 0 |
| MEMBER_NAME | varchar(128) | Name of the member |
| DESIGNATION | varchar(255) | Designation/title of the member |
| OTHER_ROLE_NAME | varchar(128) | Name of other role if applicable |
| EMAIL_ADDRESS | varchar(128) | Email address of the member |
| PHONE_NUMBER | varchar(64) | Phone number of the member |
| NID | varchar(18) | National ID number of the member |
| DATE_OF_BIRTH | date | Date of birth of the member |
| ORGANIZATION_NAME | varchar(128) | Name of the organization the member belongs to |
| RESIDENCE | varchar(255) | Residence information for foreign nationals |
| PASSPORT_NUMBER | varchar(24) | Passport number for foreign nationals |
| PR_NUMBER | varchar(32) | Permanent Residence number for foreign nationals |
| WORK_EXPERIENCE | varchar(36) | Work experience of the member |
| EDUCATION | varchar(255) | Educational background of the member |
| RESPONSIBILITY | text | Responsibilities of the member in the project |
| CREATED_BY | varchar(64) | Username of person who created the record |
| CREATED_ON | datetime | Date and time when the record was created |
| UPDATED_BY | varchar(64) | Username of person who last updated the record |
| UPDATED_ON | datetime | Date and time when the record was last updated |

## Table: beprc_application_member_info_history

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the history record |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0), defaults to 0 |
| REVISION | int | Revision number of the history record, defaults to 0 |
| APPLICATION_ID | varchar(36) | Foreign key reference to beprc_application_info table |
| APPLICATION_DETAILS_ID | varchar(36) | Foreign key reference to beprc_application_details table |
| MEMBER_ROLE_ID | varchar(36) | Foreign key reference to beprc_member_role table |
| ORGANIZATION_ADDRESS_HISTORY_ID | varchar(36) | Foreign key reference to beprc_address_history table for organization address |
| PRESENT_ADDRESS_HISTORY_ID | varchar(36) | Foreign key reference to beprc_address_history table for present address |
| PERMANENT_ADDRESS_HISTORY_ID | varchar(36) | Foreign key reference to beprc_address_history table for permanent address |
| IS_BANGLADESHI | tinyint(1) | Flag indicating if the member is Bangladeshi (1) or not (0), defaults to 1 |
| COUNTRY_ID | varchar(36) | Foreign key reference to beprc_country table for foreign nationality |
| PHOTO_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for profile photo |
| SIGNATURE_ATTACHMENT_ID | varchar(36) | Foreign key reference to beprc_attachment table for signature |
| GENDER_ID | varchar(36) | Foreign key reference to beprc_gender table |
| IS_NRB | tinyint(1) | Flag indicating if the member is a Non-Resident Bangladeshi (1) or not (0), defaults to 0 |
| MEMBER_NAME | varchar(128) | Name of the member |
| DESIGNATION | varchar(255) | Designation/title of the member |
| OTHER_ROLE_NAME | varchar(128) | Name of other role if applicable |
| EMAIL_ADDRESS | varchar(128) | Email address of the member |
| PHONE_NUMBER | varchar(64) | Phone number of the member |
| NID | varchar(18) | National ID number of the member |
| DATE_OF_BIRTH | date | Date of birth of the member |
| ORGANIZATION_NAME | varchar(128) | Name of the organization the member belongs to |
| RESIDENCE | varchar(255) | Residence information for foreign nationals |
| PASSPORT_NUMBER | varchar(24) | Passport number for foreign nationals |
| PR_NUMBER | varchar(32) | Permanent Residence number for foreign nationals |
| WORK_EXPERIENCE | varchar(36) | Work experience of the member |
| EDUCATION | varchar(255) | Educational background of the member |
| RESPONSIBILITY | text | Responsibilities of the member in the project |
| CREATED_BY | varchar(64) | Username of person who created the record |
| CREATED_ON | datetime | Date and time when the record was created |
| UPDATED_BY | varchar(64) | Username of person who last updated the record |
| UPDATED_ON | datetime | Date and time when the record was last updated |
