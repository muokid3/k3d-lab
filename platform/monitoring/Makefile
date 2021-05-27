default: install-namespace

install: repo install-namespace install-prometheus install-grafana 

delete: delete-grafana delete-prometheus delete-namespace

install-namespace:
	@kubectl apply -f namespace.yaml

install-prometheus:
	@make -C prometheus install

install-grafana:
	@make -C grafana install

delete-grafana:
	@make -C grafana delete

delete-prometheus:
	@make -C prometheus delete

delete-namespace:
	@kubectl delete -f namespace.yaml

repo:
	@make -C prometheus repo
	@make -C grafana repo
	@helm repo update





