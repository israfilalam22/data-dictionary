# BEPRC Database Schema Data Dictionary

## Table: beprc_pm_allocation_v2

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| PM_BUDGET_TYPE_ID | varchar(36) | Foreign key to beprc_budget_type table |
| PERIOD_ID | varchar(36) | Foreign key to beprc_pm_period table, Period Id |
| ALLOCATION_AMOUNT | double | The allocated budget amount |
| DETAILS | text | Detailed information about the allocation |
| PROCESS_STATUS | varchar(36) | Status of the process: PENDING, REJECTED, ACCEPTED, defaults to 'PENDING' |
| REVISION | int | Revision number, defaults to 0 |
| ADMIN_REMARK | text | Administrative remarks |
| ADMIN_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for admin attachments |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_pm_annual_year

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| SERIAL_NUMBER | int | Sequential number, defaults to 0 |
| START_DATE | date | Start date of the annual year |
| START_MONTH | int | Starting month number |
| END_DATE | date | End date of the annual year |
| END_MONTH | int | Ending month number |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_pm_budget

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| REVISION | int | Revision number, defaults to 0 |
| PROCESS_STATUS | varchar(36) | Status of the process: PENDING, REJECTED, ACCEPTED |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| BUDGET_SUMMARY | text | Summary of the budget |
| INN_HONORARIUM_DETAILS | text | Details of innovation honorarium |
| INN_EQUIPMENT_PRODUCT_DETAILS | text | Details of innovation equipment and products |
| INN_TRAVEL_DETAILS | text | Details of innovation travel expenses |
| INN_OTHER_DIRECT_DETAILS | text | Details of other direct innovation expenses |
| INC_SALARIES_AND_WAGES_DETAILS | text | Details of incubation salaries and wages |
| INC_CONSULTATION_DETAILS | text | Details of incubation consultation expenses |
| INC_IT_DETAILS | text | Details of incubation IT expenses |
| INC_TRAVEL_DETAILS | text | Details of incubation travel expenses |
| INC_TECHNOLOGY_TRANSFER_DETAILS | text | Details of incubation technology transfer expenses |
| INC_PERMANENT_EQUIPMENT_DETAILS | text | Details of incubation permanent equipment expenses |
| INC_CONSUMABLE_DETAILS | text | Details of incubation consumable expenses |
| INC_COST_RELATED_TO_MARKET_ANALYSIS_DETAILS | text | Details of incubation market analysis expenses |
| ENT_BRANDING_DETAILS | text | Details of enterprise branding expenses |
| ENT_LICENSING_DETAILS | text | Details of enterprise licensing expenses |
| ENT_MARKET_STUDY_DETAILS | text | Details of enterprise market study expenses |
| ENT_EQUIPMENT_PRODUCT_DETAILS | text | Details of enterprise equipment and product expenses |
| LAB_DEV_EQUIPMENT_DETAILS | text | Details of laboratory development equipment expenses |
| LAB_DEV_MAINTENANCE_DETAILS | text | Details of laboratory development maintenance expenses |
| LAB_DEV_RAW_MATERIALS_CONSUMABLES_DETAILS | text | Details of laboratory development raw materials and consumables expenses |
| LAB_DEV_BUDGET_FOR_DIRECT_OTHER_DETAILS | text | Details of other direct laboratory development expenses |
| PROCUREMENT_PLAN_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for procurement plan |
| ADMIN_REMARK | text | Administrative remarks |
| ADMIN_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for admin attachments |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_pm_budget_history

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| REVISION | int | Revision number, defaults to 0 |
| PROCESS_STATUS | varchar(36) | Status of the process: PENDING, REJECTED, ACCEPTED |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| BUDGET_SUMMARY | text | Summary of the budget |
| INN_HONORARIUM_DETAILS | text | Historical details of innovation honorarium |
| INN_EQUIPMENT_PRODUCT_DETAILS | text | Historical details of innovation equipment and products |
| INN_TRAVEL_DETAILS | text | Historical details of innovation travel expenses |
| INN_OTHER_DIRECT_DETAILS | text | Historical details of other direct innovation expenses |
| INC_SALARIES_AND_WAGES_DETAILS | text | Historical details of incubation salaries and wages |
| INC_CONSULTATION_DETAILS | text | Historical details of incubation consultation expenses |
| INC_IT_DETAILS | text | Historical details of incubation IT expenses |
| INC_TRAVEL_DETAILS | text | Historical details of incubation travel expenses |
| INC_TECHNOLOGY_TRANSFER_DETAILS | text | Historical details of incubation technology transfer expenses |
| INC_PERMANENT_EQUIPMENT_DETAILS | text | Historical details of incubation permanent equipment expenses |
| INC_CONSUMABLE_DETAILS | text | Historical details of incubation consumable expenses |
| INC_COST_RELATED_TO_MARKET_ANALYSIS_DETAILS | text | Historical details of incubation market analysis expenses |
| ENT_BRANDING_DETAILS | text | Historical details of enterprise branding expenses |
| ENT_LICENSING_DETAILS | text | Historical details of enterprise licensing expenses |
| ENT_MARKET_STUDY_DETAILS | text | Historical details of enterprise market study expenses |
| ENT_EQUIPMENT_PRODUCT_DETAILS | text | Historical details of enterprise equipment and product expenses |
| LAB_DEV_EQUIPMENT_DETAILS | text | Historical details of laboratory development equipment expenses |
| LAB_DEV_MAINTENANCE_DETAILS | text | Historical details of laboratory development maintenance expenses |
| LAB_DEV_RAW_MATERIALS_CONSUMABLES_DETAILS | text | Historical details of laboratory development raw materials and consumables expenses |
| LAB_DEV_BUDGET_FOR_DIRECT_OTHER_DETAILS | text | Historical details of other direct laboratory development expenses |
| PROCUREMENT_PLAN_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for procurement plan |
| ADMIN_REMARK | text | Administrative remarks |
| ADMIN_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for admin attachments |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_pm_budget_increase

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| BUDGET | double | The increased budget amount |
| IS_READONLY | tinyint(1) | Flag indicating if the record is read-only, defaults to 0 |
| PROOF_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for proof documents |
| APPROVED_ON | date | Date when the budget increase was approved |
| SERIAL_NUMBER | int | Sequential number, defaults to 0 |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_pm_committee_member

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| PM_INFO_ID | varchar(36) | Foreign key to beprc_pm_info table, PM Info Id |
| USER_ID | varchar(36) | Foreign key to beprc_user table |
| COMMITTEE_DESIGNATION_ID | varchar(36) | Foreign key to beprc_committee_designation table |
| COMMITTEE_TYPE_ID | varchar(36) | Foreign key to beprc_committee_type table |
| DESIGNATION | varchar(64) | Member's designation in the committee |
| PHOTO_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table, Profile photo for Committee Member |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_pm_details

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| PM_INFO_ID | varchar(36) | Foreign key to beprc_pm_info table, PM Info Id |
| APPLICATION_ID | varchar(36) | Foreign key to beprc_application_info table |
| APPLICATION_DETAILS_ID | varchar(36) | Foreign key to beprc_application_details table |
| APPLICATION_TYPE_ID | varchar(36) | Foreign key to beprc_application_type table |
| ORGANIZATION_TYPE | varchar(36) | Type of organization: lead, non-lead |
| NON_LEAD_ORGANIZATION_SERIAL | int | Serial number for non-lead organizations, defaults to 0 |
| TOTAL_DURATION | int | Total duration in months, defaults to 0 |
| TOTAL_BUDGET | double | Total budget amount |
| HAS_BUDGET_INFO_UPDATE_PERMISSION | tinyint(1) | Flag indicating if budget info can be updated, defaults to 0 |
| HAS_TECHNICAL_INFO_UPDATE_PERMISSION | tinyint(1) | Flag indicating if technical info can be updated, defaults to 0 |
| HAS_FINANCIAL_INFO_UPDATE_PERMISSION | tinyint(1) | Flag indicating if financial info can be updated, defaults to 0 |
| HAS_MEMBER_INFO_UPDATE_PERMISSION | tinyint(1) | Flag indicating if member info can be updated, defaults to 0 |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_pm_disbursement

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| PM_DETAILS_ID | varchar(36) | Foreign key to beprc_pm_details table |
| DSB_AMOUNT | double | Disbursement amount |
| DSB_REMARK | text | Remarks about the disbursement |
| DSB_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for disbursement documents |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |

## Table: beprc_pm_duration

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier |
| VERSION | int | Version number, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active, defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted, defaults to 0 |
| PM_INFO_ID | varchar(36) | Foreign key to beprc_pm_info table, PM Info Id |
| SERIAL_NUMBER | int | Sequential number, defaults to 0 |
| START_DATE | date | Start date of the project duration |
| EXTENDED_FROM | date | Original end date before extension |
| END_DATE | date | End date of the project duration |
| APPROVED_DOC_ID | varchar(36) | Foreign key to beprc_attachment table for approved documents |
| IS_READONLY | tinyint(1) | Flag indicating if the record is read-only, defaults to 0 |
| PROCESS_STATUS | varchar(36) | Status of the process: PENDING, REJECTED, ACCEPTED |
| REVISION | int | Revision number, defaults to 0 |
| ADMIN_REMARK | text | Administrative remarks |
| ADMIN_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for admin attachments |
| CREATED_BY | varchar(64) | User who created the record |
| CREATED_ON | datetime | Timestamp when the record was created |
| UPDATED_BY | varchar(64) | User who last updated the record |
| UPDATED_ON | datetime | Timestamp when the record was last updated |
