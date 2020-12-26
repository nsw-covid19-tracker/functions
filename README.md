# NSW COVID-19 Cloud Functions

[![GitHub license](https://img.shields.io/github/license/nsw-covid19-tracker/functions)](https://github.com/nsw-covid19-tracker/functions/blob/main/LICENSE)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/4e901f973d7c4653be00bd1da452a879)](https://www.codacy.com/gh/nsw-covid19-tracker/functions/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=nsw-covid19-tracker/functions&amp;utm_campaign=Badge_Grade)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

This repo contains scripts to fetch NSW COVID-19 data for the [Tracker App](https://www.nswcoviddata.com.au/).

## Getting Started

### Setup Firebase

Create a new project on Firebase.

Then create a service account by going into Settings > Project settings > Service accounts > Firebase Admin SDK > Generate new private key. Rename the file to `keyfile.json` and place it under `functions/`.

### Setup Database

The scripts require Python 3.6+ to run. 

Install the required packages:

    pip3 install -r requirements.txt

Then run the following commands to fetch and add all the data:

    python fetch_data_old.py  # For fetching the outdated data
    python main.py            # For fetching the latest data
