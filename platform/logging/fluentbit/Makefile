cycle: delete install

install:
	@kubectl apply -f fluentbit.yaml

delete:
	@kubectl delete -f fluentbit.yaml

repo:
	@helm repo add fluent https://fluent.github.io/helm-charts