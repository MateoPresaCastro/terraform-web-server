
This folder contains an example [Terraform](https://www.terraform.io/) configuration that deploys a cluster of web servers 
(using [EC2](https://aws.amazon.com/ec2/) and [Auto Scaling](https://aws.amazon.com/autoscaling/)) and a load balancer
(using [ELB](https://aws.amazon.com/elasticloadbalancing/)) in an [Amazon Web Services (AWS) 
account](http://aws.amazon.com/).

## Pre-requisites

* You must have [Terraform](https://www.terraform.io/) installed on your computer. 
* You must have an [Amazon Web Services (AWS) account](http://aws.amazon.com/).

## Quick start

Configure your [AWS access 
keys](http://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html#access-keys-and-secret-access-keys) as 
environment variables:

```
export AWS_ACCESS_KEY_ID=(your access key id)
export AWS_SECRET_ACCESS_KEY=(your secret access key)
```
Change the default deployer name in `variables.tf` to yours.


Deploy the code:

```
terraform init
terraform apply
```

When the `apply` command completes, it will output the DNS name of the load balancer. To test the load balancer copy the DNS name and paste it in your browser.

Clean up when you're done:

```
terraform destroy
```
##Dependency graph

You can run `terraform graph` and use [GraphvizOnline](https://dreampuf.github.io/GraphvizOnline/) to see the dependency graph:

```
terraform graph
```

Example:

![graphviz](https://user-images.githubusercontent.com/96750403/190396200-3cd19b3b-ee67-447e-88b9-c4fac3533ba5.png)




