## How To Install And Configure Apache On Your Linux Server

Hello everyone I am *Shashikant* and in this article I'm going to demonstrate, how you can setup an apache on your linux server. 

Apache is use to create a HTTP server, in which we host our web applications.

So before heading toward the procedure there are some prerequisite that you must have. The prerequisite are  -

+ . Linux server (ubuntu server - recommended)

If you don't have an linux server, you can create a one for you from aws. Go through this article to create an linux server.

https://shashikant.xyz/how-to-create-an-ubuntu-server-in-aws-ck5fh509502iiqps1o030txkg

If you have all the prerequisite things then let's move on to the steps.

### Steps

1. Firstly connect to your ubuntu server. For this open Instances tab on your EC2 dashboard in aws account and copy the IPv4 public ip. Then open your terminal and types this command
   ```ssh
   ssh -i private-key.pem ubuntu@your-public-ip
   ```
 ![1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579253481704/q2CDi3YG1.png)
  
 ![3.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579253490848/-rgN3lKIh.png)

  ![4.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579253500734/O9MMGBc0A.png)

2. Now update and upgrade your linux server by using commands
   ```ssh
   sudo apt-get update
   sudo apt-get upgrade
   ```
![5.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579253511034/EkjSizNHk.png)
 ![6.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579253519604/7c_Jr5V9W.png)

3. Now install apache server using command
   ```ssh
   sudo apt-get install apache2
   ```
![7.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579253528053/dsOMk3QVG.png)

4. Now check if firewall is enabled or not if not enabled then enable it by command
   ```ssh
   sudo ufw status
   ```
   If this shows `status: inactive` . Then allow it by command
   ```ssh
   sudo ufw enable
   ```
![8.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579253539449/2moL0T_hW.png)
![10.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579253546863/Oqc-kh1k4.png)

5. Now enable apache and ssh in ufw by commands
   ```ssh
   sudo ufw allow 'Apache Full'
   sudo ufw allow '22'
   ```
![11.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579253557877/lv6GOoA76.png)
![12.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579253566797/g3ywdriPe.png)

6. Now from server all things are configure now its time to do some changes from EC2 dashboard in aws dashboard.

7. Open security groups from EC2 instance tab.
![13.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579253576998/dV2sRnV4U.png)

8. Now open Inbound tab and press edit button.
![14.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579253588124/BoKpdmGWL.png)

9. Now just add HTTP rule and make it available from everywhere and save this configuration.
![15.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579253597031/ZZ_ft_l3b.png)

10. Now just copy your server public ip and paste it into the browser.
![16.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579253606021/qGQMR2q3E.png)

So just by following these 10 steps you can easily setup a apache server.

If you have any problem you can ask me in the comment section.

