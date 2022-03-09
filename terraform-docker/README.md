# terraform docker

Provider docs: [link](https://registry.terraform.io/providers/kreuzwerker/docker/latest/docs)

## Basic Operations

- `terraform apply`
- `terraform plan`
- `terraform destroy`

## Terraform plan

- `terraform plan -out=plan1`
- Good for automation - will directly apply without confirmation
- `terraform apply plan1`
- To destroy: `terraform plan -destroy`

# Terraform State
- `terraform destroy --auto-approve` - wont ask confirmation
- file `terraform.tfstate` keeps recording state changes
- `terraform.tfstate.backup` keeps last state
- View current state: `terraform show -json | jq`
- Listing resources: `terraform state list`

# Outputs / console
- CLI: `terraform console`
    - can type things like `docker_container.name`
- Better: add outputs in tf file
    - or type `terraform output`