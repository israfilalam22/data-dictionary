# BEPRC Database Data Dictionary

## Table: beprc_awardee_organization_info

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| ORGANIZATION_NAME | varchar(512) | Name of the awardee organization |
| DISTRICT_ID | varchar(36) | Foreign key to district table |
| THANA_UPAZILA_ID | varchar(36) | Foreign key to thana/upazila table |
| ADDRESS | text | Physical address of the organization |
| POST_CODE | varchar(4) | Postal code of the organization address |
| IDENTIFICATION_NUMBER | varchar(64) | Unique identification number for the organization |
| TAX_PAPER_NUMBER | varchar(64) | Tax identification number for the organization |
| DEPARTMENT | varchar(128) | Department name within the organization |
| ORGANIZATION_LOGO_ATTACHMENT_ID | varchar(36) | Foreign key to the attachment table for the organization logo |
| AW_ORG_URL | varchar(512) | URL of the organization's website |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_awardee_organization_info_history

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| ORGANIZATION_NAME | varchar(128) | Name of the awardee organization |
| DISTRICT_ID | varchar(36) | Foreign key to district table |
| THANA_UPAZILA_ID | varchar(36) | Foreign key to thana/upazila table |
| ADDRESS | varchar(128) | Physical address of the organization |
| POST_CODE | varchar(4) | Postal code of the organization address |
| IDENTIFICATION_NUMBER | varchar(64) | Unique identification number for the organization |
| TAX_PAPER_NUMBER | varchar(64) | Tax identification number for the organization |
| DEPARTMENT | varchar(128) | Department name within the organization |
| ORGANIZATION_LOGO_ATTACHMENT_ID | varchar(36) | Foreign key to the attachment table for the organization logo |
| AW_ORG_URL | varchar(512) | URL of the organization's website |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_budget_type

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_TYPE_ID | varchar(36) | Foreign key to application type table |
| NAME | varchar(128) | Name of the budget type |
| TAG | varchar(128) | Tag or category for the budget type |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_carousel

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| SERIAL_NUMBER | int | Display order for carousel items |
| ATTACHMENT_ID | varchar(36) | Foreign key to attachment table for the carousel image |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_committee_designation

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| TITLE | varchar(255) | Title of the committee designation |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_committee_member

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| USER_ID | varchar(36) | Foreign key to user table |
| COMMITTEE_DESIGNATION_ID | varchar(36) | Foreign key to committee designation table |
| COMMITTEE_TYPE_ID | varchar(36) | Foreign key to committee type table |
| DESIGNATION | varchar(64) | Designation of the committee member |
| PHOTO_ATTACHMENT_ID | varchar(36) | Foreign key to attachment table for the member's photo |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_committee_type

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| APPLICATION_TYPE_ID | varchar(36) | Foreign key to application type table |
| COMMITTEE_NAME | varchar(128) | Name of the committee |
| COMMITTEE_TAG | varchar(64) | Tag or category of the committee (e.g., Screening, Negotiation) |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_country

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| COUNTRY_NAME | varchar(64) | Name of the country |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_district

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| DIVISION_ID | varchar(36) | Foreign key to division table |
| DISTRICT_NAME | varchar(52) | Name of the district |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_division

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| DIVISION_NAME | varchar(128) | Name of the division |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_entrepreneurship_application_summary

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| REVISION | int | Revision number of the application |
| APPLICATION_ID | varchar(36) | Foreign key to application info table |
| APPLICATION_DETAILS_ID | varchar(36) | Foreign key to application details table |
| COVER_PAGE_ID | varchar(36) | Foreign key to attachment table for the cover page |
| EXECUTIVE_SUMMARY_ID | varchar(36) | Foreign key to attachment table for the executive summary |
| MARKET_STUDY_ID | varchar(36) | Foreign key to attachment table for the market study |
| BUSINESS_PLAN_ID | varchar(36) | Foreign key to attachment table for the business plan |
| DETAILED_PRODUCTION_PLAN_ID | varchar(36) | Foreign key to attachment table for the detailed production plan |
| BRANDING_ID | varchar(36) | Foreign key to attachment table for branding documents |
| MASTER_SCHEDULE_ID | varchar(36) | Foreign key to attachment table for the master schedule |
| PROJECT_MANAGEMENT_TEAM_ID | varchar(36) | Foreign key to attachment table for project management team details |
| BUDGET_AND_BUDGET_JUSTIFICATION_ID | varchar(36) | Foreign key to attachment table for budget and justification |
| DESCRIPTION_OF_ASSESSMENT_CRITERIA_ID | varchar(36) | Foreign key to attachment table for assessment criteria description |
| INTELLECTUAL_PROPERTY_ROYALTY_SHARING_AND_LICENSING_ID | varchar(36) | Foreign key to attachment table for IP and licensing details |
| REMARKS_ID | varchar(36) | Foreign key to attachment table for remarks |
| ATTACHMENT_DECLARATION_ID | varchar(36) | Foreign key to attachment table for attachment declarations |
| ORGANIZATION_PDF_ID | varchar(36) | Foreign key to attachment table for organization PDF |
| PROPOSAL_PDF_ID | varchar(36) | Foreign key to attachment table for proposal PDF |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_gender

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| GENDER_TYPE | varchar(8) | Type of gender (e.g., Male, Female, Other) |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_important_links

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| IMAGE_ATTACHMENT_ID | varchar(36) | Foreign key to attachment table for the link image |
| SERIAL_NUMBER | int | Display order for the links |
| TITLE | varchar(128) | Title of the link |
| URL | varchar(64) | URL of the link |
| CREATED_BY | varchar(64) | Username of the person who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_incubation_application_summary

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number of the record |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0) |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0) |
| REVISION | int | Revision number of the application |
| APPLICATION_ID | varchar(36) | Foreign key to application info table |
| APPLICATION_DETAILS_ID | varchar(36) | Foreign key to application details table |
| COVER_PAGE_ID | varchar(36) | Foreign key to attachment table for the cover page |
| TECHNOLOGY_REVIEW