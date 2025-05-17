#terraform 

_Data sources_ allow Terraform to use information defined outside of Terraform, defined by another separate Terraform configuration, or modified by functions.

```
data "aws_ami" "example" {
	// config here
}
```

Similar to [[Terraform Resources]], Terraform requests data from a given data source (`aws_ami`) and exports it under a name (`example`)