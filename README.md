# NFHL ETL Pipeline  


**DONE** : 'E'—extract and 'T'-transform so far  
**NEXT** : 'Dockerize' these services + Deploy with Cloud Run


## Summary

- **E**: This repo can use the `Selenium WebDriver protocol`, configured for the Google Chrome web browser, to scrape the National Flood Hazard Layer (NFHL) from the FEMA Map Service Center (MSC) or make requests from the FEMA NFHL API.  
- **T**: Revelant layers are selected from the NFHL data and converted to `GeoJSON` format via `geopandas`.  
- **L**: GeoJSON files will be uploaded to a Google Cloud Storage bucket to further explore, clean and prepare the data for analysis.


## Run Pipeline

1. Navigate to your `~/Downloads` directory in terminal.
2. `git clone https://github.com/derekz3/NFHL_ETL.git pipeline`
3. `cd pipeline`
4. `chmod +x build.sh crawl.sh fema.sh`
5. `./build.sh` to build environment.
6. Enter password when prompted.
7. Method 1: `./crawl.sh` to implement web crawler.
8. Method 2: `./fema.sh` to implement FEMA API requests. 


## Update '`main`' Branch

1. git add -A
2. git commit -m "[*commit message*]"
3. git push origin main