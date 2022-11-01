<h2>Prometheus-Setup-on Kubernetes using Helm and Prometheus Operator</h2>
There are 3 ways to deploy prometheus on Kubernetes
<h4>1. Creating all configuration YAML files yourself and execute them in right order</h4>
<p> This method is inefficent and needs lot of efforts beacuase you actually need to have knowledge of each steps and what you are going to do</p>
<h4>2. Using Operator</h4>
<p> Operators are manager of all prometheus components. Here you need to 1) Find the operator for prometheus and 2) Deploy it in K8s cluster using configuration file of the operator</p>
<h4>3. Using Helm Chart to deploy operator</h4>
<p>Prometheus operator have Helm chart which is maintained by Helm community. Heml will do initial setup and operator will manage setup</p>

<h3>Setup With HELM Chart</h3>

```ruby
```
