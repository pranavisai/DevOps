## IAM Users
1. An IAM user can access AWS using the management console, CLI, or SDKs.
2. The configuration takes place under AWS IAM (Identity and Access Management).
3. To access any service, users need to be given permissions through policies, either as groups or roles.
4. ``` aws sts get-caller-identity ``` -> to see which identity is currently being used within the CLI.
5. ```aws configure --profile <iam-user> ``` -> to switch to a new user within CLI.
6. To get the Access key and secret access key
   ``` Go to IAM User profile -> Security Credentials -> Create access key -> CLI ```

## IAM Groups
1. Used to simplify user management.
2. Best rules for IAM groups:
   1. Provide descriptive names
   2. Similar roles in the same group
   3. Assign policies so that the users within a specific group will have similar permissions.
