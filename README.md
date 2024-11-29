# foundry-tf-multi-env

[Cookiecutter](https://www.cookiecutter.io/) template to generate a basic multi-environment Terraform
project.

## Pre-requisites

```sh
pip install pipx
```

## Run

```sh
pipx run cookiecutter gh:Particle41/foundry-tf-multi-env
```

## Configurations

**TODO:** add more info

### Terraform bootstrap

Use the CloudFormation templates in the [cf/]({{cookiecutter.project_name}}/cf) directory to bootstrap the Terraform configuration:

- [tf-remote-state.yaml]({{cookiecutter.project_name}}/cf/tf-remote-state.yaml): deploy the resources for Terraform remote state in the shared services account
- [workload-role.yaml]({{cookiecutter.project_name}}/cf/workload-role.yaml): deploy as a stack set on the management AWS account to create workload roles in each account, which can be assumed from the shared services initial IAM role

### CI/CD bootstrap

Check this file and follow the instructions in the comments: [envs/shared/ci-iam-bootstrap.tf]({{cookiecutter.project_name}}/envs/shared/ci-iam-bootstrap.tf)
