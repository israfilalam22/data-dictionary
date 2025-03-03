# BEPRC Application Database Data Dictionary

## Table: `DATABASECHANGELOG`
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| ID | VARCHAR(255) | Unique identifier for the database change log entry |
| AUTHOR | VARCHAR(255) | Author of the database change |
| FILENAME | VARCHAR(255) | File name containing the change set |
| DATEEXECUTED | DATETIME | Date and time when the change was executed |
| ORDEREXECUTED | INT | Execution order of the change |
| EXECTYPE | VARCHAR(10) | Type of execution (e.g., EXECUTED, FAILED) |
| MD5SUM | VARCHAR(35) | MD5 checksum of the change set |
| DESCRIPTION | VARCHAR(255) | Description of the change |
| COMMENTS | VARCHAR(255) | Additional comments about the change |
| TAG | VARCHAR(255) | Tag associated with the change |
| LIQUIBASE | VARCHAR(20) | Liquibase version used |
| CONTEXTS | VARCHAR(255) | Contexts for the change |
| LABELS | VARCHAR(255) | Labels for the change |
| DEPLOYMENT_ID | VARCHAR(10) | Deployment identifier |

## Table: `DATABASECHANGELOGLOCK`
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| ID | INT | Primary key identifier for the lock |
| LOCKED | TINYINT(1) | Flag indicating if the database is locked (1) or not (0) |
| LOCKGRANTED | DATETIME | Date and time when the lock was granted |
| LOCKEDBY | VARCHAR(255) | Information about who or what obtained the lock |

## Table: `beprc_address`
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier for the address |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the address is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the address is deleted (1) or not (0) |
| IS_LOCAL_ADDRESS | TINYINT(1) | Flag indicating if it's a local address (1) or not (0) |
| DIVISION_ID | VARCHAR(36) | Foreign key reference to division |
| DISTRICT_ID | VARCHAR(36) | Foreign key reference to district |
| THANA_ID | VARCHAR(36) | Foreign key reference to thana/upazila |
| POST_CODE | VARCHAR(8) | Postal code |
| CITY | VARCHAR(128) | City name |
| STATE_PROVINCE | VARCHAR(128) | State or province name |
| ADDRESS | TEXT | Full address details |
| CREATED_BY | VARCHAR(64) | Username of the creator |
| CREATED_ON | DATETIME | Date and time of creation |
| UPDATED_BY | VARCHAR(64) | Username of the last updater |
| UPDATED_ON | DATETIME | Date and time of last update |

## Table: `beprc_address_history`
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier for the address history |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the address is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the address is deleted (1) or not (0) |
| IS_LOCAL_ADDRESS | TINYINT(1) | Flag indicating if it's a local address (1) or not (0) |
| DIVISION_ID | VARCHAR(36) | Foreign key reference to division |
| DISTRICT_ID | VARCHAR(36) | Foreign key reference to district |
| THANA_ID | VARCHAR(36) | Foreign key reference to thana/upazila |
| POST_CODE | VARCHAR(8) | Postal code |
| CITY | VARCHAR(128) | City name |
| STATE_PROVINCE | VARCHAR(128) | State or province name |
| ADDRESS | VARCHAR(255) | Full address details |
| CREATED_BY | VARCHAR(64) | Username of the creator |
| CREATED_ON | DATETIME | Date and time of creation |
| UPDATED_BY | VARCHAR(64) | Username of the last updater |
| UPDATED_ON | DATETIME | Date and time of last update |

## Table: `beprc_application_action`
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier for the application action |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the action is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the action is deleted (1) or not (0) |
| TITLE | VARCHAR(512) | Title of the action (e.g., Submitted, Completed, Save as draft) |
| STATUS_ID | VARCHAR(36) | Foreign key reference to application status |
| CREATED_BY | VARCHAR(64) | Username of the creator |
| CREATED_ON | DATETIME | Date and time of creation |
| UPDATED_BY | VARCHAR(64) | Username of the last updater |
| UPDATED_ON | DATETIME | Date and time of last update |

