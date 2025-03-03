# BEPRC Database Data Dictionary

## Table: beprc_incubation_application_summary

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the record |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0), defaults to 0 |
| REVISION | int | Revision number of the record, defaults to 0 |
| APPLICATION_ID | varchar(36) | Foreign key referencing beprc_application_info table |
| APPLICATION_DETAILS_ID | varchar(36) | Foreign key referencing beprc_application_details table |
| COVER_PAGE_ID | varchar(36) | Foreign key referencing attachment for cover page |
| TECHNOLOGY_REVIEW_ID | varchar(36) | Foreign key referencing attachment for technology review |
| PROPOSED_PRODUCT_SUMMARY_ID | varchar(36) | Foreign key referencing attachment for proposed product summary |
| INCUBATION_DESCRIPTION_ID | varchar(36) | Foreign key referencing attachment for incubation description |
| STATEMENT_OF_WORK_AND_SCHEDULE_ID | varchar(36) | Foreign key referencing attachment for statement of work and schedule |
| BUDGET_AND_BUDGET_JUSTIFICATION_ID | varchar(36) | Foreign key referencing attachment for budget and budget justification |
| FACILITIES_EQUIPMENT_AND_OTHER_RESOURCES_ID | varchar(36) | Foreign key referencing attachment for facilities, equipment and other resources |
| MARKET_STUDY_ID | varchar(36) | Foreign key referencing attachment for market study |
| ANY_OTHER_RELEVANT_INFORMATION_ID | varchar(36) | Foreign key referencing attachment for any other relevant information |
| ATTACHMENT_DECLARATION_ID | varchar(36) | Foreign key referencing attachment for attachment declaration |
| ORGANIZATION_PDF_ID | varchar(36) | Foreign key referencing attachment for organization PDF |
| PROPOSAL_PDF_ID | varchar(36) | Foreign key referencing attachment for proposal PDF, nullable |
| CREATED_BY | varchar(64) | Username of the person who created the record, nullable |
| CREATED_ON | datetime | Timestamp when the record was created, nullable |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record, nullable |
| UPDATED_ON | datetime | Timestamp when the record was last updated, nullable |

## Table: beprc_innovation_application_summary

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key identifier for the record |
| VERSION | int | Version number of the record, defaults to 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if the record is active (1) or not (0), defaults to 1 |
| IS_DELETED | tinyint(1) | Flag indicating if the record is deleted (1) or not (0), defaults to 0 |
| REVISION | int | Revision number of the record, defaults to 0 |
| APPLICATION_ID | varchar(36) | Foreign key referencing beprc_application_info table |
| APPLICATION_DETAILS_ID | varchar(36) | Foreign key referencing beprc_application_details table |
| COVER_PAGE_ID | varchar(36) | Foreign key referencing attachment for cover page, nullable |
| RESEARCH_BACKGROUND_ID | varchar(36) | Foreign key referencing attachment for research background, nullable |
| RESEARCH_SUMMARY_WITH_KEY_WORDS_ID | varchar(36) | Foreign key referencing attachment for research summary with key words, nullable |
| LITERATURE_REVIEW_ID | varchar(36) | Foreign key referencing attachment for literature review, nullable |
| RESEARCH_DESCRIPTION_ID | varchar(36) | Foreign key referencing attachment for research description, nullable |
| STATEMENT_OF_ACTIVITIES_AND_WORK_PLAN_ID | varchar(36) | Foreign key referencing attachment for statement of activities and work plan, nullable |
| BUDGET_AND_BUDGET_JUSTIFICATION_ID | varchar(36) | Foreign key referencing attachment for budget and budget justification, nullable |
| LIST_OF_FACILITIES_EQUIPMENT_AND_OTHER_RESOURCES_ID | varchar(36) | Foreign key referencing attachment for list of facilities, equipment and other resources, nullable |
| PROCUREMENT_PLAN_ID | varchar(36) | Foreign key referencing attachment for procurement plan, nullable |
| REFERENCE_CITED_ID | varchar(36) | Foreign key referencing attachment for references cited, nullable |
| ATTACHMENT_DECLARATION_ID | varchar(36) | Foreign key referencing attachment for attachment declaration, nullable |
| FACILITIES_ID | varchar(36) | Foreign key referencing attachment for non-lead organization facilities, nullable |
| ORGANIZATION_PDF_ID | varchar(36) | Foreign key referencing attachment for organization PDF |
| PROPOSAL_PDF_ID | varchar(36) | Foreign key referencing attachment for proposal PDF, nullable |
| CREATED_BY | varchar(64) | Username of the person who created the record, nullable |
| CREATED_ON | datetime | Timestamp when the record was created, nullable |
| UPDATED_BY | varchar(64) | Username of the person who last updated the record, nullable |
| UPDATED_ON | datetime | Timestamp when the record was last updated, nullable |
