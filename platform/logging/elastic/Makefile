install: install-elastic install-kibana 

delete: delete-kibana delete-elastic

install-elastic:
	@helm install elasticsearch elastic/elasticsearch -f elastic-values.yaml -n logging

install-kibana:
	@helm install kibana elastic/kibana -f kibana-values.yaml -n logging

delete-kibana:
	@helm delete kibana

delete-elastic:
	@helm delete elastic

repo:
	@helm repo add elastic https://helm.elastic.co

