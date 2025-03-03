# BEPRC Database Schema Data Dictionary

## Table: beprc_pm_finance

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number with default value of 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (default: 1) |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (default: 0) |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| PM_BUDGET_TYPE_ID | varchar(36) | Foreign key to beprc_budget_type table |
| PM_QUARTER_ID | varchar(36) | Foreign key to beprc_pm_quarter table |
| EXPENSE_AMOUNT | double | The expense amount |
| PROOF_DOC_ID | varchar(36) | Foreign key to beprc_attachment table for proof document |
| DETAILS | text | Additional details about the finance entry |
| PROCESS_STATUS | varchar(36) | Status of the process (PENDING, REJECTED, ACCEPTED) with default ACCEPTED |
| REVISION | int | Revision number with default value of 0 |
| ADMIN_REMARK | text | Admin's remarks |
| ADMIN_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for admin attachment |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Creation timestamp |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Last update timestamp |

## Table: beprc_pm_finance_v2

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number with default value of 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (default: 1) |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (default: 0) |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| PM_BUDGET_TYPE_ID | varchar(36) | Foreign key to beprc_budget_type table |
| PERIOD_ID | varchar(36) | Foreign key to beprc_pm_period table |
| EXPENSE_AMOUNT | double | The expense amount |
| PROOF_DOC_ID | varchar(36) | Foreign key to beprc_attachment table for proof document |
| DETAILS | text | Additional details about the finance entry |
| PROCESS_STATUS | varchar(36) | Status of the process (PENDING, REJECTED, ACCEPTED) with default PENDING |
| REVISION | int | Revision number with default value of 0 |
| ADMIN_REMARK | text | Admin's remarks |
| ADMIN_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for admin attachment |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Creation timestamp |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Last update timestamp |

## Table: beprc_pm_half_year

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number with default value of 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (default: 1) |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (default: 0) |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| SERIAL_NUMBER | int | Sequential number with default value of 0 |
| START_DATE | date | Start date of the half year |
| START_MONTH | int | Starting month number |
| END_DATE | date | End date of the half year |
| END_MONTH | int | Ending month number |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Creation timestamp |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Last update timestamp |

## Table: beprc_pm_info

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number with default value of 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (default: 1) |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (default: 0) |
| PROJECT_NAME | varchar(127) | Name of the project |
| RESEARCH_AREA_TITLE_ID | varchar(36) | Foreign key to beprc_research_area table |
| SOLICITATION_ID | varchar(36) | Foreign key to beprc_solicitation table |
| LAB_PROGRAM_ID | varchar(36) | Foreign key to beprc_lab_program table |
| APPLICATION_ID | varchar(36) | Foreign key to beprc_application_info table (unique constraint) |
| APPLICATION_TYPE_ID | varchar(36) | Foreign key to beprc_application_type table |
| AWARDED_ON | date | Date when project was awarded |
| INITIATE_DATE | date | Project initiation date |
| START_DATE | date | Project start date |
| PROPOSED_END_DATE | date | Proposed end date for the project |
| END_DATE | date | Actual end date of the project |
| PROGRESS | int | Progress indicator of the project |
| PROJECT_TYPE | varchar(36) | Type of the project |
| PROJECT_STATUS | varchar(36) | Current status of the project |
| DESCRIPTION | varchar(766) | Description of the project |
| PROJECT_FILE | varchar(36) | Foreign key to beprc_attachment table for project file |
| PROPOSAL_PDF_ID | varchar(36) | Foreign key to beprc_attachment table for proposal PDF |
| HAS_TECHNICAL_INFO_UPDATE_PERMISSION | tinyint(1) | Flag for technical info update permission (default: 0) |
| APPLICATION_CREATOR | varchar(64) | Username of application creator |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Creation timestamp |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Last update timestamp |

## Table: beprc_pm_inventory

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number with default value of 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (default: 1) |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (default: 0) |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| DATA | text | Inventory data |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Creation timestamp |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Last update timestamp |

