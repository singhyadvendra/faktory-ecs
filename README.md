# AWS Cloudformation for Deploying contribsys/faktory
This template will deploy the follwing resources

1. Application load balancer for accesing UI of faktory on Port 80 which maps to port 7420 on the conatiner
2. Network Load Balancer to access tcp Endpoint on 7419 which maps to same port on the container
3. ECS Cluster
4. ECS Service
5. ECS Task Definition
6. EFS
7. and peripheral resources like security groups, elb listener for application and network load balancer, elb target groups for tcp endpoint for NLB and htpp endpoint for ALB, security groups for alb, ecs and efs

## references
For Faktory information [Faktory](https://github.com/contribsys/faktory)

For docker image information [Docker Hub](https://hub.docker.com/r/contribsys/faktory/)
