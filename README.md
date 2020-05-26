###

Running:
```
docker-compose up -d
docker-compose ps
```

Update
```
./anchore-cli system status
./anchore-cli system feeds list
./anchore-cli system wait
```

Test the security
```
./anchore-cli image add mario21ic/devopsperu:1.0
./anchore-cli image wait mario21ic/devopsperu:1.0

./anchore-cli image content mario21ic/devopsperu:1.0
./anchore-cli image content mario21ic/devopsperu:1.0 os
./anchore-cli image content mario21ic/devopsperu:1.0 all

./anchore-cli image vuln mario21ic/devopsperu:1.0 
./anchore-cli image vuln mario21ic/devopsperu:1.0 all

./anchore-cli evaluate check  mario21ic/devopsperu:1.0 
```

Note: Download or update docker-compose recipe:
```
curl https://docs.anchore.com/current/docs/engine/quickstart/docker-compose.yaml > docker-compose.yaml
```
