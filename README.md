# Test Solr HadoopAuthenticationPlugin - LDAP

```bash
docker-compose up -d
docker-compose exec solr bash -c "./bin/solr zk cp file:/opt/security.json zk:/security.json -z localhost:9983"
docker-compose stop
docker-compose start
```

