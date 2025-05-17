#terraform 

_Resources_ are the most important element in the Terraform language. Each resource block describes one or more infrastructure objects, such as virtual networks, compute instances, or higher-level components such as DNS records.

## Syntax
A `resource` block declares a resource of a specific type with a local name (the name is used as a reference by terraform but not used outside the module)

```
resource "aws_instance" "web" {
	// config here
}
```

In this case, the `aws_instance` resource is named `web`.

## Config documentation
Each resource has their own documentation, usually found in the registry

