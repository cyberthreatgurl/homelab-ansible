# Step-CA Credentials Configuration

> [!IMPORTANT]
> **Manual Credential Required**: The inline encrypted `ca_password` has been removed from repository tracking to adhere to the zero-secret policy.
>
> To supply the real CA password when running this playbook:
>
> ### Option 1: Environment Variable (Recommended for CLI / CI)
> ```bash
> export STEP_CA_PASSWORD="your-strong-ca-password"
> ansible-playbook playbooks/step-ca-playbook.yml
> ```
>
> ### Option 2: Command Line Extra Var
> ```bash
> ansible-playbook playbooks/step-ca-playbook.yml -e ca_password="your-strong-ca-password"
> ```
>
> ### Option 3: Local Untracked Vault
> Define `vault_ca_password: "your-strong-ca-password"` inside a local untracked `vault.yml` file.
