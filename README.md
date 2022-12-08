# k8-maas-custodian
A metal-as-a-service custodian, which wakes up nodes with Wake-On-LAN and makes them available to a Kubernetes cluster in need (employing the K8-API-Server). In the other way, the k8-maas-custodian decomissions metal (physical nodes), which is not needed anymore by the Kubernetes cluster and puts them asleep.

## Functionality
- Manually register MAC addresses with a form.
- Automatically detect and recommend MAC Addresses to add to the managed metal array.
- Learn what the Kubernetes Clusters need (by the API Server resp by stats).
- Wake up one or many metals/nodes.
- Learn what the Kubernetes Cluster can dispense/suspend.
- Put to sleep idle nodes marked by Kubernetes (or anticipated by stats).

## Tech Stack
- Starelette/JINJA2 for the website.
- Request library to query the K8 API Server
- SQLite to store the data within the deployment (docker volumes).
- pyhton WOL Library to send magick packages: https://pypi.org/project/wakeonlan/ 
- Dockerized.
