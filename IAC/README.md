### Project Title - Deploy a high-availability web app using CloudFormation
This folder provides the necessary files for the "ND9991 - C2- Infrastructure as Code - Deploy a high-availability web app using CloudFormation" project. This folder contains the following files:


#### final-project-network.yml
CloudFormation code using YAML defining the network infrastructure.

#### final-project-network-parameters.json
Parameters used by final-project-network.yml

#### final-project-server.yml
CloudFormation code using YAML defining security groups, load balancer, auto scaling group

#### final-project-server-parameters.json
Parameters used by final-project-server.yml

#### create.sh
script used to create a new cloud formation stack in eu-central-1 region

usage: ./create.sh $1 $2 $3

- $1: stack-name
- $2: template body file
- $3: parameters file

#### update.sh
script used to update an existing cloud formation stack in eu-central-1 region

usage: ./update.sh $1 $2 $3

- $1: stack-name
- $2: template body file
- $3: parameters file


#### delete.sh
script used to delete a cloud formation stack

usage: ./delete.sh $1

- $1: stack-name


### deployment

#### deploy the network
- ./create.sh UdacityProjectNetwork final-project-network.yml final-project-network-parameters.json
#### deploy the web app
- ./create.sh UdacityProjectServer final-project-server.yml final-project-server-parameters.json