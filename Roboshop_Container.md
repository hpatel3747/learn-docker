### TO deploy Roboshop on Docker Containers
1. unseal the vault
```text
#login to vault server
$sudo -i
#VAULT_ADDR://127.0.0.1:8200 vault operator unseal 0d76651d1698321....type_in_entire_unseal_key
```
2. login to workstation
3. cd tools-setup-code/misc/vault_secrets
4. git pull ; make vault_token="type_in_token"
5. apply terraform infra provision workflow using github runner
6. varify that roboshop is deployed in docker containers

