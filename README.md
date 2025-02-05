# test

1.	Customize configuration (values.yaml)
	It's best to create an overload file (myvalues.yaml) to customize the configuration without affecting the default values.
TODO what to modify? 

2.	Deploy chart with Helm
following command from the repository root (where the chart folder is located)
helm install netbox ./netbox-chart --namespace my-namespace -f myvalues.yaml

netbox is the name you give to the Helm release.
-f myvalues.yaml takes into account your configuration overrides (if you've created any).
To upgrade
helm upgrade netbox ./netbox-chart --namespace my-namespace -f myvalues.yaml

3.	Check deployment
kubectl get pods

Translated with DeepL.com (free version)
