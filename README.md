# Web Tier using AWS EC2 Windows (single-az/single EC2/no auto scaling)

Deploying a Windows Server EC2 Instance in AWS using Terraform

![Alt text](/images/diagram.png)

1. vpc module - to create vpc, public subnet, internet gateway, security groups and route tables
2. web module - to create Windows Web EC2 instance with userdata script to display instance metadata using latest Windows ami.
3. main module - Above modules get called in main config.

Terraform Plan Output:
```
Plan: 7 to add, 0 to change, 0 to destroy.
```

Terraform Apply Output:
```
Apply complete! Resources: 7 added, 0 changed, 0 destroyed.

Outputs:

instance_id = "i-0af8c526023ab3d7d"
public_ip = "http://44.205.246.179/"
```

Running Website:

![Alt text](/images/website.png)

Console:
![Alt text](/images/console.png)

Windows RDP:
![Alt text](/images/rdp.png)

Terraform Destroy Output:
```
Plan: 0 to add, 0 to change, 7 to destroy.

Destroy complete! Resources: 7 destroyed.
```