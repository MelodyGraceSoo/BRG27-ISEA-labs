## Configuring EC2 Instance in AWS and installing Apache Web Server

![](./images/image1.png)

Configuring storage

![](./images/image2.png)

Network Settings -- setting ssh and http inbound rules

![](./images/image3.png)

Instance is created successfully

![](./images/image4.png)

Instance details -- I have a public ipv4 address and a public DNS (Domain Name Service) which I use to test the Apache Web Server

![](./images/image5.png)

Instance is running successfully

![](./images/image6.png)

![](./images/image7.png)

SSH Access on my laptop's window powershell is successful

![](./images/image8.png)

Confirming that Apache has been installed successfully on the server

![](./images/image9.png)

Apache Web Page

![](./images/image10.png)

Viewing the page source of the Apache2 default page using Nano text editor. Before modification

![](./images/image11.png)

After modifying the index file and personalizing it using Nano

![](./images/image12.png)

Reloading the browser (in my own computer) -- the edits made on the page source are reflected on the web browser

![](./images/image13.png)

Successful download of file from the web using wget

![](./images/image14.png)

Sudo cp command showing the file was copied to /var/www/html

![](./images/image15.png)

ls output confirming that the pdf has been saved to /var/www/html successfully

![](./images/image16.png)

Adding a hyperlink pointing to the file on the apache web browser

![](./images/image17.png)

Hyperlink added successfully on the Apache Web browser

![](./images/image18.png)

Successful viewing of the file by clicking on the hyperlink

![](./images/image19.png)

I used edge and entered the public ip address of my instance. This proves that my server is genuinely accessible to the public

![](./images/image20.png)

Stopped the instance after I completed the lab. Can see that the instance has been stopped successfully and it isn't anymore.

## Enabling Budget Monitoring for my Instance

![](./images/image21.png)

Billing and Cost Management Dashboard

![](./images/image22.png)

![](./images/image23.png)

Using the zero spend budget template and configuring alerts to be sent to my email. I will get an email notification on how much money I spend on this instance so I can keep track of my usage better.

![](./images/image24.png)

Budget list created successfully!

![](./images/image25.png)

Email has been linked to my budget list
