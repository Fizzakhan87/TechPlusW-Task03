# TechPlusW-Task03
Manually And Automatically Deployment Application process on AWS

Documented different steps of Deployment Application process steps are given:
* First Launch the Instance on AWS and connect the Instance, paste the ssh key on git bash, command 'git clone' to clone the repository on my local instance.
* Manually Steps are done than move to install the dependancies such as python3 pip, django on locally
* Migrate the Data 'python3 manage.py migrate' Run the server Application locally 'python3 manage.py runserver'
* Before running the port set, set port on AWS Security Group, go to AWS Security Groups, edit inbound rules, Add a new rule for set port '8001' with the source set to Anywhere, and then save the rule.
* Then go to the settings.py file on gitbash Allowed host ['*']
* Running the server on background 'nohup python3 manage.py runserver 0.0.0.0:8001' , Succesfully Application todolist run on web server.
* Using Docker to deploy the Application on AWScto run the different commands like:
   "FROM python:3" > Dockerfile
   "RUN pip3 install django" >> Dockerfile
   "COPY . ." >> Dockerfile
   "RUN python manage.py migrate" >> Dockerfile
   'CMD ["python", "manage.py", "runserver", "0.0.0.0:8001"]' >> Dockerfile 
* Finally the Application is Successfully Deploy on Web Server. 
