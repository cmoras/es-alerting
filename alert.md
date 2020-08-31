ogin
Register for Qiita Jobs and find the best jobs!
Click here for details
rururu_kenken
Atto Rururu_kenken
updated at 2020-08-23
Investigation of alert notification method based on Elasticsearch data
Elasticsearch
elastalert
praeco
17


X-Pack Watcher Alert
Developer: Elastic
Paid

Let's get started with Watcher

I tried using Elasticsearch's alert detection plug-in "Watcher"
Elastic Stack Alerting

X-Pack Alerting and action settings in Kibana
Developer: Elastic

Alerts and Actions
Managing Alerts
Alert details
Managing Connectors

ElastAlert
Developer: Yelp
Made in Python.
You are using "elasticsearch" from the Python library.
https://pypi.org/project/elasticsearch/
License is Apache License 2.0
0.2.4 (2020/04/17)

-Only operation based on command/setting file (YAML).
-Supports Elasticsearch 7.x from 0.2.0b2.
-Supports Python 3 from 0.2.0.

About ElastAlert (August 11, 2020)
Status of the elastalert project #2911

Alert notification destination
https://elastalert.readthedocs.io/en/latest/ruletypes.html#alerts

Alert notification destination	Remark
Command	Alert notification confirmed
Email	unconfirmed. There are no problems because cases can be seen in issues
JIRA	
OpsGenie	The description of the document is wrong
wrong
opsgenie_default_recipients
positive
Opsgenie_default_receipients
Fix Opsgenie_default_receipients To Docs # 2812
or less of what is described in the document forget that
Opsgenie_addr
Add Opsgenie_addr To Docs # 2278
Opsgenie_proxy
Add Opsgenie_proxy To Docs # 2813
Opsgenie_details
AWS SNS	Document is old
・aws_access_key → aws_access_key_id
・aws_secret_key → aws_secret_access_key
・profile → aws_profile
Elastalert AWS SNS Template #2205
HipChat	The service should have ended on 2019/02
Stride	The service should have ended on 2019/02
MS Teams	
Slack	Alert notification confirmed
Mattermost	Alert notification confirmed
Telegram	
Google Chat	
PagerDuty	
PagerTree	Since it does not work properly with the latest 0.2.4 as of August 23, 2020, I issued a pull request
Fix PagerTree #2934
Exotel	
Twilio	Alert notification confirmed
VictorOps	
Gitter	Alert notification confirmed
ServiceNow	
Debug	
Stomp	
Alerta	
HTTP POST	
Line Notify	Since it does not work properly with the latest 0.2.4 as of 5/20/2020, I issued a pull request
Fix LineNotify #2783
TheHive	
Zabbix	· Documents in what is described as "zbx_item" is "zbx_key". When writing zbx_item, the error "Missing required option(s): zbx_key" appears. I issued a pull request for document correction-An
error occurs when I add and move settings. There seems to be a bug.
(expected 2, got 1)Could not import module zabbix: not enough values ​​to unpack
Zabbix alert #2601
Zabbix alert module error #2621
Elastalet fails if alerter type zabbix is ​​used: "ValueError: not enough values ​​to unpack" [bug] #
It works properly with 2586 or less. Helped operation check
Bugfix and better error handling on zabbix alerter # 2640
Docker image
I am worried that ElastAlert Server will be maintained in the future.
Bitsensor/elastalert is not maintained. I think it is better to consider hiring johnsusek/elastalert-server forking and doing maintenance by yourself.
・ Will deprecated libraries (request, request-promise-native) be replaced?
-Support for new Node.js.
・Elasticserach major version support (latest 8.x)

Docker image name	tag	ElastAlert	Remark
bitsensor/elastalert	2.0.1	0.1.39	Problem with Elastcserach 7.x
bitsensor/elastalert	lastet	0.1.39	Problem with Elastcserach 7.x
bitsensor/elastalert	3.0.0-beta.0	0.2.0b2	
bitsensor/elastalert	3.0.0-beta.1	unconfirmed	
servercentral/elastalert	latest	0.2.1	
daichi703n/elastalert	0.2.1-dev2	0.2.1	Use image of jfcantu/elastalert:v0.1.1? .. Refer to the following site for other bug fixes.
Praeco + ElastAlert2.0 + ES7.x configuration bug fix method
daichi703n/elastalert-server (GitHub)
praecoapp/elastalert-server	latest	0.2.4	Updated
library of Elast Alert Server for Praeco Updated
Babel 6→7
Fixed issue where alert log was not displayed
Java heap memory exhaustion due to too many open indexes
circuit_breaking_exception may occur → Elastic Search
heap size changed
→ ElasticSearch
indices.breaker.total.limit changed
→ ElasticSearch Index data deleted, or unnecessary Index data closed
Heap memory exhaustion due to too
large Elasticsearch index opening elastalert feels very unhappy ( circuit_breaking_exception, Data too large) #2485
circuit_breaking_exception, Data too large #349
After Upgrade to 6.2.4 Circuitbreaker Exception Data too large #31197
Elastalert deployment failed

Reference URL
Introducing Kubernetes monitoring system with Elastic Stack
Elasticsearch index monitoring and notification with
ElastAlert I want to automatically detect and notify anomaly of an app with
elastalert – elastalert – Easy and flexible alert with
ElasticSearch Create custom rules with
ElastAlert Error log with ElasticSearch + Elastalert I want to notify you when it is detected
Expand the monitoring rule of ElastAlert and be a little happy It is
a service monitoring utilizing Elasticsearch I will be a little happy Monitoring
AWS ElasticSearch Service logs with ElastAlert
twitter -> fluentd -> elasticsearch -> elastalert- > It was a life where I wanted to play egoza with slack.
Alert to the slack using the Elastalert
Alerting On Kubernetes Events With EFK Stack
ElastAlert: Alerting At Scale With Elasticsearch, Part 1

sample
elastalert/example_rules
andromedarabbit/elastalert-rule.yaml
Alert to slack using elastalert

