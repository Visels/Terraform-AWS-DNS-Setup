# terraform-aws-cloudfront

Terraform Module that creates an AWS Route 53 resources.




## Documentation

- [AWS Route 53](https://aws.amazon.com/route53/)

## Usage example



See `examples` directory for working examples to reference:

```hcl
module "dns" {
  source  = "terraform-module/dns/aws"
  version = "~> 2"
  # insert the 3 required variables here
}
```

<!-- BEGINNING OF PRE-COMMIT-TERRAFORM DOCS HOOK -->
## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | ~> 1 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | n/a |

## Modules

No modules.

## Resources

| Name | Type |
|------|------|
| [aws_route53_record.this](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/route53_record) | resource |
| [aws_route53_zone.this](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/route53_zone) | resource |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_parent_dns_zone_id"></a> [parent\_dns\_zone\_id](#input\_parent\_dns\_zone\_id) | The ID of the hosted zone to contain this record. | `string` | n/a | yes |
| <a name="input_parent_dns_zone_name"></a> [parent\_dns\_zone\_name](#input\_parent\_dns\_zone\_name) | The name of the hosted zone | `string` | n/a | yes |
| <a name="input_subdomain"></a> [subdomain](#input\_subdomain) | Subdomain zone | `string` | n/a | yes |
| <a name="input_tags"></a> [tags](#input\_tags) | A mapping of tags to assign to the zone. | `map(string)` | `{}` | no |
| <a name="input_ttl"></a> [ttl](#input\_ttl) | The TTL of the recod | `string` | `"30"` | no |
| <a name="input_type"></a> [type](#input\_type) | The record  type. Valid values are A, AAAA, CAA, CNAME, MX, NAPTR, NS, PTR, SOA, SPF, SRV and TXT. | `string` | `"NS"` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_zone_id"></a> [zone\_id](#output\_zone\_id) | Zone ID for a dns distribution |
| <a name="output_zone_name"></a> [zone\_name](#output\_zone\_name) | The name of the zone record. |
<!-- END OF PRE-COMMIT-TERRAFORM DOCS HOOK -->


