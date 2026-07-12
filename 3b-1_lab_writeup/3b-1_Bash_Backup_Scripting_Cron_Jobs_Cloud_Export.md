# 3b-1 Bash Backup Scripting, Cron Jobs & Cloud Export – Lab walkthrough and screenshots

![](./images/image1.png)

Adding basic calculations and echo variables in the script

![](./images/image2.png)

Executing the script and seeing the results of the calculations performed by the script

![](./images/image3.png)

Making testfolder, creating the files and adding the files to the testfolder

![](./images/image4.png)

Ls -r output showing test files and testfolder created in /home/melody/Documents

![](./images/image5.png)

Creating the backup script -- using echo

![](./images/image6.png)

script initiated successfully -- can see the content of the backup script that I created

![](./images/image7.png)

Adding timestamp to the filename

![](./images/image8.png)

the date and time is printed successfully

![](./images/image9.png)

Creating the ZIP Archive with Date Filename

![](./images/image10.png)

Setting permissions and testing the script again

![](./images/image11.png)

Making the script globally accessible

![](./images/image12.png)

Scheduling the testscript to run every hour by using a cron job to automate it

![](./images/image13.png)

Using SCP to transfer the files from my Ubuntu VM to the remote server (Amazon EC2 instance)

After that, I connected to my instance using ssh. In this screenshot, ssh is successful, so I am currently inside the Ec2 instance

![](./images/image14.png)

Using ls to verify that the backup_.zip folder has been transferred successfully

![](./images/image15.png)

Adding all the commands I did previously into the testscript so that I can automate it without retyping the commands physically each time.

![](./images/image16.png)

![](./images/image17.png)

After initiating the script, a new zip folder is created on the VMware

![](./images/image18.png)

I logged into the my EC2 instance via ssh to check if the zip folder has been copied successfully. Using ls -la, I can see that the new zip folder has been copied to the EC2 instance

![](./images/image19.png)

Using /var/log/syslog to verify that the cron job executed automatically every hour as melody user
