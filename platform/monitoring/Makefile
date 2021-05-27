default: install-namespace

install: install-namespace install-prometheus install-grafana 

delete: delete-grafana delete-prometheus delete-namespace

install-namespace:
	@kubectl apply -f namespace.yaml

install-prometheus:
	@make -C prometheus repo
	@make -C prometheus install

install-grafana:
	@make -C grafana repo
	@make -C grafana install

delete-grafana:
	@make -C grafana delete

delete-prometheus:
	@make -C prometheus delete

delete-namespace:
	@kubectl delete -f namespace.yaml

update-repo:
	@helm repo update





