# Importing Data
For bulk importing Data Assets metadata in AirMapper, your file must be in XLSX format. You can upload the file directly from your local machine or fetch it from cloud object storage like Amazon S3, Google Cloud Storage (GCS), or Azure Data Lake Storage (ADLS)

## Standard XLSX Formatting Rules
- File must be an Excel XLSX file
- File must contain a Workbook with name of **Assets**
- In Asset Workbook the first row must include headers as per below

### Mandatory Column Headers

| Header | Subsequent rows should contain |
| -------- | -------- |
| column_name  | exact names of data assets you want to map.   |

### Optional Column Headers
The following columns will automatically be created by the import process and subsequently updated by any mapping you perform. By supplying these columns values will be pre-set and preserved.

| Header | Subsequent rows should contain |
| -------- | -------- |
| table_schema  | In case of a database the table schema name where data asset resides.  In case of other structures the highest level grouping.   |
| table_name  | In case of a database the table name where data asset resides.  In case of other structures the table-like grouping.   |
| data_type  | The data_type of the data asset   |
| mapstatus  | Either **not aligned** or **aligning** or **aligned**   |
| Source  | The name of the platform/system or source containing the data asset   |

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




