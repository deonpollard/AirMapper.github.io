# Input file formats
For bulk importing information into AirMapper, your file must be in **XLSX** format. You can upload the file directly from your local machine or fetch it from cloud object storage like Amazon S3, Google Cloud Storage (GCS), OneDrive etc.

1. Import a file containing a [list of terms and descriptions](#add-a-new-business-standard-for-glossaries) against which mappings can be done, effectively to create a new standard Glossary
2. Import a file containing a [list of terms](#add-a-new-dataset-for-mapping-terms) to be mapped.
3. Import a file containing a [list of data assets](#add-a-new-dataset-for-mapping-data-assets) to be mapped.


## Add a new Business Standard for Glossaries

### Standard Formatting Rules
- File must be an Excel XLSX file
- File must contain a Worksheet with name of **Glossary**
- Within Glossary Worksheet the first row must include headers as per below

### Mandatory Column Headers

| Header | Subsequent rows should contain |
| -------- | -------- |
| **TermName**  | names of terms   |
| **ShortDescription**  | Term Description   |
| **Package**  | Package Name or Standard Group name applicable to Term   |


## Add a new Dataset for mapping Terms

### Standard Formatting Rules
- File must be an Excel XLSX file
- File must contain a Worksheet with name of **Sheet1**
- Within Sheet1 Worksheet the first row must include headers as per below

### Mandatory Column Headers

| Header | Subsequent rows should contain |
| -------- | -------- |
| **ProjectName**  | names of term to be mapped   |

### Optional Column Headers
The following columns will automatically be created by the import process and subsequently updated by any mapping you perform. By supplying these columns, values can be pre-set.

| Header | Subsequent rows should contain |
| -------- | -------- |
| ShortDescription  | Description of Term  |
| Readme  | Additional supporting information   |
| data_type  | The data_type of the data asset   |
| mapstatus  | Either **not aligned** or **aligning** or **aligned**   |
| Source  | The name of the platform/system or source containing the data asset   |
| exactness | numeric value from 0 to a 100, designating the sureaty of the mapping  |
| Package  | Name of the Target (map-to) Package   |
| Domain  | Name of the Target (map-to) Domain or Entity   |
| TermName  | Standard Term   |
| Category  | Category name   |
| Type  | Either **Term** or **Concept** or **Metric**   |


## Add a new Dataset for mapping Data Assets

### Standard XLSX Formatting Rules
- File must be an Excel XLSX file
- File must contain a Worksheet with name of **Raw**
- Within Raw Worksheet the first row must include headers as per below

### Mandatory Column Headers

| Header | Subsequent rows should contain |
| -------- | -------- |
| **column_name**  | names of data assets you want to map as they exist in your'e environment.   |

### Optional Column Headers
The following columns will automatically be created by the import process and subsequently updated by any mapping you perform. By supplying these columns, values can be pre-set.

| Header | Subsequent rows should contain |
| -------- | -------- |
| table_schema  | In case of a database the table schema name where data asset resides.  In case of other structures the highest level grouping.   |
| table_name  | In case of a database the table name where data asset resides.  In case of other structures the table-like grouping.   |
| data_type  | The data_type of the data asset   |
| mapstatus  | Either **not aligned** or **aligning** or **aligned**   |
| Source  | The name of the platform/system or source containing the data asset   |
| exactness | numeric value from 0 to a 100, designating the sureaty of the mapping  |
| Package  | Name of the Target (map-to) Package   |
| Domain  | Name of the Target (map-to) Domain or Entity   |
| Attribute  | Name of the Target (map-to) Attribute   |

## Example 1
| column_name | 
| -------- | 
| Broker  | 
| Tied Agent  | 
| Claim Reservation  | 

## Example 2
| column_name | table_name | Source |
| -------- | -------- | --------- |
| Broker  | PartyTable | Guidewire |
| Tied Agent  | PartyTable | Guidewire |
| Claim Reservation  | PartyTable | Main Claim System |

