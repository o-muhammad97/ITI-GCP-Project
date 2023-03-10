# ITI-GCP-Project

## Tools used to build the project
> - Terraform
> - Google Cloud Platform Services and APIs (GCP Services & APIs)
> - Docker

## Creating Infrastructure Using Terraform

### Network

- VPC that project will be assigned to
- 2 subnets attached to 2 different ips [(managment subnet) for VM and (restrecited subnet -for GKE]
- NAT Gateway and Router
- Firewall to allow SSH Connection

### Service Account (SA)

- Service accounts that are attached to VM and GKE cluster.
> - service account [vm:container.admin]
> - service account [GKE:(roles/storage.admin) and (iam.workloadIdentityUser)]

### VM  Contains 

- A VM isolated in a private subnet (without external ip)

### GKE  Contains  :

- Setting up GKE in private subnet
- Container Node Pool

## Images 

- Build 2 images on the local machine 1 for the python app and the other for radis pull this images from (docker hub) then build these images 
> - docker build -t <name> .

- Next step is push this 2 images into GCR by the following command :
> - [docker push gcr.io/< project id >/ < image name >]

## Apply Deployments To GKE

## Running Bash Script to automate Installing CLI, kubectl and deploy all Yaml-files into the VM:

>> File included in Terraform Folder and its name is script.sh


## Load Balancer
![LB](https://user-images.githubusercontent.com/50025855/215360028-98dbbfab-7610-4dbf-90ac-e70e6cc80f91.png)

## Bucket
![Bucket](https://user-images.githubusercontent.com/50025855/215360015-be623fb7-a72b-49b7-8718-a5d99cfefa38.png)

## Web app while up and run on the browser 
![Webapp_up_and_run](https://user-images.githubusercontent.com/50025855/215360020-de7bf7a2-fe14-4e55-ab64-a9d22a090230.png)
