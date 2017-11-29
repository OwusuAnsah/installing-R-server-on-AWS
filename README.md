# Install and run R, RStudio Server, and Shiny Server on Amazon EC2
<h3>A quick overview on how to install and run R, R Studios server on Amazon Web Services Cloud</h3>
In this tutorial, we will focus on the following;
<ul>
  <li>Choosing an AMI for R</li>
  <li>Choosing an Insatance type for R</li>
  <li>Configuring Instance Details</li>
  <li>Configuring Security Group</li>
  <li>Configuring Shiny Server</li>
</ul>
<hr>
<ol>
  <li><b>Choosing an AMI for R</b></li>
  First and foremost, you need to launch an EC2 instance and to do that, you have to choose an AMI, In this tutorial, we'll be using the <a href="https://aws.amazon.com/amazon-linux-ami/">Amazon Linux AMI</a> since it has a stable version of R in its repository.
  NB: Starting a server on AWS—called an EC2 instance to know more about how to go about launching an instance <a href="http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html">click here<a>
  <li><b>Choosing an Insatance type for R</b></li>
  Choose an EC2 instance type that matches the data size and processing that your analysis requires. By default, R runs only on one core node and, in many cases, requires a lot of memory.

For programming and development, the general-purpose T2 instance types are sufficient and cheap, and t2.micro is available through the <a href="https://aws.amazon.com/free/">AWS Free Tier.<a><br>
  Details of more <a href="https://aws.amazon.com/ec2/instance-types/">instance types</a>
  <li><b>Configuring Instance Details</b></li>
  To configure the instance maintain the default options and pass in user data to perform automated tasks and in this instance, we pass in scripts to install R and Shiny server which helps create interactive dashboards.<br>
  <img src="https://github.com/OwusuAnsah/installing-R-server-on-AWS/blob/master/R_Best_Practices_Image_2.png">
  <li><b>Configuring Security Group</b></li>
  In the EC2 launch wizard, you define a security group, which acts as a virtual firewall that controls the traffic for one or more instances. For your R-based analysis environment, you have to open up port 8787 for RStudio Server and port 3838 for Shiny Server.
  <img src="https://github.com/OwusuAnsah/installing-R-server-on-AWS/blob/master/r-update-1.gif">
  <li><b>Configuring Shiny Server</b></li>
</ol>
 Once running, you can connect to your instance through an SSH client, in this case PuTTY using primary key generated.
You can connect using a web browser to RStudio Server and R. For login credentials, use the newly created user and password.

This is an example of a URL format which will be used to access the launched server on the internet:
http://ec2-52-49-144-46.eu-west-1.compute.amazonaws.com:8787

