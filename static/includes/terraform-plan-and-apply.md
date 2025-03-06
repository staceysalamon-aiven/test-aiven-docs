1. To initialize Terraform, run:

```sh
$ terraform init
```

The output is similar to the following:

```sh

Initializing the backend...

Initializing provider plugins...
- Finding aiven/aiven versions matching ">= 4.0.0, < 5.0.0"...
- Installing aiven/aiven v4.9.2...
- Installed aiven/aiven v4.9.2
...
Terraform has been successfully initialized!
...
```

1. To create an execution plan and preview the changes, run:

```sh
$ terraform plan

```

1. To deploy your changes, run:

```sh
$ terraform apply --auto-approve
```
