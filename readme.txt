#Set no replicas for new index. Not automated.
curl -XPUT 'localhost:9200/_template/logstash_template' -d ' 
{ 
  "template" : "logstash-*", 
  "settings" : {"number_of_replicas" : 0 }
} '