## Table: beprc_pm_member_info

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number with default value of 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (default: 1) |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (default: 0) |
| PROCESS_STATUS | varchar(36) | Status of the process (PENDING, REJECTED, ACCEPTED) |
| REVISION | int | Revision number with default value of 0 |
| ADMIN_REMARK | text | Admin's remarks |
| ADMIN_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for admin attachment |
| PM_INFO_ID | varchar(36) | Foreign key to beprc_pm_info table |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| MEMBER_ROLE_ID | varchar(36) | Foreign key to beprc_member_role table |
| ORGANIZATION_ADDRESS_ID | varchar(36) | Foreign key to beprc_address table for organization address |
| PRESENT_ADDRESS_ID | varchar(36) | Foreign key to beprc_address table for present address |
| PERMANENT_ADDRESS_ID | varchar(36) | Foreign key to beprc_address table for permanent address |
| IS_BANGLADESHI | tinyint(1) | Flag indicating if member is Bangladeshi (default: 1) |
| COUNTRY_ID | varchar(36) | Foreign key to beprc_country table (for foreign nationals) |
| PHOTO_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for profile photo |
| SIGNATURE_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for signature image |
| GENDER_ID | varchar(36) | Foreign key to beprc_gender table |
| IS_NRB | tinyint(1) | Flag indicating if member is Non-Resident Bangladeshi (default: 0) |
| MEMBER_NAME | varchar(128) | Name of the member |
| DESIGNATION | varchar(255) | Designation of the member |
| OTHER_ROLE_NAME | varchar(128) | Name for other role if not in standard roles |
| EMAIL_ADDRESS | varchar(128) | Email address of the member |
| PHONE_NUMBER | varchar(64) | Phone number of the member |
| NID | varchar(18) | National ID number |
| DATE_OF_BIRTH | date | Birth date of the member |
| ORGANIZATION_NAME | varchar(128) | Name of the organization |
| RESIDENCE | varchar(255) | Residence details (for foreign nationals) |
| PASSPORT_NUMBER | varchar(24) | Passport number (for foreign nationals) |
| PR_NUMBER | varchar(32) | Permanent Residence number (for foreign nationals) |
| WORK_EXPERIENCE | varchar(36) | Work experience details |
| EDUCATION | varchar(255) | Educational background |
| RESPONSIBILITY | text | Responsibilities of the member |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Creation timestamp |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Last update timestamp |

## Table: beprc_pm_milestone

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number with default value of 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if record is active (default: 1) |
| IS_DELETED | tinyint(1) | Flag indicating if record is deleted (default: 0) |
| PROCESS_STATUS | varchar(36) | Status of the process (PENDING, REJECTED, ACCEPTED) |
| REVISION | int | Revision number with default value of 0 |
| PM_INFO_ID | varchar(36) | Foreign key to beprc_pm_info table |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| NAME | varchar(255) | Name of the milestone |
| WEIGHT | double | Weight or importance of the milestone |
| START_MONTH | int | Starting month number |
| END_MONTH | int | Ending month number |
| START_DATE | date | Start date of the milestone |
| END_DATE | date | End date of the milestone |
| DESCRIPTION | text | Description of the milestone |
| APPROVAL_DOC_ID | varchar(36) | Foreign key to beprc_attachment table for approval document |
| STATUS | varchar(64) | Status of the milestone |
| IS_PROCESSING | tinyint(1) | Flag indicating if milestone is being processed (default: 0) |
| ADMIN_INFO_REMARK | text | Admin's remarks for information |
| ADMIN_INFO_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for admin info attachment |
| ADMIN_PROGRESS_REMARK | text | Admin's remarks for progress |
| ADMIN_PROGRESS_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for admin progress attachment |
| CREATED_BY | varchar(64) | Username of creator |
| CREATED_ON | datetime | Creation timestamp |
| UPDATED_BY | varchar(64) | Username of last updater |
| UPDATED_ON | datetime | Last update timestamp |
