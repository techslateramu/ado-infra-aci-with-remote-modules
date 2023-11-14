# Introduction

- This project contains few terraform resources ( for ex: resource group and container instance )
- There is ADO pipeline written ( use Azure DevOps to run Pipeline)
- Make sure to follow pre-requisites to create stroage account

# Pre-requisites
 - Make sure to create a storage account, since we store terraform statefile into storage account.
 - Whatever the storage account details, please store them into these as group variables.
 - Create a group variable called 'common' and have all the below varialbes stored there

  ![Common](./img/common.png)

 * ARM_CLIENT_ID
 * ARM_CLIENT_SECRET
 * ARM_TENANT_ID
 * ARM_SUBSCRIPTION_ID

 * tf_state_rg_name
 * tf_state_rg_name
 * tf_state_st_cont_name
 * tf_state_subscription_id
 * tf_state_tenant_id

# Folder Structure
- Modules - which contains modules of terraform
- Pipeline - this folder contains pipeline
- Terraform - this folder contains actual terraform project files ( main.tf, var.tf, provider.tf, backend.tf)

# Pipeline
- Pipeline contains 4 steps, terraform init, validte, plan, apply 
- Make sure to set env variables ( including terraform backend variables) - pls see pre-requisites for more info.