# NSW COVID-19 Cloud Functions

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
