# furry-happiness

![Furry Happiness](src/img/giphy.gif)

Simple nginx docker container serving static page and images

## K8 Commands

Create Pod with Replicas (default Port 80)

```kubectl apply -f k8deploy.yaml```

For Localhost Expose Ports (Port 8081 => Container Port 80) with round robin load balancer

```kubectl expose -f k8deploy.yaml --port=8081 --target-port=80 --type=LoadBalancer```


## DockerHub Image
```scalabl3/furry-happiness```

[furry-happiness](https://hub.docker.com/repository/docker/scalabl3/furry-happiness/general)