Elastalert rule for CPU usage in percentage
Elastalert-Regel ausge führt: IOError: [Errno 2] Keine solche Datei oder Verzeichnis:'config.yaml'
Example fails: elastalert.util.EAException: Invalid Rule: Metricbeat CPU Spike Rule
ELK: ElastAlert for alerting based on data from ElasticSearch
manankalra/elastalert-tutorial
・elastalert_cpu_watch.yaml
・elastalert_filesystem_watch.yaml
・elastalert_memory_watch.yaml

ElastAlert Kibana Plugin
Developer: BitSensor
license is The 3-clause BSD license (Modified)
1.1.0 (2019/07/22)

・ElastAlert rule file editor
・ElastAlert can be incorporated as a tab of Kibana. -Only
files under the alert rule directory can be
managed.-Kibana 7.2.0 to 7.5.0 is supported.
・It is recommended not to use with Praero.
<Reason>
If you edit with settings that are not supported by Praeco, the settings you wrote when changing the alert rules to valid or invalid in Praeco will be erased.
It should be noted that this movement is caused by the user's incorrect use, and I think it is a specification.

Thoughts on ElastAlert Kibana Plugin (as of 2020/8/23)
It is not possible to use it with the latest Kibana (officially supports up to Kibana 7.5.0), so it is not recommended to
use it.
Although it is unofficial support, I fork the repository on GitHub to support the latest Kibana.

Kibana 6.8.1 ~ 6.8.10, 7.5.1 ~ 7.9.0 compatible
https://github.com/nsano-rururu/elastalert-kibana-plugin/releases

Will Kibana 6.8.x work?
kibana 6.8.1 support #117
Can't install elastalert-kibana-plugin-1.0.3-6.8.0.zip to Kibana 6.8.3 #123

Works with Kibana 7.5.1-7.8.1
Download elastalert-kibana-plugin-1.1.0-7.5.0.zip , update Kibana version of
kibana/elastalert-kibana-plugin/package.json
and compress it to a zip file
Kibana 7.5.1, Works with 7.5.2.
For Kibana 7.6.0 to 7.8.1, it is necessary to replace elastalert.js in addition to updating Kibana version in package.json.

By the way, regarding Kibana 7.6.x support, pull request has been raised on the official website (checked on April 7, 2020)
manually disabling payload validation on the routes to fix for Kibana 7.6.0 #148

Plugin elastalert-kibana-plugin [7.5.0] is incompatible with Kibana [7.5.1] #139
Plugin is incompatible with Kibana 7.6.0 #141
[Legacy] Route payload must be set to'parse ' when payload validation enabled #57777
update elasticsearch to 7.6.2; also, fix issue idaholab#119

When making a Docker image with the ElastAlert plugin installed in Kibana
I wrote another article about how to create a Docker image of Kibana 7.5.1 to 7.8.1 How
to create a Docker image with elastalert-kibana-plugin installed

The following is when installing the ElastAlert plugin with docker-compose command
# (Reference information) elastalert-kibana-plugin-1.1.0-7.5.1.zip created
cd /tmp
curl -L -O https://github.com/bitsensor/elastalert-kibana-plugin/releases/download/1.1.0/elastalert-kibana-plugin-1.1.0-7.5.0.zip
mv elastalert-kibana-plugin-1.1.0-7.5.0.zip elastalert-kibana-plugin-1.1.0-7.5.1.zip
unzip elastalert-kibana-plugin-1.1.0-7.5.1.zip kibana/elastalert-kibana-plugin/package.json
sed -i "s/7\.5\.0/7\.5\.1/g" kibana/elastalert-kibana-plugin/package.json
zip elastalert-kibana-plugin-1.1.0-7.5.1.zip kibana/elastalert-kibana-plugin/package.json
rm -rf kibana

# elastalert-kibana-plugin-1.1.0-7.5.2.zip created
cd /tmp
curl -L -O https://github.com/bitsensor/elastalert-kibana-plugin/releases/download/1.1.0/elastalert-kibana-plugin-1.1.0-7.5.0.zip
mv elastalert-kibana-plugin-1.1.0-7.5.0.zip elastalert-kibana-plugin-1.1.0-7.5.2.zip
unzip elastalert-kibana-plugin-1.1.0-7.5.2.zip kibana/elastalert-kibana-plugin/package.json
sed -i "s/7\.5\.0/7\.5\.2/g" kibana/elastalert-kibana-plugin/package.json
zip elastalert-kibana-plugin-1.1.0-7.5.2.zip kibana/elastalert-kibana-plugin/package.json
rm -rf kibana

# (Reference information) elastalert-kibana-plugin-1.1.0-7.6.0.zip created
cd /tmp
curl -L -O https://github.com/bitsensor/elastalert-kibana-plugin/releases/download/1.1.0/elastalert-kibana-plugin-1.1.0-7.5.0.zip
# [update elasticsearch to 7.6.2; also, fix issue idaholab#119](https://github.com/mmguero-dev/Malcolm/commit/b38ddb7f0d4c5b03e6f8ccad58a656644e113b19)
curl -L -O https://raw.githubusercontent.com/mmguero-dev/Malcolm/development/kibana/elastalert-kibana-plugin/server/routes/elastalert.js
mv elastalert.js elastalert-server-routes.js
mv elastalert-kibana-plugin-1.1.0-7.5.0.zip elastalert-kibana-plugin-1.1.0-7.6.0.zip
unzip elastalert-kibana-plugin-1.1.0-7.6.0.zip kibana/elastalert-kibana-plugin/package.json
sed -i "s/7\.5\.0/7\.6\.0/g" kibana/elastalert-kibana-plugin/package.json
mkdir -p kibana/elastalert-kibana-plugin/server/routes/
cp /tmp/elastalert-server-routes.js kibana/elastalert-kibana-plugin/server/routes/elastalert.js
zip elastalert-kibana-plugin-1.1.0-7.6.0.zip kibana/elastalert-kibana-plugin/package.json kibana/elastalert-kibana-plugin/server/routes/elastalert.js
rm -rf kibana
rm elastalert-server-routes.js

