# furry-happiness

![Furry Happiness](src/img/giphy.gif)

Simple nginx docker container serving static page and images

&nbsp;  

## Docker Commands

Pull image from DockerHub into local image repository

```docker pull scalabl3/furry-happiness```

(Git Clone this repo) then Launch the image (uses port 8082 => 80 from docker-compose.yaml)  

```docker-compose up```

&nbsp;  

## K8 Commands

Locahost 8081 => 80 -- Create Pod with Replicas & Expose Service (YAML)

```kubectl apply -f k8deploy.yaml;kubectl apply -f k8service.yaml```

Delete Pod & Service (YAML)

```kubectl delete -f k8deploy.yaml;kubectl delete -f k8service.yaml```

Expose Pod Service (YAML)

```kubectl apply -f k8service.yaml```

Manual Expose: For Localhost Expose Ports (Port 8081 => Container Port 80) with round robin load balancer

```kubectl expose -f k8deploy.yaml --port=8081 --target-port=80 --type=LoadBalancer```

Manual Delete: For Localhost Expose Load Balancer

``` kubectl delete service furry-happiness-canary```

&nbsp;  

## Public DockerHub Image

Based on nginx:latest

```scalabl3/furry-happiness```

[furry-happiness](https://hub.docker.com/repository/docker/scalabl3/furry-happiness/general)
