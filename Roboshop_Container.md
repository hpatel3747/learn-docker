### TO deploy Roboshop on Docker Containers
0. unseal the vault
1. login to workstation
2. cd tools-setup-code/misc/vault_secrets
3. git pull ; make vault_token="type_in_token"
4. apply terraform infra provision workflow using github runner
5. varify that roboshop is deployed in docker containers
#### unseal vault from commandline
```text
#login to vault server
$sudo -i
#VAULT_ADDR://127.0.0.1:8200 vault operator unseal 0d76651d1698321....type_in_entire_unseal_key
