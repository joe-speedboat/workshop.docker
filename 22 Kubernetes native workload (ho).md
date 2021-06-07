# Deploy Kubernetes native workload
Let us deploy a Kubernetes native workload.
So we can get familiar with some of the components.

## Get k8s resources
```bash
cd
mkdir nodered
cd nodered
for r in deployment.yml ingress.yml pod.yml pvc.yml svc.yml
do
   wget https://raw.githubusercontent.com/joe-speedboat/workshop.docker/main/files/k8s/nodered/$r
done
```

From logs you can take two needs of the current container:
- Persistent volume (storage): `/data`
- Listen port: `1880`

## Configure depending container resources
Of course it is not given at any time that container needs are written to the logs.
If you can't find out the needs, you should look for:
- container registry documentation at  [dockerhub](https://hub.docker.com/r/nodered/node-red)
- Use `docker inspect` to look into a container
- Read the `Dockerfile` to see how the container got built.


<!--stackedit_data:
eyJoaXN0b3J5IjpbMTA2NDI5NTgzMCwtMTY0MTAzMzY3MV19
-->