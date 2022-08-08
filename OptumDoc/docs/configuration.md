# Configuration
---
For full documentation of Apache Airflow visit [airflow.apache.org](https://airflow.apache.org/).

## Token
!!! info

    Prefer to getToken for further details on how to get **token** on Hashicorp Vault Web UI
## Hashicorp Vault Secrets Backend

To enable Hashicorp Vault to retrieve Airflow connection/variable, specify VaultBackend as the backend in [secrets] section of airflow.cfg.  
Here is a sample configuration:  
```
[secrets]  
backend = airflow.providers.hashicorp.secrets.vault.VaultBackend  
backend_kwargs = {"connections_path": "connections", "variables_path": "variables", "mount_point": "airflow", "url": "http://127.0.0.1:8200"}
```   
!!! info

    - Prefer to [Create Secret](createSecrets.md) for further details on the values of **mount_point**, **namespace**, **config_path**  
    - For Vault running with self signed certificates Add “verify”: “absolute path to ca-certificate file”
The default KV version engine is 2.

## Optional lookup

Optionally connections, variables, or config may be looked up exclusive of each other or in any combination. This will prevent requests being sent to Vault for the excluded type.  

If you want to look up some and not others in Vault you may do so by setting the relevant *_path parameter of the ones to be excluded as null.  

For example, if you want to set parameter config_path to "mui", and not look up variables, your configuration file should look like this:

```

[secrets]
backend = airflow.providers.hashicorp.secrets.vault.VaultBackend  
backend_kwargs = {"connections_path": null, "variables_path": null, "mount_point": "airflow", "config_path": "mui", "url": "http://127.0.0.1:8200"}
``` 


