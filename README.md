# high-availability-web-app

AWS CloudFormation templates for the network and servers required for a highly available web application

## What's inside the templates?

This template deploys:
* a VPC,
    with a pair of public and private subnets spread 
    across two Availabilty Zones. 
* It deploys an Internet Gateway, with a default 
route on the public subnets. 
* It deploys a pair of NAT Gateways (one in each AZ), 
and default routes for them in the private subnets.

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
