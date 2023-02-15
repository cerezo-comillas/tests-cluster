# tests-cluster

Me descargo el instalable: **wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-7.17.9-x86_64.rpm**

Instalo el software: **yum -y install elasticsearch-7.17.9-x86_64.rpm**

Arranco el servicio: **systemctl start elasticsearch**

Compruebo si el servicio está OK: **systemctl status elasticsearch**

Compruebo cuantos nodos tiene el cluster: **curl -XGET localhost:9200/_cat/nodes?v**

Fichero de configuracion: **/etc/elasticsearch/elasticsearch.yml**
