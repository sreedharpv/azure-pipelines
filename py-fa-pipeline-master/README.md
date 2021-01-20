# Python Function App Container Demo Project 
Project Name: py-fa-pipeline

## Prerequisite : 
    Provisioning the following azure resources through azure portal or any(ARM, Azure-cli and Terraform)
	    Create Free Subscription or Any               :  My Free Tier Account 
	    Resource Group
		Function App Resource Group               :  function-app-group
		Sonar Resource Group                      : SonarRG
	    Storage Account                               :  funcppstorage
	    Function App Container Environments                
		Dev Function App Container Environment    :  func-app-container
		Test Function App Container Environment   :  test-func-app-container
		Prod Function App Container Environment   :  prod-func-app-container

## Create CI/CD Azure Pipeline to use Azure Devops Portal
	Azure pipeline for continuous integration
		Ex: azyre-pipeline.yml(project root folder)
	Release pipeline for continuous Deployment 
		 Navigation in azure devops portal (Org --> project -->pipeline --> release
		 Ex: devops-pipelines --> py-fa-demo --> pipeline-releases-release-10, Refer the below image part of release Continuous deployment section.
		
## Continuous Integration through Azure Pipeline
	Part of continuous integration build follows the below stages 
        Sonarqube (code quality analyser to prepare, analyse and publish)  
        Build an docker image and publish to azure container registry 
## Sonar report 

<img width="1539" alt="Screenshot 2021-01-10 at 16 30 56" src="https://user-images.githubusercontent.com/76499386/104128798-7e402c00-5361-11eb-8b4c-c8c8c05c506f.png">

## CI Build stage

 <img width="1680" alt="Screenshot 2021-01-10 at 10 13 46" src="https://user-images.githubusercontent.com/76499386/104121197-61d9ca80-5334-11eb-8d60-4463442af295.png">

## Continuous Deployment through Release Pipeline
	Part of continuous deployment build follows the below stages.	      
		Deploy the py-fa-demo container image to development environment with post approval
		Deploy the py-fa-demo container image to test environment with pre and post approval
		Deploy the py-fa-demo container image to prod environment with pre approval

 <img width="1678" alt="Screenshot 2021-01-10 at 10 44 23" src="https://user-images.githubusercontent.com/76499386/104121111-d829fd00-5333-11eb-956e-3bce490ebb88.png">

