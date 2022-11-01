<h2> Prometheus </h2> 
<p>Prometheus was built to monitor highly dynamic container environments e.g. Kubernetes, and docker swarm. However, it can also monitor applications deployed on bare servers.</p>

<p> Modern DevOps is more complex, where 100 of the processes might be running on multiple containerized applications on different servers, all of which could be interconnected. Maintaining such infrastructure is extremely difficult and complex, this is where Prometheus help us to monitor all these things effectively. </p>
<h3>Prometheus Server</h3> 
Prometheus server is main component which do actual monitoring work.
<ol>
  <li>Time series database: It stores metrics data. eg. CPU Usage, No. of exceptions </li>
  <li>Data Retrieval worker: It pull metrics data from servers, applications and services and push them into database</li>
  <li>API Server: It accepts queries for stored data in database and server API is used to diplay data on dashboard using Prometheus web UI or grafana </li>
</ol> 
<img src="https://github.com/ShubhPatil95/Prometheus/blob/main/images/Prometheus-server.png">

<h3>Target and Metrics</h3> 
<ol>
  <li> Target: It could be Linux/Windows server, Apache server, Single application or service like Database</li>
  <li> Metrics: It us unit that you want to monitor for your target. eg. CPU status, memory/disk usage, exception count</li>
</ol> 

<h3>Metrics</h3> 
Format: Human readable text based
Metrics entries: TYPE and HELP attributes

<ol>
  <li> HELP: It could be Linux/Windows server, Apache server, Single application or service like Database</li>
  <li> TYPE: It us unit that you want to monitor for your target. eg. CPU status, memory/disk usage, exception count</li>
  <ol>
    <li>Counter : How many times X happend?</li>
    <li>Gauge : What is current value of X?</li>
    <li>Histogram : How long or how big?</li>
  </ol>
</ol> 

<h3>Exporter</h3> 
<p>Prometheus pulls metric data from target using HTTP endpoint which is by default is hostaddress/metrics.</p>
<p> For that to work 1) Target must expose to /metrics endpoint and 2) data available at /metrics must be in correct format</p>
<p> Some servers are already exposing Prometheus endpoints by default, but many services dont have native Prometheus endpoints. Hence extra component is needed for that which is Exporter</p>
<p>Exporter is service or script that 1) Fetches metrics from target 2) Convert to correct format 3) expose this data to /metrics endpoint from where Prometheus can grab them. There are many exporters eg. node exporter is used for linux sservers</p>

<h3>Pull system advantages</h3> 
<p>Most monitoring system like Amazon cloud watch uses push system, meaninig applications and server push own metrics data, but when many applications/services are pushing data, it will create a nertwork traffic hence our monitoring will become bottlneck for our infrastructure.</p>
<p>Prometheus do offers Pushgateway for short time running targets</p>
<ol>
  <li> multiple Prometheus instances can pull metrics data</li>
  <li> better detection/insight if service is up and running</li>
</ol> 

<h3>Prometheus configuration</h3>
<p>prometheus.yml file contains 1) which target? and 2) at what interval metrics need to be pulled</p>

<p> Global section contains varibles at what interval metrics to be pulled, rule_files section is contains Rule for aggregating metric values or creating alerts when condition met,scrape_configs section contain what resources need to be monitored</p>

<img src="https://github.com/ShubhPatil95/Prometheus/blob/main/images/config.png" alt="Default config file">

<h3>Prometheus Charecteristics</h3>
<ol>
  <li> Reliable</li>
  <li> stand-alone and self containing</li>
  <li> no extensive set up needed</li>
  <li> less complex</li>
  <li> works well even if other part of infrastructure is broken</li>
  <li> difficult to scale</li>
  <li> limit on number of metrics you monitor. Workaround: increase prometheus server capacity, limit number of metrics</li>
</ol> 

</p>
