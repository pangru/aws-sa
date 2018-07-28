# Auto-Scaling

## AMI ID
  - Amazon Machine Image (AMI)
  - Launch Configuration is a template that an Auto Scaling group uses to launch EC2 instances
  - when create a launch configuration, you specify information for the instances such as the AMI ID

https://docs.aws.amazon.com/ko_kr/autoscaling/ec2/userguide/LaunchConfiguration.html

## Auto Scaling Life Cycle
https://docs.aws.amazon.com/autoscaling/ec2/userguide/AutoScalingGroupLifecycle.html

![Alt text](images/auto_scaling_lifecycle.png "Auto Scaling Lifecycle")

### Scale out

  1. Manual Scaling
    * manually increase the size of the group
  2. Dynamic Scaling
    * create a scaling policy to automatically increase the size of the group based on a specified increase in demand
  3. Scheduled Scaling
    * set up scaling by schedule to increase the size of the group at a specific time


 