# (Reference information) elastalert-kibana-plugin-1.1.0-7.6.1.zip created
cd /tmp
curl -L -O https://github.com/bitsensor/elastalert-kibana-plugin/releases/download/1.1.0/elastalert-kibana-plugin-1.1.0-7.5.0.zip
# [update elasticsearch to 7.6.2; also, fix issue idaholab#119](https://github.com/mmguero-dev/Malcolm/commit/b38ddb7f0d4c5b03e6f8ccad58a656644e113b19)
curl -L -O https://raw.githubusercontent.com/mmguero-dev/Malcolm/development/kibana/elastalert-kibana-plugin/server/routes/elastalert.js
mv elastalert.js elastalert-server-routes.js
mv elastalert-kibana-plugin-1.1.0-7.5.0.zip elastalert-kibana-plugin-1.1.0-7.6.1.zip
unzip elastalert-kibana-plugin-1.1.0-7.6.1.zip kibana/elastalert-kibana-plugin/package.json
sed -i "s/7\.5\.0/7\.6\.1/g" kibana/elastalert-kibana-plugin/package.json
mkdir -p kibana/elastalert-kibana-plugin/server/routes/
cp /tmp/elastalert-server-routes.js kibana/elastalert-kibana-plugin/server/routes/elastalert.js
zip elastalert-kibana-plugin-1.1.0-7.6.1.zip kibana/elastalert-kibana-plugin/package.json kibana/elastalert-kibana-plugin/server/routes/elastalert.js
rm -rf kibana
rm elastalert-server-routes.js

# (Reference information) elastalert-kibana-plugin-1.1.0-7.6.2.zip created
cd /tmp
curl -L -O https://github.com/bitsensor/elastalert-kibana-plugin/releases/download/1.1.0/elastalert-kibana-plugin-1.1.0-7.5.0.zip
# [update elasticsearch to 7.6.2; also, fix issue idaholab#119](https://github.com/mmguero-dev/Malcolm/commit/b38ddb7f0d4c5b03e6f8ccad58a656644e113b19)
curl -L -O https://raw.githubusercontent.com/mmguero-dev/Malcolm/development/kibana/elastalert-kibana-plugin/server/routes/elastalert.js
mv elastalert.js elastalert-server-routes.js
mv elastalert-kibana-plugin-1.1.0-7.5.0.zip elastalert-kibana-plugin-1.1.0-7.6.2.zip
unzip elastalert-kibana-plugin-1.1.0-7.6.2.zip kibana/elastalert-kibana-plugin/package.json
sed -i "s/7\.5\.0/7\.6\.2/g" kibana/elastalert-kibana-plugin/package.json
mkdir -p kibana/elastalert-kibana-plugin/server/routes/
cp /tmp/elastalert-server-routes.js kibana/elastalert-kibana-plugin/server/routes/elastalert.js
zip elastalert-kibana-plugin-1.1.0-7.6.2.zip kibana/elastalert-kibana-plugin/package.json kibana/elastalert-kibana-plugin/server/routes/elastalert.js
rm -rf kibana
rm elastalert-server-routes.js

# (Reference information) elastalert-kibana-plugin-1.1.0-7.7.0.zip created
cd /tmp
curl -L -O https://github.com/bitsensor/elastalert-kibana-plugin/releases/download/1.1.0/elastalert-kibana-plugin-1.1.0-7.5.0.zip
# [update elasticsearch to 7.7.0; also, fix issue idaholab#119](https://github.com/mmguero-dev/Malcolm/commit/b38ddb7f0d4c5b03e6f8ccad58a656644e113b19)
curl -L -O https://raw.githubusercontent.com/mmguero-dev/Malcolm/development/kibana/elastalert-kibana-plugin/server/routes/elastalert.js
mv elastalert.js elastalert-server-routes.js
mv elastalert-kibana-plugin-1.1.0-7.5.0.zip elastalert-kibana-plugin-1.1.0-7.7.0.zip
unzip elastalert-kibana-plugin-1.1.0-7.7.0.zip kibana/elastalert-kibana-plugin/package.json
sed -i "s/7\.5\.0/7\.7\.0/g" kibana/elastalert-kibana-plugin/package.json
mkdir -p kibana/elastalert-kibana-plugin/server/routes/
cp /tmp/elastalert-server-routes.js kibana/elastalert-kibana-plugin/server/routes/elastalert.js
zip elastalert-kibana-plugin-1.1.0-7.7.0.zip kibana/elastalert-kibana-plugin/package.json kibana/elastalert-kibana-plugin/server/routes/elastalert.js
rm -rf kibana
rm elastalert-server-routes.js

# (Reference information) elastalert-kibana-plugin-1.1.0-7.7.1.zip created
cd /tmp
curl -L -O https://github.com/bitsensor/elastalert-kibana-plugin/releases/download/1.1.0/elastalert-kibana-plugin-1.1.0-7.5.0.zip
# [update elasticsearch to 7.7.1; also, fix issue idaholab#119](https://github.com/mmguero-dev/Malcolm/commit/b38ddb7f0d4c5b03e6f8ccad58a656644e113b19)
curl -L -O https://raw.githubusercontent.com/mmguero-dev/Malcolm/development/kibana/elastalert-kibana-plugin/server/routes/elastalert.js
mv elastalert.js elastalert-server-routes.js
mv elastalert-kibana-plugin-1.1.0-7.5.0.zip elastalert-kibana-plugin-1.1.0-7.7.1.zip
unzip elastalert-kibana-plugin-1.1.0-7.7.1.zip kibana/elastalert-kibana-plugin/package.json
sed -i "s/7\.5\.0/7\.7\.1/g" kibana/elastalert-kibana-plugin/package.json
mkdir -p kibana/elastalert-kibana-plugin/server/routes/
cp /tmp/elastalert-server-routes.js kibana/elastalert-kibana-plugin/server/routes/elastalert.js
zip elastalert-kibana-plugin-1.1.0-7.7.1.zip kibana/elastalert-kibana-plugin/package.json kibana/elastalert-kibana-plugin/server/routes/elastalert.js
rm -rf kibana
rm elastalert-server-routes.js

