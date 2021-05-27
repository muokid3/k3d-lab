install: repo namespace install-all

delete: delete-all

repo:
	@make -C fluentbit repo
	@make -C elastic repo
	@helm repo update

namespace:
	@kubectl apply namespace.yaml

install-all:
	@make -C fluentbit install
	@make -C elastic install

delete-all:
	@make -C fluentbit delete
	@make -C elastic delete
	@kubectl delete -f namespace.yaml