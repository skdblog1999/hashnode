## How To Host Flask Website Using Apache On Ubuntu Server In AWS

Hello everyone in this article, I am going to demonstrate how you can host flask website on ubuntu server in aws.

## Prerequisite

1. To get started with this article you must have an running ubuntu server in aws. If you don't have one than follow this article.

 %[https://shashikant.xyz/how-to-create-an-ubuntu-server-in-aws-ck5fh509502iiqps1o030txkg]

2. If you have fulfilled the first requirement, than you can setup and configure apache on your linux server. Here's the link to the article if you don't know how to setup apache on linux server.

 %[https://shashikant.xyz/how-to-install-and-configure-apache-on-your-linux-server-ck5jmdspn03y1qps1rv005akc]

So, if you get completed with all the above prerequisite, move to the following steps

## Steps

1. First download and setup the python environment using miniconda for your project.
 
 ```shell
mkdir downloads && cd Downloads
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
chmod 777 Miniconda3-latest-Linux-x86_64.sh
./Miniconda3-latest-Linux-x86_64.sh
``` 
Then load the remote terminal again so that the changes take place

 ```shell
source ~/.bashrc
```
Now create python environment for your project.
 ```shell
conda create -n <project_name> python flask <other_libraries>
```
Replace `<project_name>` with your project name and `<other_libraries>` with the libraries you want to install as per your project requirement.
So you are all setup with the python environment.

2. Now install `mod_wsgi` package that is required to host flask application.
 ```shell
sudo apt-get install libapache2-mod-wsgi
```

3. Now setup your project and your project tree structure must be like
 ```shell
project_name/
      project_name.wsgi
      project_name/
          app.py
          static/
          templates/
```
So now if you have arranged your project structure like above, then move to the next part to create the `project_name.wsgi` file

4. So insert these lines in the `project_name.wsgi` file and remember to replace the `project_name` with your original project name.
 
 %[https://gist.github.com/skdblog1999/3dba52f8773c616c745dd48ed130b35b]

  If you are done with the wsgi configuration file, move toward next step.
5.  In this step we are going to create the configuration file for our project. Use the below command to create the file

 ```bash
sudo vim /etc/apache2/sites-available/<project_name>.conf
```
Replace the `<project_name>` with your project name.
Now insert the following content in the file
 
 %[https://gist.github.com/skdblog1999/4f80e745f9f1de2e1e9d6fa7b89fc69b]

 Here replace the `<project_name>` with your project name and `<version>` with the python version in the python miniconda environment. And also `<your-server-name-or-domain-name>` with your domain name or the IP address of your server.

 You are just about to host your flask website, only some of the steps are remaining.

6. Now enable site and reload apache server.

 ```bash
sudo a2ensite <project_name>.conf
sudo systemctl reload apache2
```


Now you are all setup. You have successfully hosted your flask website.
To check open the domain name or IP address (that you used in configuration file ) in the browser.


Hope you have successfully hosted your flask application by using these steps and if you have any problem or if you are unable to host the flask application you can ask me in the comment section for help.









