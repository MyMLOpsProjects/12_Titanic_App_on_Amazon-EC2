# 12_Titanic_App_on_Amazon-EC2
Continuous deployment of FastAPI app on Amazon EC2
Follow the following steps for e2e App deployment in EC2 :

**After creating EC2 instance:**
- Install Docker on virtual machine / EC2 instance:
1. Open the terminal.
2. Remove any Docker files that are running in the system, using the following command:
sudo apt-get remove docker docker-engine docker.io
NOTE that we are using the sudo keyword along with commands.
Using sudo, users no longer had to change to the root user or log into that account to run administrative commands (such as installing software). Users could run those admin activities through sudo with the same effect as if they were run from the root user account.
3. Get the system up-to-date using the following commands.
It will update the package index files on the instance, which contain information about available packages and their versions.
Press enter, if a popup comes saying - Services will be restarted.
4. Install Docker using the following command:
sudo apt install docker.io -y
5. Start docker service and enable the service to start at boot using the following commands:
sudo systemctl start docker
sudo systemctl enable docker
6. Before testing Docker, check the version installed using the following command:
docker --version

**Add EC2 instance as a Self-hosted Github Runner:**
Follow [10_](https://github.com/MyMLOpsProjects/10_CI-CD_Docker_On_Test_Project)

- Run ./run.sh in EC2 cli terminal, it will start listening the job
- Trigger some code checkin to github repo
- CI and CD will be triggered
- Snapshots:
**- CI pipeline**
- <img width="1677" alt="image" src="https://github.com/MyMLOpsProjects/12_Titanic_App_on_Amazon-EC2/assets/90625369/ad793f92-fb9e-4663-ac6a-c6fc6d5e294b">
**- CD pipeline**
<img width="1245" alt="image" src="https://github.com/MyMLOpsProjects/12_Titanic_App_on_Amazon-EC2/assets/90625369/0ae19c60-fff8-4c37-966b-f542db86386c">

**EC2 runner logs:**
<img width="1097" alt="image" src="https://github.com/MyMLOpsProjects/12_Titanic_App_on_Amazon-EC2/assets/90625369/7fff87b2-db16-41ff-b9a6-a350d7df0313">

**- Titanic app running in browser:**
<img width="2042" alt="image" src="https://github.com/MyMLOpsProjects/12_Titanic_App_on_Amazon-EC2/assets/90625369/90a981f0-95e3-4d8f-a883-126b2cab1ae0">

_**Dont forget to delete all the jobs, instances in EC2 else unnecessary bill will be generated.**_

Done!!