# (Reference information) elastalert-kibana-plugin-1.1.0-7.8.0.zip created
cd /tmp
curl -L -O https://github.com/bitsensor/elastalert-kibana-plugin/releases/download/1.1.0/elastalert-kibana-plugin-1.1.0-7.5.0.zip
# [update elasticsearch to 7.8.0; also, fix issue idaholab#119](https://github.com/mmguero-dev/Malcolm/commit/b38ddb7f0d4c5b03e6f8ccad58a656644e113b19)
curl -L -O https://raw.githubusercontent.com/mmguero-dev/Malcolm/development/kibana/elastalert-kibana-plugin/server/routes/elastalert.js
mv elastalert.js elastalert-server-routes.js
mv elastalert-kibana-plugin-1.1.0-7.5.0.zip elastalert-kibana-plugin-1.1.0-7.8.0.zip
unzip elastalert-kibana-plugin-1.1.0-7.8.0.zip kibana/elastalert-kibana-plugin/package.json
sed -i "s/7\.5\.0/7\.8\.0/g" kibana/elastalert-kibana-plugin/package.json
mkdir -p kibana/elastalert-kibana-plugin/server/routes/
cp /tmp/elastalert-server-routes.js kibana/elastalert-kibana-plugin/server/routes/elastalert.js
zip elastalert-kibana-plugin-1.1.0-7.8.0.zip kibana/elastalert-kibana-plugin/package.json kibana/elastalert-kibana-plugin/server/routes/elastalert.js
rm -rf kibana
rm elastalert-server-routes.js
Directory structure
./elastalert/rules, ./elastalert/rule_templates, ./es/data are chmod 777 settings

ElastAlert files are from the following sites. Fixed some values
https://github.com/bitsensor/elastalert

/home/username/dkwork/es/
|--docker-compose.yml
|--Dockerfiles
| |--Dockerfile.elastalert
|
|--es
| |--config
| | |--elasticsearch.yml
| |--data
|
|--kibana
| |--config
| | |--kibana.yml
| |--plugin
| | |--elastalert-kibana-plugin-1.1.0-7.7.0.zip
|
|--elastalert
| |--bin
| | |--elastalert-start.sh
| | |--elastic_search_status.sh
| |--config
| | |--config.json
| | |--elastalert-test.yaml
| | |--elastalert.yaml
| |--rule_templates
| |--rules
docker-compose.yml
Version :  " 3.7" 
Services : 
  Elasticsearch : 
    Container_name :  Elasticsearch 
    Image :  Docker.Elastic.Co/elasticsearch/elasticsearch:7.7.0 
    Ports : 
      -  9200: 9200 
      -  9300: 9300 
    Environment : 
      -  ES_JAVA_OPTS = -Xms256m -Xmx512m 
      -  Discovery.Type =single-node 
    restart :  always 
    volumes : 
      --  ./es/data:/usr/share/elasticsearch/data-./es/config/elasticsearch.yml 
      :  /usr/share/elasticsearch/config/elasticsearch.yml 
    healthcheck :
        test :  [ " CMD-SHELL" ,  " curl -f http://localhost:9200 || exit 1" ] interval : 30s timeout : 15s retries : 3 start_period : 180s     
         
         
         
         

  kibana : 
    container_name :  kibana 
    image :  docker.elastic.co/kibana/kibana:7.7.0 
    command :  sh -c'./bin/kibana-plugin list | grep elastalert-kibana-plugin@1.1.0; result=`echo $$?`; if [$$result = 1 ]; then ./bin/kibana-plugin install file:///usr/share/kibana/work/elastalert-kibana-plugin-1.1.0-7.7.0. zip && exec /usr/local/bin/kibana-docker; else exec /usr/local/bin/kibana-docker; fi' 
    ports : 
      --  5601:5601 
    depends_on : 
      --  elasticsearch 
    restart :  always 
    volumes : 
      --  ./kibana/config /Kibana.Yml:/Usr/share/kibana/config/kibana.Yml 
      - ./kibana/plugin:/usr/share/kibana/work 
    healthcheck : 
        test :  [ " CMD-SHELL" ,  " curl -f http://localhost:5601/api/status || exit 1" ] interval : 30s timeout : 15s retries : 3 start_period : 200s     
         
         
         
         

  Elastalert : 
    Container_name :  Elastalert 
    Build : 
      Context :  . 
      Dockerfile :  Dockerfiles / Dockerfile.Elastalert 
    Image :  Elastalert: 3.0.0-Beta.0 
    Ports : 
      -  3030: 3030 
      -  3333: 3333 
    Depends_on : 
      -  Elasticsearch 
      -  Kibana 
    Restart :  Always 
    Volumes : 
      -  ./Elastalert/config/elastalert.Yaml:/Opt/elastalert/config.Yaml 
      -  ./Elastalert/config/elastalert-test.Yaml:/Opt/elastalert/config-test.Yaml 
      - ./Elastalert/config/config.Json:/Opt/elastalert-server/config/config.Json 
      -  ./Elastalert/rules:/Opt/elastalert/rules 
      -  ./Elastalert/rule_templates:/Opt/elastalert/rule_templates 
    Healthcheck : 
        test :  [ " CMD-SHELL" ,  " curl -f http://localhost:3030 || exit 1" ] interval : 30s timeout : 15s retries : 3 start_period : 200s     
         
         
         
         
Dockerfiles/Dockerfile.elastalert
FROM bitsensor/elastalert:3.0.0-beta.0

USER root

