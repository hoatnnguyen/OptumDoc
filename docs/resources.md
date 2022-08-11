# Resources
## Useful Airflow Commands

* `airflow cheat-sheet [-h] [-v]` - Display cheat sheet.
* `airflow config [-h] COMMAND` - View configuration.
* `airflow db check [-h]` - Check if the database can be reached.
* `airflow db init [-h]` - Initialize the metadata database.  
Visit [Airflow Commands](https://airflow.apache.org/docs/apache-airflow/stable/cli-and-env-variables-ref.html) for more airflow commands.

## Useful Vault Commands (CLI)
* `vault namespace list` - List all namespaces.
* `vault token create` - Create a new token.
* `vault token renew` - Renew a token lease.
* `vault secrets enable database` - Enable a secrets engine.
* `vault secrets list` - List all secrets engines.
* `vault kv put [secret path] value=[secret value]` - Store a secret.