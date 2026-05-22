# Importing Data
For bulk importing Data Assets metadata in AirMapper, your file must be in XLSX format. You can upload the file directly from your local machine or fetch it from cloud object storage like Amazon S3, Google Cloud Storage (GCS), or Azure Data Lake Storage (ADLS)

## Standard XLSX Formatting Rules
- File must be an Excel XLSX file
- File must contain a Workbook with name of **Assets**
- In Asset Workbook the first row must include headers as per below

### Compulsary Headers

| Heading | Requirement |
| -------- | -------- |
| column_name  | exact names of data assets you want to map.   |


