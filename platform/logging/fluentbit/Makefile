cycle: delete install

install:
	@helm apply -f fluentbit.yaml

delete:
	@helm delete -f fluentbit.yaml

repo:
	@helm repo add fluent https://fluent.github.io/helm-charts