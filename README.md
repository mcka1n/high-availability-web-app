# high-availability-web-app

AWS CloudFormation templates for the network components, servers, and other resources (security roles, AutoScalingGroups, LoadBalancers, etc.) required for a highly available web application

## What's inside the templates?

This template deploys:
* a VPC,
    with a pair of public and private subnets spread 
    across two Availabilty Zones. 
* It deploys an Internet Gateway, with a default 
route on the public subnets. 
* It deploys a pair of NAT Gateways (one in each AZ), 
and default routes for them in the private subnets.

## Infrastructure diagram

We shouldn't start coding without clear view of what's the goal of the project isn't it? ... so in the same way, we shouldn't start building our Infrastructure As Code without an infrastructure diagram, here is the one I made for this project:

![infra-diagram](https://github.com/mcka1n/high-availability-web-app/blob/master/infrastructure_diagram/ERMPHighAvailabilityWebAppProject.png)

## How to use it?

I'm leveraging the `create.sh` and `update.sh` bash scripts provided by Udacity to save some time in every CloudFormation command.

So the way you use it is:


### Create

#### Network

```
bash create.sh edwin-infra-project-1 network.yml network-parameters.json
```

#### Servers

```
bash create.sh edwin-servers-project-1 servers.yml server-parameters.json
```

### Update

#### Network

```
bash update.sh edwin-infra-project-1 network.yml network-parameters.json
```

#### Servers

```
bash update.sh edwin-servers-project-1 servers.yml server-parameters.json
```
