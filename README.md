# Terraform-gcp-labels
# Google Cloud Infrastructure Provisioning with Terraform

This Terraform module is designed to create structured labels for resources with specific attributes.

## Table of Contents

- [Introduction](#introduction)
- [Usage](#usage)
- [Module Inputs](#module-inputs)
- [Module Outputs](#module-outputs)
- [Examples](#examples)
- [License](#license)

## Introduction

The **"labels"** Terraform module allows you to define and manage labels for your resources in a structured manner. Labels are essential for resource organization and identification, and this module provides an easy way to create and manage them.

## Usage

You can use this module in your Terraform configuration like this:
## Example: _labels_
```hcl
module "labels" {
  source      = "git::https://github.com/cypik/terraform-gcp-labels.git?ref=v1.0.0"
  name        = "app"
  environment = "test"
  label_order = ["name", "environment"]
  attributes  = ["private"]
  extra_tags  = {
    Application = "Demo"
  }
}
```
Please ensure you specify the correct 'source' path for the module.
# Module Inputs
The module accepts the following input variables:

- `name` : The name of the application or resource.
- `environment` : The environment in which the resource exists.
- `label_order` : The order in which labels should be applied.
- `attributes` : Additional attributes to add to the labels.
- `extra_tags` : Extra tags to associate with the resource.
# Module Outputs
This module does not produce any outputs. It is primarily used for labeling resources within your Terraform configuration.

# Examples
For detailed examples on how to use this module, please refer to the [Examples](https://github.com/cypik/terraform-gcp-labels/tree/master/_example) directory within this repository.

# License
This Terraform module is provided under the **'[License Name]'** License. Please see the [LICENSE](https://github.com/cypik/terraform-gcp-labels/blob/master/LICENSE) file for more details.

# Author
Your Name
Replace **'[License Name]'** and **'[Your Name]'** with the appropriate license and your information. Feel free to expand this README with additional details or usage instructions as needed for your specific use case.
