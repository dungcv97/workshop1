---
title : "Clean up resources"
date : "`r Sys.Date()`"
weight : 6
chapter : false
pre : " <b> 6. </b> "
---
## Clean up resources

We will proceed to delete the resources in the following order:

#### Terminate EC2 Instances

- Access the Amazon EC2 console at [EC2](https://console.aws.amazon.com/ec2/).
- On the left navigation bar, select "Instances."
- Select all EC2 instances related to the lab.
- Select **Instance state**.
- Select **Terminate instance**.

#### Delete service network associations in VPC Lattice Service

- Visit the Amazon VPC console page at [VPC](https://console.aws.amazon.com/vpc/).
- On the left navigation bar, click "Services."
- Select service.
- Select **Service network associations** tab
- Click **Action**.
- Click **Delete network associations**.
- Type "confirm."

#### Delete Service

- Visit the Amazon VPC console page at [VPC](https://console.aws.amazon.com/vpc/).
- On the left navigation bar, click "Services."
- Select service.
- Click **Action**.
- Click **Delete service**.
- Type "confirm."

#### Delete Target Group

- Visit the Amazon VPC console page at [VPC](https://console.aws.amazon.com/vpc/).
- On the left navigation bar, click "Target groups."
- Select target group.
- Click **Action**.
- Click **Delete**.
- Type "confirm."

#### Delete VPC associations in VPC Lattice Service Networks

- Visit the Amazon VPC console page at [VPC](https://console.aws.amazon.com/vpc/).
- On the left navigation bar, click "Service networks."
- Select service network.
- Select **VPC associations** tab
- Select all VPC related to the lab.
- Click **Action**.
- Click **Delete VPC associations**.
- Type "confirm."

#### Delete Service Networks

- Visit the Amazon VPC console page at [VPC](https://console.aws.amazon.com/vpc/).
- On the left navigation bar, click "Service networks."
- Select service network.
- Click **Action**.
- Click **Delete service network**.
- Type "confirm."

#### Delete NAT gateways

- Remove NAT Gateway and Elastic IP Address. AWS charges for wasted EIPs, so you need to double-check to avoid unintended charges.
- Visit the Amazon VPC console page at [VPC](https://console.aws.amazon.com/vpc/).
- On the left navigation bar, click "NAT Gateway."
- Select NAT Gateway.
- Click **Action**.
- Click **Delete NAT Gateway**.
- Type "delete."

#### Delete VPC

- Visit the Amazon VPC console page at [VPC](https://console.aws.amazon.com/vpc/).
- On the left navigation bar, click "Your VPCs."
- Select all VPC related to the lab.
- Click **Action**.
- Click **Delete VPC**.
- Type "delete."

#### Delete Elastic IP Address

- Visit the Amazon VPC console page at [VPC](https://console.aws.amazon.com/vpc/).
- On the left navigation bar, click "Elastic IP."
- Select the Elastic IP Address we created.
- Click **Action**.
- Click **Release Elastic IP Address**.
- Click **Release**.
