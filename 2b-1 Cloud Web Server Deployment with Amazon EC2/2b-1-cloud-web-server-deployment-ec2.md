# Lab 2b-1: Cloud Web Server Deployment with Amazon EC2

## Configuring EC2 Instance in AWS and installing Apache Web Server

![Configuring storage](./images/ec2-configure-storage.png)

Configuring storage

![Network Settings – setting ssh and http inbound rules](./images/ec2-security-group-inbound-rules.png)

Network Settings – setting ssh and http inbound rules

![Instance is created successfully](./images/ec2-instance-created-successfully.png)

Instance is created successfully

![Instance details](./images/ec2-instance-details-public-ip-dns.png)

Instance details – I have a public ipv4 address and a public DNS (Domain Name Service) which I use to test the Apache Web Server

![Instance is running successfully](./images/ec2-instance-running-successfully.png)

Instance is running successfully

![SSH connect command](./images/ec2-ssh-connect-command.png)

![SSH Access on my laptop's window powershell is successful](./images/ec2-ssh-access-powershell-success.png)

SSH Access on my laptop's window powershell is successful

![Confirming that Apache has been installed successfully on the server](./images/apache-installed-confirmation.png)

Confirming that Apache has been installed successfully on the server

![Apache Web Page](./images/apache-default-web-page.png)

Apache Web Page

![Viewing the page source before modification](./images/apache-index-source-before-edit-nano.png)

Viewing the page source of the Apache2 default page using Nano text editor. Before modification

![After modifying the index file](./images/apache-index-source-after-edit-nano.png)

After modifying the index file and personalizing it using Nano

![Reloading the browser – edits reflected](./images/apache-page-edit-reflected-browser.png)

Reloading the browser (in my own computer) – the edits made on the page source are reflected on the web browser

![Successful download of file from the web using wget](./images/wget-file-download-success.png)

Successful download of file from the web using wget

![Sudo cp command showing the file was copied to /var/www/html](./images/sudo-cp-file-to-var-www-html.png)

Sudo cp command showing the file was copied to /var/www/html

![ls output confirming that the pdf has been saved to /var/www/html successfully](./images/ls-confirm-file-var-www-html.png)

ls output confirming that the pdf has been saved to /var/www/html successfully

![Adding a hyperlink pointing to the file on the apache web browser](./images/apache-hyperlink-added-source.png)

Adding a hyperlink pointing to the file on the apache web browser

![Hyperlink added successfully on the Apache Web browser](./images/apache-hyperlink-added-browser.png)

Hyperlink added successfully on the Apache Web browser

![Successful viewing of the file by clicking on the hyperlink](./images/apache-hyperlink-file-view-success.png)

Successful viewing of the file by clicking on the hyperlink

![Public IP access via Edge browser](./images/apache-public-ip-access-edge-browser.png)

I used edge and entered the public ip address of my instance. This proves that my server is genuinely accessible to the public

![Instance stopped successfully](./images/ec2-instance-stopped.png)

Stopped the instance after I completed the lab. Can see that the instance has been stopped successfully and it isn't anymore.

## Enabling Budget Monitoring for my Instance

![Billing and Cost Management Dashboard](./images/aws-billing-cost-management-dashboard.png)

Billing and Cost Management Dashboard

![Zero spend budget template](./images/aws-budget-zero-spend-template.png)

![Configuring alerts to be sent to my email](./images/aws-budget-alert-email-configuration.png)

Using the zero spend budget template and configuring alerts to be sent to my email. I will get an email notification on how much money I spend on this instance so I can keep track of my usage better.

![Budget list created successfully](./images/aws-budget-list-created.png)

Budget list created successfully!

![Email has been linked to my budget list](./images/aws-budget-email-linked.png)

Email has been linked to my budget list
