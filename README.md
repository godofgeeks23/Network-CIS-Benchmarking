# Network-CIS-Benchmarking
CIS bench marking and interactive dashboard to analyse security status of your network

# Installation and Usage - 

## Requirements - 

For host machines - 
* Python 3

For server machine - 
* Node
* Docker

## Running -

### Setup the ElasticSearch Cluster + Kibana server

```
docker compose up
```

### Run ingestor

In single core mode as - 

```
node ingestor.js
```

or in Multicore mode by using - 

```
npm i -g pm2
pm2 start ingestor.js -i max
```

### Run agent by - 

```
python cis_audit.py --outformat json
```