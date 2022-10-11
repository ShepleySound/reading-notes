# Class 16 - AWS: Cloud Servers



### What is an EC2 Instance?  

An EC2 instance is a virtual machine created using AWS. It is classified as Infrastructure as as Service (IaaS). The instances are scalable, and they offer many flexible options.

### Name 2 use cases for EC2.  
EC2 has many basic use cases, such as hosting a simple web server. At it's core, it can be just a virtual machine with an operating system and networking capabilities. Some of the uses that Amazon points out are running cloud-native applications and training/deploying machine learning application.

### Provide 1 reason to use ECS instead of Heroku.  
Heroku may be very easy to use, but that comes with limitations. If an app becomes complex, there may be things that need configuring that Heroku just doesn't give you access to. Using EC2/ECS may be more difficult and take more time to spin up a working deployment, but in the end you'll have more control over the environment your application runs in.

### Where can we find EC2 on the AWS Console?

If it is not in the "Home" section, it can be found under "Compute" in the AWS Console.

### Explain the general difference between T2 Micro and XL.  

A t2.micro instance has 1 vCPU while t2.xlarge has 4 vCPUs. A vCPU is essentially a software version of a single CPU core. t2.micro comes with 1.0GB of RAM, and t2.xlarge comes with 16.0GB of RAM.  
One of the important differences is also their CPU Credits/hr. These are defined as a unit of vCPU-time.

>Examples:
>
>1 CPU credit = 1 vCPU * 100% utilization * 1 minute.
>
>1 CPU credit = 1 vCPU * 50% utilization * 2 minutes
>
>1 CPU credit = 2 vCPU * 25% utilization * 2 minutes

### What is Elastic Beanstalk?

Elasic Beanstalk is a Platform as a Service (PaaS) that manages the deployment of an application. It uses existing AWS services and helps developers manage things like scaling, load-balancing, and database administration.

### Describe the relationship between EC2 and Elastic Beanstalk.

Elastic Beanstalk uses AWS services, and EC2 is one of those services. Depending on your application's needs, EB will decide which EC2 instances need to be spun up and maintained to keep the application running.

### Name some benefits of using Elastic Beanstalk. 
Elastic Beanstalk can make a developer's life much easier. Rather than worrying about spinning up servers and managing load-balancers, the developer can write code, push it over to EB, and feel confident that the deployment should work. Of course, it's not 100% fool-proof, but for many use-cases it can make the development life-cycle much faster.