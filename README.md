# AWS-CF-templates

[CloudFormation](https://aws.amazon.com/cloudformation/) (CF) is the IaC solution/service offered in the AWS cloud.

This repository contains a few CF templates developed by Paulo Dantas (from AWS) and Paulo Merson. They were created to 
be used in an educational project about distributed systems architecture.
For each CF template, you see the AWS deployment architecture and an example of application architecture that could be deployed 
to that AWS infrastructure. The templates have increasing complexity. 

## EC2 and RDS cluster

The [CF template](/templates/CF-A1-cmu.yml).

AWS deployment diagram (using [AWS notation](https://aws.amazon.com/architecture/icons/)).

![AWS deployment diagram](/images/a1-deployment-view.jpg)


Example of application design that could be deployed to this infrastructure.

![runtime view diagram](/images/a1-runtime-view.jpg)
![notation key](/images/notation-key-runtime-views.jpg)


## Multiple EC2 instances, routing based on HTTP header, BFFs, and RDS cluster

The [CF template](/templates/CF-A2-cmu.yml). (The routing rules are incomplete on purpose. 
It's a challenge to you to fix them based on the application design further below.)

AWS deployment diagram (using [AWS notation](https://aws.amazon.com/architecture/icons/)).

![AWS deployment diagram](/images/a2-deployment-view.jpg)


Example of application design that could be deployed to this infrastructure.

![runtime view diagram](/images/a2-runtime-view.jpg)

The mapping of microservices to EC2 instances could be the one in this table. The CF template has target groups corresponding to these subsets of instances.

| Service | EC2 instances it should be deployed to |
|---------|----------------------------------------|
| Book store web app BFF (port 80)       | EC2BookstoreA, EC2BookstoreB           |
| Book store mobile app BFF (port 80)       | EC2BookstoreC, EC2BookstoreD           |
| Customer service (port 3000)       | EC2BookstoreA, EC2BookstoreD   |
| Book service (port 3000)       | EC2BookstoreB, EC2BookstoreC       |


## EKS cluster and RDS cluster

The [CF template](/templates/CF-A3-cmu.yml).

AWS deployment diagram (using [AWS notation](https://aws.amazon.com/architecture/icons/)).

![AWS deployment diagram](/images/a3-deployment-view.jpg)


Example of application design that could be deployed to this infrastructure.

![runtime view diagram](/images/a3-runtime-view.jpg)

