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
</ol> 
### Step 1: Create a new conda environment
```bash
conda create -n dvc_env python=3.8
```

</p>
