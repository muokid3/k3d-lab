install: build release deploy test

build:
	docker build --tag muokid3/corpora .

run:
	docker run -d --name corpora -p 8080:80 muokid3/corpora

release:
	docker push muokid3/corpora

deploy:
	kubectl -n corpora apply -f ./k8s

test:
	@echo "Running tests -- may take a few seconds"
	@./test.sh > /dev/null
	@echo "Passed"
