**Note:** For the screenshots, you can store all of your answer images in the `answer-img` directory.

## Verify the monitoring installation

*TODO:* run `kubectl` command to show the running pods and services for the three components. Copy and paste the output or take a screenshot of the output and include it here to verify the installation

screenshot: running_services.png

vagrant@localhost:~> kubectl get pods
No resources found in default namespace.
vagrant@localhost:~> kubectl get pods --all-namespaces
NAMESPACE       NAME                                                     READY   STATUS      RESTARTS   AGE
kube-system     local-path-provisioner-7ff9579c6-kgnv2                   1/1     Running     0          5m4s
kube-system     metrics-server-7b4f8b595-qm7q8                           1/1     Running     0          5m4s
kube-system     coredns-66c464876b-bd7cs                                 1/1     Running     0          5m4s
kube-system     helm-install-traefik-5s9jt                               0/1     Completed   0          5m5s
kube-system     svclb-traefik-97bz8                                      2/2     Running     0          4m39s
kube-system     traefik-5dd496474-wvsbl                                  1/1     Running     0          4m39s
monitoring      prometheus-kube-prometheus-operator-7946cd46c7-ds957     1/1     Running     0          2m10s
monitoring      prometheus-kube-state-metrics-5b8f9bdbbd-d4vjk           1/1     Running     0          2m10s
monitoring      prometheus-prometheus-node-exporter-v9mrt                1/1     Running     0          2m11s
monitoring      alertmanager-prometheus-kube-prometheus-alertmanager-0   2/2     Running     0          112s
monitoring      prometheus-prometheus-kube-prometheus-prometheus-0       2/2     Running     1          110s
monitoring      prometheus-grafana-7b764c9d78-rdl7c                      2/2     Running     0          2m10s
observability   jaeger-operator-6954c97677-f65vv                         1/1     Running     0          60s
## Setup the Jaeger and Prometheus source
*TODO:* Expose Grafana to the internet and then setup Prometheus as a data source. Provide a screenshot of the home page after logging into Grafana.

screenshot: grafana_after_login.png

## Create a Basic Dashboard
*TODO:* Create a dashboard in Grafana that shows Prometheus as a source. Take a screenshot and include it here.

screenshots: dashboard_with_prometheus

It is not clear exactly what is required, I made different shots, all uses Prometheus as source


## Describe SLO/SLI
*TODO:* Describe, in your own words, what the SLIs are, based on an SLO of *monthly uptime* and *request response time*.

## Creating SLI metrics.
*TODO:* It is important to know why we want to measure certain metrics for our customer. Describe in detail 5 metrics to measure these SLIs. 

## Create a Dashboard to measure our SLIs
*TODO:* Create a dashboard to measure the uptime of the frontend and backend services We will also want to measure to measure 40x and 50x errors. Create a dashboard that show these values over a 24 hour period and take a screenshot.

## Tracing our Flask App
*TODO:*  We will create a Jaeger span to measure the processes on the backend. Once you fill in the span, provide a screenshot of it here.

## Jaeger in Dashboards
*TODO:* Now that the trace is running, let's add the metric to our current Grafana dashboard. Once this is completed, provide a screenshot of it here.

## Report Error
*TODO:* Using the template below, write a trouble ticket for the developers, to explain the errors that you are seeing (400, 500, latency) and to let them know the file that is causing the issue.

TROUBLE TICKET

Name:

Date:

Subject:

Affected Area:

Severity:

Description:


## Creating SLIs and SLOs
*TODO:* We want to create an SLO guaranteeing that our application has a 99.95% uptime per month. Name three SLIs that you would use to measure the success of this SLO.

## Building KPIs for our plan
*TODO*: Now that we have our SLIs and SLOs, create KPIs to accurately measure these metrics. We will make a dashboard for this, but first write them down here.

## Final Dashboard
*TODO*: Create a Dashboard containing graphs that capture all the metrics of your KPIs and adequately representing your SLIs and SLOs. Include a screenshot of the dashboard here, and write a text description of what graphs are represented in the dashboard.  