## Table: `beprc_application_action_description`
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier for the action description |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the description is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the description is deleted (1) or not (0) |
| APPLICATION_ACTION_ID | VARCHAR(36) | Foreign key reference to application action |
| APPLICATION_TYPE_ID | VARCHAR(36) | Foreign key reference to application type |
| TITLE | VARCHAR(512) | Title of the action description (e.g., INNV, INC, ENT action description) |
| CREATED_BY | VARCHAR(64) | Username of the creator |
| CREATED_ON | DATETIME | Date and time of creation |
| UPDATED_BY | VARCHAR(64) | Username of the last updater |
| UPDATED_ON | DATETIME | Date and time of last update |

## Table: `beprc_application_attachment`
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier for the application attachment |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the attachment is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the attachment is deleted (1) or not (0) |
| APPLICATION_DETAILS_ID | VARCHAR(36) | Foreign key reference to application details |
| ATTACHMENT_DECLARATION_DOC_ID | VARCHAR(36) | Foreign key reference to attachment declaration document |
| ATTACHMENT_ID | VARCHAR(36) | Foreign key reference to attachment |
| CREATED_BY | VARCHAR(64) | Username of the creator |
| CREATED_ON | DATETIME | Date and time of creation |
| UPDATED_BY | VARCHAR(64) | Username of the last updater |
| UPDATED_ON | DATETIME | Date and time of last update |

## Table: `beprc_application_attachment_declaration_doc`
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier for the attachment declaration document |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the document is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the document is deleted (1) or not (0) |
| APPLICATION_TYPE_ID | VARCHAR(36) | Foreign key reference to application type |
| TITLE | VARCHAR(128) | Title of the document |
| TYPE | VARCHAR(16) | Type of document (ATTACHMENT, DECLARATION) |
| IS_COMMON | TINYINT(1) | Flag indicating if it's a common file (1) or not (0) |
| SERIAL_NUMBER | INT | Serial number for ordering |
| ATTACHMENT_ID | VARCHAR(36) | Foreign key reference to attachment |
| CREATED_BY | VARCHAR(64) | Username of the creator |
| CREATED_ON | DATETIME | Date and time of creation |
| UPDATED_BY | VARCHAR(64) | Username of the last updater |
| UPDATED_ON | DATETIME | Date and time of last update |

## Table: `beprc_application_attachment_history`
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier for the attachment history |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the attachment history is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the attachment history is deleted (1) or not (0) |
| REVISION | INT | Revision number |
| APPLICATION_DETAILS_ID | VARCHAR(36) | Foreign key reference to application details |
| ATTACHMENT_DECLARATION_DOC_ID | VARCHAR(36) | Foreign key reference to attachment declaration document |
| ATTACHMENT_ID | VARCHAR(36) | Foreign key reference to attachment |
| CREATED_BY | VARCHAR(64) | Username of the creator |
| CREATED_ON | DATETIME | Date and time of creation |
| UPDATED_BY | VARCHAR(64) | Username of the last updater |
| UPDATED_ON | DATETIME | Date and time of last update |

## Table: `beprc_application_budget`
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier for the application budget |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the budget is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the budget is deleted (1) or not (0) |
| APPLICATION_DETAILS_ID | VARCHAR(36) | Foreign key reference to application details |
| BUDGET_SUMMARY | TEXT | Summary of the budget |
| INN_HONORARIUM_DETAILS | TEXT | Innovation honorarium details |
| INN_EQUIPMENT_PRODUCT_DETAILS | TEXT | Innovation equipment product details |
| INN_TRAVEL_DETAILS | TEXT | Innovation travel details |
| INN_OTHER_DIRECT_DETAILS | TEXT | Innovation other direct details |
| INC_SALARIES_AND_WAGES_DETAILS | TEXT | Incubation salaries and wages details |
| INC_CONSULTATION_DETAILS | TEXT | Incubation consultation details |
| INC_IT_DETAILS | TEXT | Incubation IT details |
| INC_TRAVEL_DETAILS | TEXT | Incubation travel details |
| INC_TECHNOLOGY_TRANSFER_DETAILS | TEXT | Incubation technology transfer details |
| INC_PERMANENT_EQUIPMENT_DETAILS | TEXT | Incubation permanent equipment details |
| INC_CONSUMABLE_DETAILS | TEXT | Incubation consumable details |
| INC_COST_RELATED_TO_MARKET_ANALYSIS_DETAILS | TEXT | Incubation cost related to market analysis details |
| ENT_BRANDING_DETAILS | TEXT | Enterprise branding details |
| ENT_LICENSING_DETAILS | TEXT | Enterprise licensing details |
| ENT_MARKET_STUDY_DETAILS | TEXT | Enterprise market study details |
| ENT_EQUIPMENT_PRODUCT_DETAILS | TEXT | Enterprise equipment product details |
| LAB_DEV_EQUIPMENT_DETAILS | TEXT | Laboratory development equipment details |
| LAB_DEV_MAINTENANCE_DETAILS | TEXT | Laboratory development maintenance details |
| LAB_DEV_RAW_MATERIALS_CONSUMABLES_DETAILS | TEXT | Laboratory development raw materials and consumables details |
| LAB_DEV_BUDGET_FOR_DIRECT_OTHER_DETAILS | TEXT | Laboratory development budget for direct other details |
| PROCUREMENT_PLAN_ATTACHMENT_ID | VARCHAR(36) | Foreign key reference to procurement plan attachment |
| CREATED_BY | VARCHAR(64) | Username of the creator |
| CREATED_ON | DATETIME | Date and time of creation |
| UPDATED_BY | VARCHAR(64) | Username of the last updater |
| UPDATED_ON | DATETIME | Date and time of last update |

