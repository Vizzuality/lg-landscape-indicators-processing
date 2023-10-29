Land, carbon and biodiversity data for supply chain impact calculation
==============================

This repository contains code to generate the land, carbon and bidiversity datasets used for
supply chain impact calculation in LandGriffon (https://landgriffon.com).

These data are available at: [REPOSITORY] and [REPOSITORY]

The methodology is documented at: [CITE]

## Setup

These scripts use Google Earth Engine for comptuation. In order to run these scripts you will
need to set up an Earth Engine [service account](https://developers.google.com/earth-engine/guides/service_account)
and save the credentials.json in the `.env` file as follows:

```
GEE_JSON={"type": "service_account","project_id": "YOUR-EE-PROJECT", ...}
GEE_PROJECT=YOUR-EE-PROJECT
GEE_BUCKET=YOUR-GCS-BUCKET
```

## Notebooks

All scripts are in the notebooks directory.

The data for the `_04_validation_charts` notebook is provided in the repository and can be run
without running the other scripts.
