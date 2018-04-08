NAMESPACE := mysql
K 			  := kubectl -n $(NAMESPACE)

ns:
	kubectl create ns $(NAMESPACE)

secret:
	envsubst < secret.yaml | $(K) apply -f -

deploy:
	$(K) apply -f statefulset.yaml

password:
	$(K) -n mysql log mysql-0 | grep PASSWORD