## Table: `beprc_application_budget_history`
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier for the budget history |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the budget history is active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the budget history is deleted (1) or not (0) |
| REVISION | INT | Revision number |
| APPLICATION_DETAILS_ID | VARCHAR(36) | Foreign key reference to application details |
| BUDGET_SUMMARY | TEXT | Summary of the budget |
| INN_HONORARIUM_DETAILS | TEXT | Innovation honorarium details |
| INN_EQUIPMENT_PRODUCT_DETAILS | TEXT | Innovation equipment product details |
| INN_TRAVEL_DETAILS | TEXT | Innovation travel details |
| INN_OTHER_DIRECT_DETAILS | TEXT | Innovation other direct details |
| INC_SALARIES_AND_WAGES_DETAILS | TEXT | Incubation salaries and wages details |
| INC_CONSULTATION_DETAILS | TEXT | Incubation consultation details |
| INC_IT_DETAILS | TEXT | Incubation IT details |
| INC_TRAVEL_DETAILS | TEXT | Incubation travel details |
| INC_TECHNOLOGY_TRANSFER_DETAILS | TEXT | Incubation technology transfer details |
| INC_PERMANENT_EQUIPMENT_DETAILS | TEXT | Incubation permanent equipment details |
| INC_CONSUMABLE_DETAILS | TEXT | Incubation consumable details |
| INC_COST_RELATED_TO_MARKET_ANALYSIS_DETAILS | TEXT | Incubation cost related to market analysis details |
| ENT_BRANDING_DETAILS | TEXT | Enterprise branding details |
| ENT_LICENSING_DETAILS | TEXT | Enterprise licensing details |
| ENT_MARKET_STUDY_DETAILS | TEXT | Enterprise market study details |
| ENT_EQUIPMENT_PRODUCT_DETAILS | TEXT | Enterprise equipment product details |
| LAB_DEV_EQUIPMENT_DETAILS | TEXT | Laboratory development equipment details |
| LAB_DEV_MAINTENANCE_DETAILS | TEXT | Laboratory development maintenance details |
| LAB_DEV_RAW_MATERIALS_CONSUMABLES_DETAILS | TEXT | Laboratory development raw materials and consumables details |
| LAB_DEV_BUDGET_FOR_DIRECT_OTHER_DETAILS | TEXT | Laboratory development budget for direct other details |
| PROCUREMENT_PLAN_ATTACHMENT_ID | VARCHAR(36) | Foreign key reference to procurement plan attachment |
| CREATED_BY | VARCHAR(64) | Username of the creator |
| CREATED_ON | DATETIME | Date and time of creation |
| UPDATED_BY | VARCHAR(64) | Username of the last updater |
| UPDATED_ON | DATETIME | Date and time of last update |

## Table: `beprc_application_details`
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | VARCHAR(36) | Primary key identifier for the application details |
| VERSION | INT | Version number for optimistic locking |
| IS_ACTIVE | TINYINT(1) | Flag indicating if the details are active (1) or not (0) |
| IS_DELETED | TINYINT(1) | Flag indicating if the details are deleted (1) or not (0) |
| APPLICATION_ID | VARCHAR(36) | Foreign key reference to application info |
| AWARDEE_