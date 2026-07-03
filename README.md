# Deploying the microservices application by using load balancer and autoscaling Group

## Introduction

Microservices architecture is a software development approach where an application is divided into small
independent services. In this project, the microservices application is deployed on AWS using an Application Load Balancer and Auto Scaling Group.

The Load Balancer distributes incoming traffic across multiple EC2 instances to improve performance and availability, while the Auto Scaling Group automatically increases or decreases instances based on traffic demand. This deployment provides scalability, fault tolerance, high availability, and efficient resource
utilization in the cloud environment.

## Architecture Diagram

![alt text](<Images/Architecture Dia.png>)

## Create Launch Templates

### Steps

1. Open EC2 Dashboard.
2. Select Launch Templates.
3. Click Create Launch Template.
4. Configure AMI, Instance Type, Security Group, and Key Pair.
5. Save the template.

![alt text](<Images/Screenshot (421).png>)

![alt text](<Images/Screenshot (425).png>)

![alt text](<Images/Screenshot (426).png>)

![alt text](<Images/Screenshot (429).png>)

![alt text](<Images/Screenshot (430).png>)

![alt text](<Images/Screenshot (433).png>)

![alt text](<Images/Screenshot (434).png>)

![alt text](<Images/Screenshot (435).png>)

![alt text](<Images/Screenshot (444).png>)

![alt text](<Images/Screenshot (450).png>)

![alt text](<Images/Screenshot (456).png>)

![alt text](<Images/Screenshot (458).png>)

## Step 2: Create a New Target Group

- Click **Create Target Group**.
- Choose **Instances** as the target type.
- Enter a Target Group Name (e.g., target-group-1).
- Select **HTTP** as the protocol.
- Set Port to **80**.
- Select your VPC.

![alt text](<Images/Screenshot (460).png>)

![alt text](<Images/Screenshot (464).png>)

![alt text](<Images/Screenshot (469).png>)

## Create Auto Scaling Groups

### Steps

1. Open Auto Scaling Groups.
2. Click Create Auto Scaling Group.
3. Select the Launch Template.
4. Configure Desired, Minimum, and Maximum Capacity.
5. Create the Auto Scaling Group.


![alt text](<Images/Screenshot (473).png>)

![alt text](<Images/Screenshot (474).png>)

![alt text](<Images/Screenshot (476).png>)

![alt text](<Images/Screenshot (477).png>)

![alt text](<Images/Screenshot (478).png>)

![alt text](<Images/Screenshot (479).png>)

![alt text](<Images/Screenshot (481).png>)

![alt text](<Images/Screenshot (482).png>)

## Create Application Load Balancer and Add rules

### Steps

1. Open EC2 Dashboard and select **Load Balancers**.
2. Click **Create Load Balancer** and choose **Application Load Balancer**.
3. Enter a name and select **Internet-facing**.
4. Choose Availability Zones and subnets.
5. Configure the Security Group to allow HTTP traffic.
6. Attach the Target Group.
7. Review the configuration and click **Create Load Balancer**.
8. Verify the application using the Load Balancer DNS name.


![alt text](<Images/Screenshot (484).png>)

![alt text](<Images/Screenshot (489).png>)

![alt text](<Images/Screenshot (490).png>)

![alt text](<Images/Screenshot (496).png>)

![alt text](<Images/Screenshot (501).png>)

### Output

- Application Load Balancer was successfully created and configured.
- Traffic was distributed across multiple EC2 instances.
- The Load Balancer routed requests to the appropriate Target Group.
- High availability and fault tolerance were achieved.
- The application was accessible through the Load Balancer DNS endpoint.


![alt text](<Images/110.png>)

![alt text](<Images/111.png>)

![alt text](<Images/112.png>)
