# MySQL Schema Data Dictionary

## Table: beprc_user

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key, unique identifier for user |
| VERSION | int | Version number for optimistic locking, default 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if user is active, default 1 |
| IS_DELETED | tinyint(1) | Flag indicating if user is deleted, default 0 |
| IDP_USER_ID | varchar(36) | Identity Provider user ID, unique key |
| IS_ADMIN | tinyint(1) | Flag indicating if user is admin, default 0 |
| IS_BANGLADESHI | tinyint(1) | Flag indicating if user is Bangladeshi, default 1 |
| IS_NRB | tinyint(1) | Flag indicating if user is Non-Resident Bangladeshi, default 0 |
| COUNTRY_ID | varchar(36) | Foreign key to beprc_country table |
| NAME | varchar(128) | Name of the user |
| EMAIL_ADDRESS | varchar(128) | Email address of the user, unique key |
| DATE_OF_BIRTH | date | Date of birth of the user |
| DESIGNATION | varchar(84) | Designation or title of the user |
| PHONE_NUMBER | varchar(36) | Phone number of the user |
| NID | varchar(18) | National ID number of the user |
| ORGANIZATION_NAME | varchar(128) | Name of the organization the user belongs to |
| RESIDENCE | varchar(255) | Residence for foreign nationality users |
| PASSPORT_NUMBER | varchar(24) | Passport number for foreign nationality users |
| PR_NUMBER | varchar(32) | Permanent Resident number for foreign nationality users |
| GENDER_ID | varchar(36) | Foreign key to beprc_gender table |
| ORGANIZATION_ADDRESS_ID | varchar(36) | Foreign key to beprc_address table for organization address |
| PRESENT_ADDRESS_ID | varchar(36) | Foreign key to beprc_address table for present address |
| PERMANENT_ADDRESS_ID | varchar(36) | Foreign key to beprc_address table for permanent address |
| PHOTO_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for profile photo |
| SIGNATURE_ATTACHMENT_ID | varchar(36) | Foreign key to beprc_attachment table for signature image |
| CREATED_BY | varchar(64) | User who created this record |
| CREATED_ON | datetime | Date and time when record was created |
| UPDATED_BY | varchar(64) | User who last updated this record |
| UPDATED_ON | datetime | Date and time when record was last updated |
| IS_IMPORTED | tinyint(1) | Flag indicating if user was imported, default 0 |
| IS_EMAIL_SENT | tinyint(1) | Flag indicating if email was sent to user, default 0 |
| IS_REGISTERED_APPLICANT | tinyint(1) | Flag indicating if user is a registered applicant, default 0 |

## Table: beprc_user_role

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key, unique identifier for user role |
| VERSION | int | Version number for optimistic locking, default 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if user role is active, default 1 |
| IS_DELETED | tinyint(1) | Flag indicating if user role is deleted, default 0 |
| USER_ID | varchar(36) | Foreign key to beprc_user table, part of composite unique key |
| USER_TYPE_ID | varchar(36) | Foreign key to beprc_user_type table, part of composite unique key |
| CREATED_BY | varchar(64) | User who created this record |
| CREATED_ON | datetime | Date and time when record was created |
| UPDATED_BY | varchar(64) | User who last updated this record |
| UPDATED_ON | datetime | Date and time when record was last updated |

## Table: beprc_user_type

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| OID | varchar(36) | Primary key, unique identifier for user type |
| VERSION | int | Version number for optimistic locking, default 0 |
| IS_ACTIVE | tinyint(1) | Flag indicating if user type is active, default 1 |
| IS_DELETED | tinyint(1) | Flag indicating if user type is deleted, default 0 |
| TYPE_NAME | varchar(128) | Name of the user type |
| TITLE | varchar(128) | Display title of the user type |
| CREATED_BY | varchar(64) | User who created this record |
| CREATED_ON | datetime | Date and time when record was created |
| UPDATED_BY | varchar(64) | User who last updated this record |
| UPDATED_ON | datetime | Date and time when record was last updated |
