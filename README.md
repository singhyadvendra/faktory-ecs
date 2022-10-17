# AWS Cloudformation for Deploying contribsys/faktory
This [template](cloudformation-faktory.yaml) will deploy the follwing resources

1. Application load balancer for accesing `faktory UI on Port 80` which maps to `port 7420` on the conatiner
2. Network Load Balancer to access `tcp Endpoint on 7419` which maps to same port on the container
3. ECS Cluster
4. ECS Service
5. ECS Task Definition
6. EFS
7. and other peripheral resources like security groups, elb listener for application and network load balancer, elb target groups for tcp endpoint for NLB and htpp endpoint for ALB, security groups for alb, ecs and efs, ingress and egress rules for security groups, mount points for EFS, scaling policy and scaling target for ECS

This template creates internal load balancers if you want your factory on a internet facing load balancer. just change the scheme type
from `Scheme: "internal"` to `Scheme: "internet-facing"` for load balancers

## references
For Faktory information [Faktory](https://github.com/contribsys/faktory "FAKTORY Information Page")

For docker image information [Docker Hub](https://hub.docker.com/r/contribsys/faktory/)
