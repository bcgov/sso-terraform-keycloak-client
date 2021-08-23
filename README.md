# SSO Terraform Keycloak Client

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

## Authors

Module is maintained by [SSO Team](https://github.com/orgs/bcgov/teams/sso-ops).

## License

Apache 2 Licensed. See [license](./LICENSE) for full details.
