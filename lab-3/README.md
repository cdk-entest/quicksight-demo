---
title: caculated fileds
author: haimtran
---

## Step 1. Create Manifest Files

Manifest file for sale data

```json
{
  "fileLocations": [
    {
      "URIs": ["s3://tcb-quicksight-demo/SaaS-Sales.csv"]
    }
  ],
  "globalUploadSettings": {
    "format": "CSV",
    "delimiter": ",",
    "containsHeader": "true"
  }
}
```

Manifest file for calenda data

```json
{
  "fileLocations": [
    {
      "URIs": ["s3://tcb-quicksight-demo/FiscalCalendar.csv"]
    }
  ],
  "globalUploadSettings": {
    "format": "CSV",
    "delimiter": ",",
    "textqualifier": "\"",
    "containsHeader": "true"
  }
}
```

## Step 2 Load Datasets to SPICE

Load datasets using manifest.json file

```
s3://tcb-quicksight-demo/quicksight-fiscal-manifest.json
```

and

```
s3://tcb-quicksight-demo/quicksight-manifest.json
```

## Step 3 Prepare Data in QuickSight

- Duplicate
- Join by DateKey
- Exclude some columns
- Create a folder for some fields
