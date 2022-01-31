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

Create Pod with Replicas (default Port 80)

```kubectl apply -f k8deploy.yaml```

For Localhost Expose Ports (Port 8081 => Container Port 80) with round robin load balancer

```kubectl expose -f k8deploy.yaml --port=8081 --target-port=80 --type=LoadBalancer```

&nbsp;  

## Public DockerHub Image

Based on nginx:latest

```scalabl3/furry-happiness```

[furry-happiness](https://hub.docker.com/repository/docker/scalabl3/furry-happiness/general)
