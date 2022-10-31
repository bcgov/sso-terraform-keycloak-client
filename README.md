# SSO Terraform Keycloak Client

![Lifecycle:Stable](https://img.shields.io/badge/Lifecycle-Stable-97ca00)

Terraform module which creates a Keycloak realm client with default values.

- see https://registry.terraform.io/providers/mrparkers/keycloak/latest/docs/resources/openid_client

## Usage

```hcl
module "client_test-client" {
  source              = "github.com/bcgov/sso-terraform-keycloak-client?ref=dev"
  realm_id            = "onestopauth"
  client_name         = "test-client"
  valid_redirect_uris = [
    "http://localhost:3000"
  ]
}
```

- remove `?ref=dev` when referring `main` branch.

## Bugs

- `pkce_code_challenge_method` value is not confirmed with the Keycloak server; it only relies on the value of the TF state.

## Authors

Module is maintained by [SSO Team](https://github.com/orgs/bcgov/teams/sso-ops).

## License

Apache 2 Licensed. See [license](./LICENSE) for full details.
