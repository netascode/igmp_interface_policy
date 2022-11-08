<!-- BEGIN_TF_DOCS -->
[![Tests](https://github.com/netascode/terraform-aci-scaffolding/actions/workflows/test.yml/badge.svg)](https://github.com/netascode/terraform-aci-scaffolding/actions/workflows/test.yml)

# Terraform ACI Scaffolding Module

Description

Location in GUI:
`Tenants` » `XXX`

## Examples

```hcl
module "aci_scaffolding" {
  source  = "netascode/scaffolding/aci"
  version = ">= 0.0.1"

  name        = "ABC"
  alias       = "ABC-ALIAS"
  description = "My Description"
}
```

## Requirements

| Name | Version |
|------|---------|
| <a name="requirement_terraform"></a> [terraform](#requirement\_terraform) | >= 1.3.0 |
| <a name="requirement_aci"></a> [aci](#requirement\_aci) | >= 2.0.0 |

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aci"></a> [aci](#provider\_aci) | >= 2.0.0 |

## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_name"></a> [name](#input\_name) | IGMP Interface Policy name. | `string` | n/a | yes |
| <a name="input_tenant"></a> [tenant](#input\_tenant) | IGMP Interface Policy's Tenant name. | `string` | n/a | yes |
| <a name="input_description"></a> [description](#input\_description) | Tenant description. | `string` | `""` | no |
| <a name="input_grp_timeout"></a> [grp\_timeout](#input\_grp\_timeout) | IGMP Interface Policy Group Name. Allowed values between 3-65535. | `number` | `260` | no |
| <a name="input_allow_v3_asm"></a> [allow\_v3\_asm](#input\_allow\_v3\_asm) | IGMP Interface Policy flag for Any-source multicast (ASM) v3. | `bool` | `false` | no |
| <a name="input_fast_leave"></a> [fast\_leave](#input\_fast\_leave) | IGMP Interface Policy flag for Fast Leave. | `bool` | `false` | no |
| <a name="input_report_link_local_groups"></a> [report\_link\_local\_groups](#input\_report\_link\_local\_groups) | IGMP Interface Policy flag for Link Local groups report. | `bool` | `false` | no |
| <a name="input_last_member_count"></a> [last\_member\_count](#input\_last\_member\_count) | IGMP Interface Policy last member query count. Allowed values between 1-5. | `number` | `2` | no |
| <a name="input_last_member_response_time"></a> [last\_member\_response\_time](#input\_last\_member\_response\_time) | IGMP Interface Policy last member response time. Allowed values between 1-25. | `number` | `1` | no |
| <a name="input_querier_timeout"></a> [querier\_timeout](#input\_querier\_timeout) | IGMP Interface Policy querier timeout. Allowed values between 1-255. | `number` | `255` | no |
| <a name="input_query_interval"></a> [query\_interval](#input\_query\_interval) | IGMP Interface Policy querier interval. Allowed values between 1-18000. | `number` | `125` | no |
| <a name="input_robustness_variable"></a> [robustness\_variable](#input\_robustness\_variable) | IGMP Interface Policy robustness factor. Allowed values between 1-7. | `number` | `2` | no |
| <a name="input_query_response_interval"></a> [query\_response\_interval](#input\_query\_response\_interval) | IGMP Interface Policy query response interval. Allowed values between 1-25. | `number` | `25` | no |
| <a name="input_startup_query_count"></a> [startup\_query\_count](#input\_startup\_query\_count) | IGMP Interface Policy startup query count. Allowed values between 1-10. | `number` | `2` | no |
| <a name="input_startup_query_interval"></a> [startup\_query\_interval](#input\_startup\_query\_interval) | IGMP Interface Policy startup query interval. Allowed values between 1-10. | `number` | `31` | no |
| <a name="input_version_"></a> [version\_](#input\_version\_) | IGMP Interface Policy startup query count. Allowed values `v2` or `v3`. | `string` | `"v2"` | no |
| <a name="input_report_policy_multicast_route_map"></a> [report\_policy\_multicast\_route\_map](#input\_report\_policy\_multicast\_route\_map) | IGMP Interface Policy report multicast route-map. | `string` | `""` | no |
| <a name="input_static_report_multicast_route_map"></a> [static\_report\_multicast\_route\_map](#input\_static\_report\_multicast\_route\_map) | IGMP Interface Policy static report multicast route-map. | `string` | `""` | no |
| <a name="input_max_mcast_entries"></a> [max\_mcast\_entries](#input\_max\_mcast\_entries) | IGMP Interface Policy maximum number of multicast entries. Allowed values 1-4294967295 or `unlimited`. | `string` | `"unlimited"` | no |
| <a name="input_reserved_mcast_entries"></a> [reserved\_mcast\_entries](#input\_reserved\_mcast\_entries) | IGMP Interface Policy number of reserved multicast entries. Allowed values 0-4294967295 or `undefined`. | `string` | `"undefined"` | no |
| <a name="input_state_limit_multicast_route_map"></a> [state\_limit\_multicast\_route\_map](#input\_state\_limit\_multicast\_route\_map) | IGMP Interface Policy state limit multicast route-map. | `string` | `""` | no |

## Outputs

| Name | Description |
|------|-------------|
| <a name="output_dn"></a> [dn](#output\_dn) | Distinguished name of `igmpIfPol` object. |
| <a name="output_name"></a> [name](#output\_name) | IGMP Interface Policy name. |

## Resources

| Name | Type |
|------|------|
| [aci_rest_managed.igmpIfPol](https://registry.terraform.io/providers/CiscoDevNet/aci/latest/docs/resources/rest_managed) | resource |
| [aci_rest_managed.igmpRepPol](https://registry.terraform.io/providers/CiscoDevNet/aci/latest/docs/resources/rest_managed) | resource |
| [aci_rest_managed.igmpStRepPol](https://registry.terraform.io/providers/CiscoDevNet/aci/latest/docs/resources/rest_managed) | resource |
| [aci_rest_managed.igmpStateLPol](https://registry.terraform.io/providers/CiscoDevNet/aci/latest/docs/resources/rest_managed) | resource |
| [aci_rest_managed.rtdmcRsFilterToRtMapPol_report_policy](https://registry.terraform.io/providers/CiscoDevNet/aci/latest/docs/resources/rest_managed) | resource |
| [aci_rest_managed.rtdmcRsFilterToRtMapPol_state_limit](https://registry.terraform.io/providers/CiscoDevNet/aci/latest/docs/resources/rest_managed) | resource |
| [aci_rest_managed.rtdmcRsFilterToRtMapPol_static_report](https://registry.terraform.io/providers/CiscoDevNet/aci/latest/docs/resources/rest_managed) | resource |
<!-- END_TF_DOCS -->