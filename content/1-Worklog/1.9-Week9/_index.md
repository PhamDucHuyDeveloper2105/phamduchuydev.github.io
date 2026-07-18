---

title: "Week 9 Worklog"
date: 2026-06-22
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
----------------------

### Week 9 Objectives:

* Learn about Elastic Load Balancing and the role of Load Balancer in AWS systems.
* Understand the concepts of Target Group, Listener, and Health Check.
* Learn about Auto Scaling Group and how AWS automatically adjusts the number of EC2 Instances.
* Become familiar with Launch Template and basic scaling policies.

### Tasks to be carried out this week:

| Day       | Task                                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                                                 |
| --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ------------------------------------------------------------------ |
| Monday    | - Learn the overview of Elastic Load Balancing <br> - Understand the role of Load Balancer in distributing traffic <br> - Take notes on common types of Load Balancers on AWS                                          | 22/06/2026 | 22/06/2026      | https://cloudjourney.awsstudygroup.com/                            |
| Tuesday   | - Learn about Application Load Balancer (ALB) <br> - Become familiar with Listener, Target Group, and Health Check <br> - Observe the Load Balancer interface on AWS Console                                           | 23/06/2026 | 23/06/2026      | https://docs.aws.amazon.com/elasticloadbalancing/                  |
| Wednesday | - Learn about Auto Scaling Group <br> - Understand Min Capacity, Desired Capacity, and Max Capacity <br> - Take notes on how Auto Scaling supports systems when traffic changes                                        | 24/06/2026 | 24/06/2026      | https://docs.aws.amazon.com/autoscaling/                           |
| Thursday  | - Learn about Launch Template <br> - Relate Launch Template to the EC2 knowledge learned earlier <br> - Learn about Scaling Policy and CloudWatch Metrics used for Auto Scaling                                        | 25/06/2026 | 25/06/2026      | https://docs.aws.amazon.com/autoscaling/ec2/userguide/             |
| Friday    | - Summarize the basic model: User → Load Balancer → Target Group → EC2 Instances <br> - Review cost considerations when using Load Balancer and Auto Scaling <br> - Update Week 9 Worklog on the personal Hugo website | 26/06/2026 | 26/06/2026      | https://docs.aws.amazon.com/elasticloadbalancing/latest/userguide/ |

### Week 9 Achievements:

* Understood that Elastic Load Balancing is a service that distributes traffic to multiple backend resources such as EC2 Instances.

* Learned the role of Load Balancer in improving system availability and handling traffic more effectively.

* Became familiar with basic concepts in Application Load Balancer:

  * Listener
  * Target Group
  * Target
  * Health Check
  * Routing Rule

* Understood that Health Check helps the Load Balancer identify which backend resources are still operating normally.

* Understood that Auto Scaling Group can automatically adjust the number of EC2 Instances based on demand.

* Learned the meaning of basic Auto Scaling Group capacity settings:

  * Minimum Capacity
  * Desired Capacity
  * Maximum Capacity

* Understood that Launch Template is used to define the EC2 Instance configuration when Auto Scaling needs to launch new instances.

* Connected Auto Scaling knowledge with previous topics such as EC2, VPC, Security Group, and CloudWatch.

* Learned that CloudWatch Metrics can be used as a basis for scaling policies.

* Visualized a basic deployment model where a Load Balancer stands in front of multiple EC2 Instances.

* Became aware that Load Balancer and Auto Scaling may generate costs, so resources should be checked after practice.

* Completed Week 9 Worklog and updated the content on the personal Hugo website.