RUN apk update && \
    apk add bash curl && \
    rm -rf /var/cache/apk/*

ADD elastalert/bin/elastalert-start.sh /usr/local/bin/
ADD elastalert/bin/elastic_search_status.sh /usr/local/bin/

RUN chmod +x /usr/local/bin/elastalert-start.sh 
RUN chmod +x /usr/local/bin/elastic_search_status.sh

USER node

ENTRYPOINT ["/usr/local/bin/elastalert-start.sh"]
elastalert/bin/elastic_search_status.sh
#!/bin/bash

set  -e

If  [  $ # -Gt 0 ] ;  Then
   ES_URL = " $ 1 " 
Elif  [[  -N  $ ELASTICSEARCH_URL  ]] ;  Then
   ES_URL = " $ ELASTICSEARCH_URL " 
Elif  [[  -N  $ ES_HOST  ]]  Andoando  [[  -N  $ ES_PORT  ]] ;  then
   ES_URL = "http:// $ES_HOST : $ES_PORT " 
else
   ES_URL = "http://elasticsearch:9200" 
fi

until  [[  " $( curl -fsSL  " $ES_URL /_cat/health?h=status" | sed  -r's  /^[[:space:]]+|[[:space:]]+$//g ' ) "  = ~ ^ ( yellow|green ) $ ]] ;  do 
  # printf'+' >&2 
  sleep 1
 done

echo  "Elasticsearch is up and healthy at " $ES_URL ""  > &2
elastalert/bin/elastalert-start.sh
#!/bin/bash

set  -e

echo  "Giving Elasticsearch at $ELASTICSEARCH_URL time to start..."

elastic_search_status.sh

echo  "Starting ElastAlert!"
npm start
es/config/elasticsearch.yml
cluster.name :  " docker-cluster" 
network.host :  0.0.0.0 
discovery.zen.minimum_master_nodes :  1
kibana/config/kibana.yml
server.name :  kibana 
server.host :  " 0" 
elasticsearch.hosts :  http://elasticsearch:9200 
xpack.monitoring.ui.container.elasticsearch.enabled :  true

# elastalert-kibana-plugin 
elastalert-kibana-plugin.serverHost :  elastalert 
elastalert-kibana-plugin.serverPort :  3030
elastalert/config/config.json
{ "appName" : "elastalert-server" , "port" : 3030 , "wsport" : 3333 , "elastalertPath" : "/opt/elastalert" , "verbose" : false , "es_debug" : false , "debug" : false , "rulesPath" : { "relative" : true , "path" : "/rules" }, "templatesPath" :{ "relative" : true , "path"
   
   
   
   
   
   
   
   
     
     
  
   
     
    : "/rule_templates" }, "es_host" : "elasticsearch" , "es_port" : 9200 , "writeback_index" : "elastalert_status" } 
  
   
   
   

Change the value of es_host from "localhost" to "elasticsearch"

elastalert/config/elastalert-test.yml
# NOTE: This config is used when testing a rule

# The elasticsearch hostname for metadata writeback 
# Note that every rule can have its own elasticsearch host 
es_host :  elasticsearch

# The elasticsearch port 
es_port :  9200

# This is the folder that contains the rule yaml files 
# Any .yaml file will be loaded as a rule 
rules_folder :  rules

# How often ElastAlert will query elasticsearch 
# The unit can be anything from weeks to seconds 
run_every : 
  seconds :  5

# ElastAlert will buffer results from the most recent 
# period of time, in case some log sources are not in real time 
buffer_time : 
  minutes :  1

# Optional URL prefix for elasticsearch 
#es_url_prefix: elasticsearch

# Connect with TLS to elasticsearch 
#use_ssl: True

# Verify TLS certificates 
#verify_certs: True

# GET request with body is the default option for Elasticsearch. 
# If it fails for some reason, you can pass'GET','POST' or'source'. 
# See http://elasticsearch-py.readthedocs.io/en /master/connection.html?highlight=send_get_body_as#transport 
# for details 
#es_send_get_body_as: GET

# Option basic-auth username and password for elasticsearch 
#es_username: someusername 
#es_password: somepassword

# The index on es_host which is used for metadata storage 
# This can be a unmapped index, but it is recommended that you run 
# elastalert-create-index to set a mapping 
writeback_index :  elastalert_status

# If an alert fails for some reason, ElastAlert will retry 
# sending the alert until this time period has elapsed 
alert_time_limit : 
  days :  2
Change the value of es_host from "localhost" to "elasticsearch"

elastalert/config/elastalert.yml
# The elasticsearch hostname for metadata writeback 
# Note that every rule can have its own elasticsearch host 
es_host :  elasticsearch

# The elasticsearch port 
es_port :  9200

# This is the folder that contains the rule yaml files 
# Any .yaml file will be loaded as a rule 
rules_folder :  rules

# How often ElastAlert will query elasticsearch 
# The unit can be anything from weeks to seconds 
run_every : 
  seconds :  5

# ElastAlert will buffer results from the most recent 
# period of time, in case some log sources are not in real time 
buffer_time : 
  minutes :  1

# Optional URL prefix for elasticsearch 
#es_url_prefix: elasticsearch

# Connect with TLS to elasticsearch 
#use_ssl: True

# Verify TLS certificates 
#verify_certs: True

# GET request with body is the default option for Elasticsearch. 
# If it fails for some reason, you can pass'GET','POST' or'source'. 
# See http://elasticsearch-py.readthedocs.io/en /master/connection.html?highlight=send_get_body_as#transport 
# for details 
#es_send_get_body_as: GET

# Option basic-auth username and password for elasticsearch 
#es_username: someusername 
#es_password: somepassword

# The index on es_host which is used for metadata storage 
# This can be a unmapped index, but it is recommended that you run 
# elastalert-create-index to set a mapping 
writeback_index :  elastalert_status

# If an alert fails for some reason, ElastAlert will retry 
# sending the alert until this time period has elapsed 
alert_time_limit : 
  days :  2
1.PNG
2.PNG
When you click the "Save" button,
a yaml file (here, test.yaml) of Rule name will be created in the elastalert/rules directory . If you press the Delete rule button, a confirmation dialog will appear. Click OK to delete the corresponding rule file from the elastalert/rules directory . Delete confirmation dialog
3.PNG
4.PNG



5.PNG

6.PNG

Praeco
Maintainers: John Susek, Naoyuki Sano
license is GNU General Public License v3.0
1.3.0 (2020/08/23)

Install Praeco (ElastAlert GUI) on Kubernetes with Helm (Beta)
Praeco + ElastAlert2.0 + ES7.x Configuration bug
Remedy Elasticsearch log alert with Praeco (ElastAlert GUI)

-Praeco uses johnsusek/elastalert-server , which is a fork of ElastAlert Server developed by BitSensor, the developer of ElastAlert Kibana Plugin . It seems to have Python3 + ElastAlert 0.2.4 support and its own modification. -By using Praeco, you can operate ElastAlert on a GUI basis and 　set alert notifications from Elasticsearch logs. -Alert rule settings -Alert history - 　> 1.0.1 Nothing is displayed. Fixed in 1.1.0 (confirmed June 17, 2020)-Query history -Disable alert rules for a certain period- Support Elasticsearch 7 (0.4.2-) -Alert notification destinations are Slack, Email, HTTP POST, Telegram, Jira, MS Teams, Mattermost, Command, Line Notify, Gitter, Zabbix, SNS, Twilio, PagerTree are set. -Rule Type does not support Percentage Match and Spike Aggregation. Add "Percentage Match" rule type #82 Add "Spike Aggregation" rule type #228












Docker image
Docker image name	tag	Praeco	Remark
praecoapp/praeco	latest	1.3.0	
daichi703n/praeco	0.3.5	1.0.1	daichi703n/praeco (GitHub)
mkdir Dockerfiles
touch Dockerfiles/Dockerfile.elastalert
mkdir -p es/config
touch es/config/elasticsearch.yml
mkdir -p es/data
chmod 777 es/data
mkdir -p kibana/config
touch kibana/config/kibana.yml
mkdir -p praeco/bin
touch praeco/bin/elastalert-start.sh
touch praeco/bin/elastic_search_status.sh
mkdir -p praeco/config
mkdir -p praeco/nginx_config
mkdir -p praeco/public
mkdir -p praeco/public/js
mkdir -p praeco/rule_templates
chmod 777 praeco/rule_templates
mkdir -p praeco/rules
chmod 777 praeco/rules
cd praeco/rules
wget https://raw.githubusercontent.com/johnsusek/praeco/master/rules/BaseRule.config
cd ../
cd praeco/config
wget https://raw.githubusercontent.com/johnsusek/praeco/master/config/api.config.json
wget https://raw.githubusercontent.com/johnsusek/praeco/master/config/elastalert.yaml
cd ../
cd nginx_config
wget https://raw.githubusercontent.com/johnsusek/praeco/master/nginx_config/default.conf
wget https://raw.githubusercontent.com/johnsusek/praeco/master/nginx_config/nginx.conf
cd ../
cd public/js
wget https://raw.githubusercontent.com/johnsusek/praeco/master/public/js/cron-ui.min.js
cd ../
wget https://github.com/johnsusek/praeco/blob/master/public/favicon.ico
wget https://raw.githubusercontent.com/johnsusek/praeco/master/public/index.html
wget https://raw.githubusercontent.com/johnsusek/praeco/master/public/praeco.config.json
cd ../../

docker-compose up -d
praeco.PNG

/home/username/dkwork/es/
|--docker-compose.yml
|--Dockerfiles
| |--Dockerfile.elastalert
|--es
| |--config
| | |--elasticsearch.yml
| |--data
|
|--kibana
| |--config
| | |--kibana.yml
|
|--praeco
| |--bin
| | |--elastalert-start.sh
| | |--elastic_search_status.sh
| |--config
| | |--api.config.json
| | |--elastalert.yaml
| |--nginx_config
| | |--default.conf
| | |----nginx.conf
| |--public
| | |--js
| | | | --cron-ui.min.js
| | |--favicon.ico
| | |--index.html
| | |----praeco.config.json
| |--rule_templates
| |--rules
| | |--BaseRule.config
Dockerfiles/Dockerfile.elastalert
FROM johnsusek/elastalert-server:latest

USER root

RUN apk update && \
    apk add bash curl && \
    rm -rf /var/cache/apk/*

ADD praeco/bin/elastalert-start.sh /usr/local/bin/
ADD praeco/bin/elastic_search_status.sh /usr/local/bin/

RUN chmod +x /usr/local/bin/elastalert-start.sh 
RUN chmod +x /usr/local/bin/elastic_search_status.sh

USER node

ENTRYPOINT ["/usr/local/bin/elastalert-start.sh"]
praeco/bin/elastic_search_status.sh
#!/bin/bash

set  -e

If  [  $ # -Gt 0 ] ;  Then
   ES_URL = " $ 1 " 
Elif  [[  -N  $ ELASTICSEARCH_URL  ]] ;  Then
   ES_URL = " $ ELASTICSEARCH_URL " 
Elif  [[  -N  $ ES_HOST  ]]  Andoando  [[  -N  $ ES_PORT  ]] ;  then
   ES_URL = "http:// $ES_HOST : $ES_PORT " 
else
   ES_URL = "http://elasticsearch:9200" 
fi

until  [[  " $( curl -fsSL  " $ES_URL /_cat/health?h=status" | sed  -r's  /^[[:space:]]+|[[:space:]]+$//g ' ) "  = ~ ^ ( yellow|green ) $ ]] ;  do 
  # printf'+' >&2 
  sleep 1
 done

echo  "Elasticsearch is up and healthy at " $ES_URL ""  > &2
praeco/bin/elastalert-start.sh
#!/bin/bash

set  -e

echo  "Giving Elasticsearch at $ELASTICSEARCH_URL time to start..."

elastic_search_status.sh

echo  "Starting ElastAlert!"
npm start
es/config/elasticsearch.yml
cluster.name :  " docker-cluster" 
network.host :  0.0.0.0 
discovery.zen.minimum_master_nodes :  1
kibana/config/kibana.yml
server.name :  kibana 
server.host :  " 0" 
elasticsearch.hosts :  http://elasticsearch:9200 
xpack.monitoring.ui.container.elasticsearch.enabled :  true
docker-compose.yml
Version :  " 3.7" 
Services : 
  Elasticsearch : 
    Container_name :  Elasticsearch 
    Image :  Docker.Elastic.Co/elasticsearch/elasticsearch:7.7.0 
    Ports : 
      -  9200: 9200 
      -  9300: 9300 
    Environment : 
      -  ES_JAVA_OPTS = -Xms256m -Xmx512m 
      -  Discovery.Type =single-node 
    restart :  always 
    volumes : 
      --  ./es/data:/usr/share/elasticsearch/data-./es/config/elasticsearch.yml 
      :  /usr/share/elasticsearch/config/elasticsearch.yml 
    healthcheck :
        test :  [ " CMD-SHELL" ,  " curl -f http://localhost:9200 || exit 1" ] interval : 30s timeout : 15s retries : 3 start_period : 180s     
         
         
         
         

  kibana : 
    container_name :  kibana 
    image :  docker.elastic.co/kibana/kibana 
    : 7.7.0 ports : 
      -  5601:5601 
    depends_on : 
      -  elasticsearch 
    restart :  always 
    volumes : 
      --  ./kibana/config/kibana.yml:/usr/share /kibana/config/kibana.yml 
    healthcheck : 
        test :  [ " CMD-SHELL" ,  " curl -f http://localhost:5601/api/status || exit 1" ] interval : 30s timeout     
         
        :  15s 
        retries :  3 
        start_period :  200s

  Elastalert : 
    Container_name :  Elastalert 
    Build : 
      Context :  . 
      Dockerfile :  Dockerfiles / Dockerfile.Elastalert 
    Image :  Elastalert-Server: 1.1.0 
    Ports : 
      -  3030: 3030 
      -  3333: 3333 
    Depends_on : 
      -  Elasticsearch 
    Restart :  Always 
    Volumes : 
      -  ./Praeco/ Config / Elastalert.Yaml: /Opt/elastalert/config.Yaml 
      -  ./Praeco/config/api.Config.Json:/Opt/elastalert-server/config/config.Json 
      -  ./Praeco/rules:/Opt/elastalert /rules
      -  ./Praeco/rule_templates:/Opt/elastalert/rule_templates 
    Healthcheck : 
        Test :  [ " CMD SHELL-" ,  " Curl -F Http: // Localhost: 3030 || Exit 1" ] Interval : 30S Timeout : 15S Retries : 3 start_period : 200s     
         
         
         
         

  praeco : 
    container_name :  praeco 
    image :  johnsusek/praeco:latest 
    ports : 
      --  8080:8080 
    depends_on : 
      --  elastalert 
    restart :  always 
    volumes : 
      --  ./praeco/public/praeco.config.json:/var/www/html/praeco.config .json 
      -./  praeco 
      /  nginx_config/     
    nginx.conf : 
        /etc/nginx/nginx.conf -./ praeco / nginx_config/ default.conf : /etc/nginx/conf.d/default.conf healthcheck : test :  [ " CMD-SHELL" ,  " curl -f  http://localhost:8080 || exit 1" ] interval : 30s timeout : 15s retries : 3 start_period : 200s   
         
         
         
         
The following files use the ones on the Praeco site
https://github.com/johnsusek/praeco
・praeco/config/api.config.json
・praeco/config/elastalert.yaml
・praeco/nginx_config/default.conf
・praeco /nginx_config/nginx.conf
・praeco/public/js/cron-ui.min.js
・praeco/public/favicon.ico
・praeco/public/index.html
・praeco/public/praeco.config.json
・praeco/rules /BaseRule.config

Open Distro for Elasticsearch
Developer: AWS
License is Apache License 2.0
"Elasticsearch" original distribution
1.9.0 (2020/07/09. Elastcsearch and Kibana versions are 7.8.0)
amazon/opendistro-for-elasticsearch
amazon/opendistro-for- elasticsearch-kibana

Things I noticed by moving the screen (version 1.3.0)

・The
　initial user/password with the login screen is admin/admin

・Is it possible to delete the Index on the screen like the X-Pack Index management in the current version?

-Functions such as Index Lifecycle Management (ILM) of X-Pack seem to be the functions that can edit the yaml to set.

・I tried to monitor AWS Console Login by using Alerting of Amazon Elasticsearch Service that can set alerts on the screen

-Output function to CSV/PDF file is not yet implemented
PDF Generation and reporting #16

The following is not yet confirmed

-Is it possible to import the dashboard created by Elastic's Kibana 7.4.2? And what about versions above 7.4.2?

-In the setting of Fluentd's Elastcsearch plug-in, settings related to Index Lifecycle Management (ILM) should not be available, so if there is a setting it will be necessary to comment and check the operation

-It seems that you need to uninstall Fluentd's X-Pack plug-in and check the operation.

-Since Fluentd, Metricbeat, Filebeat, Heartbeat, and Logstash still have little information, it seems necessary to carefully investigate whether to investigate and use settings that move based on information.

Security
https://opendistro.github.io/for-elasticsearch-docs/docs/security-configuration/
https://opendistro.github.io/for-elasticsearch-docs/docs/security-access-control/
https:/ /opendistro.github.io/for-elasticsearch-docs/docs/security-audit-logs/

Alerting
https://opendistro.github.io/for-elasticsearch-docs/docs/alerting/

SQL
https://opendistro.github.io/for-elasticsearch-docs/docs/sql/

Index State Management (ISM)
X-Pack Index Lifecycle Management (ILM)-like functionality
https://opendistro.github.io/for-elasticsearch-docs/docs/ism/

KNN
https://opendistro.github.io/for-elasticsearch-docs/docs/knn/

Anomaly Detection (Alpha)
https://opendistro.github.io/for-elasticsearch-docs/docs/ad/

Performance Analyzer
https://opendistro.github.io/for-elasticsearch-docs/docs/pa/

Root Cause Analysis (Alpha)
https://opendistro.github.io/for-elasticsearch-docs/docs/rca/

Fluentd
Fluentd support
Self-signed Certificate verify failed (Fluend + Open Distro for Elasticsearch) #597

Beats
Trying out Open Distro for Elasticsearch with Logstash Filebeat connection issue
Integration with beats
Unable to index filebeat logs with LogStash #136
filebeat 6.5.4 output to elasticsearch #21
Metricbeat User Permission
Configuring OSS Beats (File/Metric) with opendistro
Alerting using metricbeat parameters #13
Logstash intergration

Introducing – Open Distro for Elasticsearch
Vendors Disagree with AWS's Open Distro for Elasticsearch
AWS Releases New Elasticsearch Distribution with Apache License
I tried Open Distro for Elasticsearch!
Open Distro for Elasticsearch Kickstart guide
[Update] Amazon Elasticsearch Service now supports alerts

Grafana
How to read Grafana
Developer: Grafana Labs
License is Apache License 2.0
7.1.3 (2020/08/07)

From 5.2.0, alert notification for data in Elasticsearch is possible.

Alerting
Alert Notifications
DingDing
Discord
Email
Google Hangouts Chat
Hipchat
Kafka
Line
Microsoft Teams
OpsGenie
Pagerduty
Prometheus Alertmanager
Pushover
Sensu
Slack
Squadcast
Telegram
Threema
VictorOps
Webhook
Creating Alert That Can Send SNMP Trap As A Notification

That is not supported right now

Email
Set alert notifications in
Grafana Grafana Email notification settings
Stuck stories in Grafana email settings
Email notifications in Grafana


Visualization of data acquired via Slack BLE (Grafana) & alert notification (Slack) implemented
Visualization of server metrics accumulated in Elasticserch with Grafana + I tried to build an Slack notification environment for alerts (Nifuku)
Performance monitoring with Prometheus+Grafana doing

Execute Alerting for data in Elasticsearch with Discord
Grafana 5.2.0+ and notify Discord

Teams
Prometheus Recommendation-Notifying Teams of Alerts with Grafana is easy

System monitoring with webhook
Prometheus 2 and Grafana 6 Use Alert of Grafana

7. Elastalert UI
License is Apache License 2.0
maintenance end. Last updated on GitHub 2018/12/12

Edit request

Stock

17
rururu_kenken
Naoyuki Sano
Atto Rururu_kenken
http://rururu.sakura.ne.jp
Follow
Why not register and get more from Qiita?
Sign up
Login

Related articles Recommended by

Linux permission confirmation and change (for super beginners)
by shisama


Table joins that can be understood even by SQL amateurs (inner join and outer join)
by naoki_mochizuki

Most straightforward OAuth description
by Takahiko Kawasaki

[Linux] How to compress and decompress files
by supersaiakujin

“What!? Haskellko talks to Wai!?” feat. Taro Yame
PR dream

Ask a LenovoPRO representative to choose a PC
PR Lenovo Japan
Linked from these articles
rururu_kenken
Investigation of Docker log collection method
Link from
3 months ago
blueskyarea
Send an alert to gmail with the Elastalert kibana plugin
Link from
4 months ago
rururu_kenken
Investigating how Docker collects metrics
Link from
1 year ago

Comments
daichi703n
@ daichi703n
2020-02-13 06:10
-Even if the value of appUrl of public/praeco.config.json was changed, the URL of the title of Slack notification, http://localhsot:8080 , did not change.

Let me check about this.

Directory structure in articles

/home/username/dkwork/es/
...
|--praeco
| |--config
| | |--api.config.json
| | |--elastalert.yaml
| |--nginx_config
| | |--default.conf.conf
| |--public
| | |--js
| | | | --cron-ui.min.js
| | |--favicon.ico
| | |--index.html
| | |----praeco.config.json
| |--rule_templates
| |--rules
Looking at, docker-compose.ymlit seems that the path of the source directory that is volume mounted is not correct.

version: "3.7"
services:
  elastalert:
    ...
  praeco:
    container_name: praeco
    image: servercentral/praeco:latest
    ports:
      -8080:8080
    volumes:
      -./public/praeco.config.json:/var/www/html/praeco.config.json
      -./nginx_config/nginx.conf:/etc/nginx/nginx.conf
      -./nginx_config/default.conf:/etc/nginx/conf.d/default.conf
    networks:
      -es_default
Wouldn't the Slack title URL be reflected as expected by making the following modifications?

version: "3.7"
services:
  elastalert:
    ...
  praeco:
    container_name: praeco
    image: servercentral/praeco:latest
    ports:
      -8080:8080
    volumes:
      -./praeco/public/praeco.config.json:/var/www/html/praeco.config.json
      -./praeco/nginx_config/nginx.conf:/etc/nginx/nginx.conf
      -./praeco/nginx_config/default.conf:/etc/nginx/conf.d/default.conf
    networks:
      -es_default
Please check the above as it works without problems in my environment.

Praeco Recommended because it is the most convenient! !!
Since you can set rules while checking the match status on the GUI, even people who are not familiar with Elasticsearch queries can easily set alerts and it is popular within the team.


1
rururu_kenken
Atto Rururu_kenken
2020-02-13 21:01
@daichi703n

Thank you for your advice.
As expected, the Slack title URL was reflected.


1
Sign up for free and join this conversation.
Sign Up
If you already have a Qiita account Login
How developers code is here.
Qiita
About
Terms
Privacy
Guideline
Release
API
Your opinion
Help
Advertisement
Increments
About
Employment information
Blog
Qiita Team
Qiita Jobs
Qiita Zine
© 2011-2020 Increments Inc.
