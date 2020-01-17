## How To Create An Ubuntu Server In Aws

Hello everyone I am *Shashikant* and in this article I'm going to demonstrate, how you can create your own Linux server in aws.

If you know what **aws** is then it's good and if you don't know about what aws is then here is a general intro of aws for you.

**AWS** - It is basically a cloud service provider. That provides you a large number of cloud services like computing, storage, database, networking etc online.

Before heading forward there is a pre-requisite that you must have. 

An **aws** account (**Must be under free tier, if you want your server created for free**).

So if you have an aws account, then login and open aws console.

### Steps

1. On aws management console search for EC2 and open it.  
![1.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579102262077/5wSWzU73U.png)

2. Now on EC2 dashboard click on Launch Instance button.
![2.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579102279121/z7IVf1G2f.png)

3. Now on Choose AMI window select Ubuntu Server 18.04LTS (HVM)
![3.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579102293695/ylNT96-6y.png)
 So here we are selecting **Ubuntu Server**. You can select any other linux distro server according to your convenience. And remember, If you want your server under free tier, then select only those server in which the label of free-tier eligible is there.

4. Now on Choose Instance type window select t2.micro as it is free tier eligible and click on Next: Configure Instance Details button. 
![4.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579102312463/NmfI85-bo.png)

 **Instance Types** is basically represents the different-different system configurations. So choose according to your requirements. But remember if you want your server under free tier use instance type with the free-tier tag only.

5. Now on Configure Instance window leave it as it is and click on Next: Add Storage button  
![5.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579102328065/39IAgBsfE.png)
You don't need to disturb these settings.

6. Now on Add Storage window you can change storage up to 30 GB as it is free tier eligible and then click on Next: Add Tags button.  
![6.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579102344368/EA3vraq_l.png)
 You can add storage according to your use.

7. You can leave Add Tags window default as it is not needed that much and click on Next: Configure Security Groups button.  
![7.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579102358253/8-UCwo8qU.png)
You can add tags to server, to categorize them.

8. Now here on Configure Security Group window change the *ssh* source to anywhere to access it from anywhere in the world. You can also restrict *ssh* access to your ip address from the source option. After that click on Review and Launch button.  
![8.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579102370275/7QYqkg70m.png)
Ok talking about security groups. It is one most important setting, because it decides your server openness to the world. You you want to host your web application in the server that you also have to allow *HTTP* and  *HTTPS* in security groups.

9. In Review window you can see all details related to your server that you are going to launch. Now press Launch button.   
![9.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579102380618/j1ZLVTzJX.png)
 Now just preview all the configuration of your server before final launch.

10. Key pair is used to connect to your server or if I say your ec2 instance. So you can select the option Create a new key pair and give that key pair a name and click on the checkbox and firstly download the key pair and then click on Launch Instances button. 
![10.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579102391228/iUdNRbDq7.png)

11. Finally your server has been launched. Now click on View Instance button.
![11.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579102408743/7azke8raU.png)

12. Now place your downloaded private key file or key pair into a safe location and open the terminal on that location. After opening terminal restrict access to the private key file by change mode command 
    ```
    chmod 400 key_filename.pem
    ```
![12.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579102422991/119Bx1nnK.png)

13. Now open your Instances window again and see if Instance State is running or not. If Instance state is running then copy the IPv4 Public IP and open terminal again in the same location. And types this command to connect to your ubuntu server 
    ```shell
    ssh -i key_filename.pem user-name@your-server-ip
    ```
    In ubuntu server by default username is `ubuntu` so your command will be
    ```shell
    ssh -i key_filename.pem ubuntu@your-server-ip
    ```
![13.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579102480592/ex-UaEm0m.png)

14. Now if asked for yes or no type yes.    
![15.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579102495179/pBWhU5noP.png)

15. Now finally you are connected to your ubuntu server.
![16.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579102505682/CbNMQWP36.png)

16. You can type `exit` to disconnect for the server and if you want to close the server permanently go to Instances on aws management console and select the server, and then press Actions button in which press on Instance State in which press Terminate.
![17.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1579102515978/pHnOKHMoa.png)

And that's it. This is how you can create an linux server on aws.

If you have any problem you can ask me in the comment section.