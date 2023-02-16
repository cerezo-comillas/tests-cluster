# tests-cluster

Me descargo el instalable: **wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.17.9-x86_64.rpm**

Instalo el software: **yum -y install elasticsearch-7.17.9-x86_64.rpm**

Arranco el servicio: **systemctl start elasticsearch**

Compruebo si el servicio está OK: **systemctl status elasticsearch**

Rearranco el servicio: **systemctl status elasticsearch**

Compruebo cuantos nodos tiene el cluster: **curl -XGET localhost:9200/_cat/nodes?v**

Fichero de configuracion: **/etc/elasticsearch/elasticsearch.yml**

Directorio de logs: **/var/log/elasticsearch**

## Comandos para Elasticsearch

Carga del fichero de datos: **curl -X POST "localhost:9200/_bulk?pretty" -H 'Content-Type: application/json' --data-binary @tenis_bulk.json**

curl localhost:9200/_cat/shards/data-atp

curl -X DELETE "localhost:9200/data-atp?pretty" 

curl -X PUT "localhost:9200/data-atp?pretty" -H 'Content-Type: application/json' -d'
{
  "settings": {
    "index": {
      "number_of_shards": 4,  
      "number_of_replicas": 3
    }
  }
}'


