# COVID19 Statud Board

## Data

- https://www.kaggle.com/kimjihoo/coronavirusdataset


## Elasticsearch (with Docker)

Document : https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html  
Guild Book (Web) : https://esbook.kimjmin.net/

## Kibana (with Docker)

Document : https://www.elastic.co/guide/en/kibana/current/docker.html

## Logstash (with Docker)

Document : https://www.elastic.co/guide/en/logstash/current/docker.html

## Command

```bash
docker pull docker.elastic.co/elasticsearch/elasticsearch:7.15.0
docker pull docker.elastic.co/logstash/logstash:7.15.0
docker pull docker.elastic.co/kibana/kibana:7.15.0

docker run --name es01-test --net elastic -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:7.15.0
docker run --name kib01-test --net elastic -p 5601:5601 -e "ELASTICSEARCH_HOSTS=http://es01-test:9200" docker.elastic.co/kibana/kibana:7.15.0
```

## Directory

```
├── Dockerfile
├── README.md
├── city_data.csv
├── corona_daliy_data.csv
├── corona_data.csv
├── data
│   ├── Case.csv
│   ├── PatientInfo.csv
│   ├── Policy.csv
│   ├── Region.csv
│   ├── SearchTrend.csv
│   ├── SeoulFloating.csv
│   ├── Time.csv
│   ├── TimeAge.csv
│   ├── TimeGender.csv
│   ├── TimeProvince.csv
│   └── Weather.csv
├── make_csv.ipynb
└── region_data.csv
```
