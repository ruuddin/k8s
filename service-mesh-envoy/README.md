
About Envoy: https://www.magalix.com/blog/what-is-a-service-mesh

- deploy to cluster: kubectl -n <ns> apply -f config-map.yaml -f deployment.yaml -f service.yaml
- send request: curl -XPOST --data '{"dateOfBirth":"2020-01-26"}' <ip>/hello/Magalixcorp
