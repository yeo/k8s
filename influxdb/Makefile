NAMESPACE := influx
K 			  := kubectl -n $(NAMESPACE)

ns:
	kubectl create ns $(NAMESPACE)

deploy:
	$(K) apply -f statefulset.yaml
