## How To Create An Ubuntu Server In Aws

Hello, everyone, I am *Shashikant* and in this article, I'm going to demonstrate, how you can create your own Linux server in AWS.

If you know what **AWS** is then it's good and if you don't know about what AWS is then here is a general intro of AWS for you.

**AWS** - It is basically a cloud service provider. That provides you with a large number of cloud services like computing, storage, database, networking, etc online.

Before heading forward there is a pre-requisite that you must have. 

An **AWS** account (**Must be under free tier if you want your server created for free**).

So if you have an aws account, then log in and open aws console.

## Steps

1. On aws management console search for EC2 and open it.
    ![5wSWzU73U.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587358274482/w6P_5c411.png)
2. Now on EC2 dashboard click on Launch Instance button.   
    ![z7IVf1G2f.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587358482958/_KwmFOzE-.png)
3. Now on Choose AMI window select Ubuntu Server 18.04LTS (HVM)
    ![ylNT96-6y.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587358590651/Ji54S7x4L.png)
    So here we are selecting **Ubuntu Server**. You can select any other Linux distro server according to your convenience. And remember, If you want your server under free tier, then select only those server in which the label of free-tier eligible is there.
4. Now on Choose Instance type window select t2.micro as it is free tier eligible and click on Next: Configure Instance Details button.
    ![NmfI85-bo.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587358683589/BjL9z_b3-.png)
    **Instance Types** is basically represents the different-different system configurations. So choose according to your requirements. But remember if you want your server under free tier use instance type with the free-tier tag only.
5. Now on Configure Instance window leave it as it is and click on Next: Add Storage button.
    ![39IAgBsfE.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587358780882/fz3etA-ID.png)
    You don't need to disturb these settings.
6. Now on Add Storage window, you can change storage up to 30 GB as it is free tier eligible and then click on Next: Add Tags button.
    ![EA3vraq_l.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587358864900/Z4G7UGyFA.png)
    You can add storage according to your use.
7. You can leave Add Tags window default as it is not needed that much and click on Next: Configure Security Groups button.
    ![8-UCwo8qU.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587358957716/dh4fhsi8O.png)
    You can add tags to a server, to categorize them.
8. Now here on Configure Security Group window change the *ssh* source to anywhere to access it from anywhere in the world. You can also restrict *ssh* access to your IP address from the source option. After that click on Review and Launch button. 
    ![7QYqkg70m.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587359033859/3kY_oRb6i.png)
    Ok talking about security groups. It is one most important setting because it decides your server openness to the world. You want to host your web application in the server that you also have to allow *HTTP* and  *HTTPS* in security groups.
9. In Review window you can see all details related to your server that you are going to launch. Now press the Launch button.
    ![j1ZLVTzJX.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587359102515/Ja9vmpBoj.png)
    Now just preview all the configuration of your server before final launch.
10. Key pair is used to connect to your server or if I say your ec2 instance. So you can select the option Create a new key pair and give that key pair a name and click on the checkbox and firstly download the key pair and then click on Launch Instances button.
    ![iUdNRbDq7.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587359177847/lXs-oRpcx.png)
11. Finally, your server has been launched. Now click on View Instance button.
     ![7azke8raU.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587359242705/1hK-rSMbw.png)
12. Now place your downloaded private key file or key pair into a safe location and open the terminal on that location. After opening terminal restrict access to the private key file by change mode command.
    ```shell
    chmod 400 key_filename.pem
    ``` 
    ![119Bx1nnK.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587359377913/VeuwnFdrf.png)
13. Now open your Instances window again and see if Instance State is running or not. If Instance state is running then copy the IPv4 Public IP and open terminal again in the same location. And types this command to connect to your ubuntu server 
    ```shell
    ssh -i key_filename.pem user-name@your-server-ip
    ```
    In ubuntu server by default username is `ubuntu` so your command will be
    ```shell
    ssh -i key_filename.pem ubuntu@your-server-ip
    ```
    ![ex-UaEm0m.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587359489977/rm86fBcTr.png)
14. Now if asked for yes or no type yes.
      ![pBWhU5noP.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587359530410/kgXcUoeg6.png)
15. Now finally you are connected to your ubuntu server.
     ![CbNMQWP36.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587359792126/FieO8qBNX.png)
16. You can type `exit` to disconnect for the server and if you want to close the server permanently go to Instances on aws management console and select the server, and then press Actions button in which press on Instance State in which press Terminate.
     ![pHnOKHMoa.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1587359828144/cEooGkAYz.png)

And that's it. This is how you can create a Linux server on aws.
If you have any problem you can ask me in the comment section.
