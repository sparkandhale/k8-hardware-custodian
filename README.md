# k8-maas-custodian
A metal-as-a-service custodian, which wakes up nodes with Wake-On-LAN and makes them available to a Kubernetes cluster in need (employing the K8-API-Server). In the other way, the k8-maas-custodian decomissions metal (physical nodes), which is not needed anymore by the Kubernetes cluster and puts them asleep.
