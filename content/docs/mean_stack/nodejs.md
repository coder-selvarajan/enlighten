# Node JS

**Install NodeJS in CentOS**

```
curl --silent --location https://rpm.nodesource.com/setup_8.x | sudo bash -
sudo yum -y install nodejs
```

From <https://nodejs.org/en/download/package-manager/#enterprise-linux-and-fedora> 


**Install pm2 & http-server:**

    npm install -g -pm2 http-server
    OR
    npm install pm2@latest -g


**Install Yarn:**

    curl --silent --location https://dl.yarnpkg.com/rpm/yarn.repo | sudo tee /etc/yum.repos.d/yarn.repo
    sudo yum install yarn

From <https://yarnpkg.com/en/docs/install#centos-stable> 


**NodeJs Setup on Centos - Tut Video: **

	- https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/deployment
	- [Deploying Node.js App With PM2](https://www.youtube.com/watch?v=RF6Dzwwpduo)
    - https://www.youtube.com/watch?v=1nEJvN778j4


**NodeJs App deployment:**

	- Zip and copy the app files except node_modules folder
	- Run  npm install
	- pm2 start --name msd server.js
		○ pm2 ls
	- pm2 startup systemd -u edureka --hp /home/edureka   [run as root]
	- pm2 save
	
	Disable startup system: 
	- pm2 unstartup


**Test:** 

    $ echo "Hello World" > index.html
    $ http-server

**Pm2 Notes:**

- http://pm2.keymetrics.io/docs/usage/quick-start/
- http://pm2.keymetrics.io/docs/usage/startup/
- http://pm2.keymetrics.io/


**Configure NGinX:**

- https://www.youtube.com/watch?v=SlBe9c54GzA