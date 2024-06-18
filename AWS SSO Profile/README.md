aws sso login 

aws sso login --profile <profile-name>

1. AWS CLI Installation
2. Configure SSO Login
3. AWS CLI SSO Login

```sh
vi ~/.aws/config
```

```sh
[default]
region = ap-south-1
[profile dev-profile]
sso_start_url = https://facctum.awsapps.com/start#/
sso_region = eu-west-2
sso_account_id = 223530587197
sso_role_name = FacctumDevOpsAccess
region = ap-south-1
output = json
[profile dev-centro]
sso_start_url = https://facctum.awsapps.com/start#/
sso_region = eu-west-2
sso_account_id = 905418413399
sso_role_name = FacctumDevOpsAccess
region = eu-west-2
output = json
[profile qa]
sso_start_url = https://facctum.awsapps.com/start#/
sso_region = eu-west-2
sso_account_id = 891377087030
sso_role_name = FacctumDevOpsAccess
region = ap-south-1
output = json
```
