Check if kubernetes is up and running(It can take some time):

`kubectl cluster-info`{{execute}}

Install terraform cli:

`curl -fsSL https://apt.releases.hashicorp.com/gpg | sudo apt-key add -`{{execute}}

`sudo apt-add-repository "deb [arch=amd64] https://apt.releases.hashicorp.com $(lsb_release -cs) main"`{{execute}}

`sudo apt-get update && sudo apt-get install terraform`{{execute}}