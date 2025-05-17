#terraform

Terraform relies on plugins called "providers" to interact with remote systems (e.g. `gcs`).

Plugins usually are retrieved from the [Terraform Registry](https://registry.terraform.io/providers/hashicorp/google/latest)

## Provider Requirements
Required Providers can be configured in the top level `terraform` block of the config:

```terraform
terraform {
  required_providers {
    mycloud = {
      source  = "mycorp/mycloud"
      version = "~> 1.0"
    }
  }
}
```

The `source` defined where terraform can find the plugin. The `version` defines the version. Every plugin also has a local name (`mycloud` in this example)

## Configuring Providers
Provider configurations belong in the root module of a Terraform configuration.

Configuration is created using a `provider` block:

```hcl
provider "google" {
  project = "acme-app"
  region  = "us-central1"
}
```

The name given for the provider (`google` in this example) is the local name of a provider that should already be defined in `required_providers` in the terraform block.