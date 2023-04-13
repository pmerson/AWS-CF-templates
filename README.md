# AWS-CF-templates

[CloudFormation](https://aws.amazon.com/cloudformation/) (CF) is the IaC solution/service offered in the AWS cloud.

This repository contains a few CF templates developed by Paulo Dantas (from AWS) to be used in an educational project about distributed systems architecture.
For each CF template, you see the AWS deployment architecture and an example of application architecture that could be deployed to that AWS infrastructure.
The templates have increasing complexity. 

## EC2 and RDS cluster

The [CF template](/templates/CF-A1-cmu.yml).

AWS deployment diagram (using [AWS notation](https://aws.amazon.com/architecture/icons/)).

![AWS deployment diagram](/images/a1-deployment-view.png)


Example of application design that could be deployed to this infrastructure.

![runtime view diagram](/images/a1-runtime-view.jpg)
![notation key](/images/notation-key-runtime-views.jpg)


## Multiple EC2 and RDS cluster

The [CF template](/templates/CF-A2-cmu.yml).

AWS deployment diagram (using [AWS notation](https://aws.amazon.com/architecture/icons/)).

![AWS deployment diagram](/images/a2-deployment-view.png)


Example of application design that could be deployed to this infrastructure.

![runtime view diagram](/images/a2-runtime-view.jpg)



## EKS cluster and RDS cluster

The [CF template](/templates/CF-A3-cmu.yml).

AWS deployment diagram (using [AWS notation](https://aws.amazon.com/architecture/icons/)).

![AWS deployment diagram](/images/a3-deployment-view.png)

Example of application design that could be deployed to this infrastructure.

![runtime view diagram](/images/a3-runtime-view.jpg)

