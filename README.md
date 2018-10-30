# Test Solr HadoopAuthenticationPlugin - LDAP

## Setup
```bash
docker-compose up -d
docker-compose exec solr bash -c "./bin/solr zk cp file:/opt/security.json zk:/security.json -z localhost:9983"
docker-compose stop
docker-compose start
```

## Testing
```bash
# First request should get a 401
curl -i "http://localhost:8983/v2/collections" 

# Second request should go through
curl -i -u billy:billy "http://localhost:8983/v2/collections"
```

