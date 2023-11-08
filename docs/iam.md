# IAM

Identify and Access Management

## Overview
Manages access of AWS users and resources

## Identities
- Users: End users who log into the console or interact with AWS programmatically
- Groups: Group up Users so they all share the same permissions
- Roles: Associate permissions to a role and then assign this to Users or Groups

### Policies: 
- JSON documents which grant permissions for users, groups or roles to acces servicies. Attached to [IAM Identities](#identities)
	- Inline policies: policies attach directly to an user
	- Managed policies: Managed by AWS. Labeled with an orange box. No editable
	- Customer Managed policies: Created by customer which is editable

[Policy JSON document structure](./images/iam/iam.png)

#### Password policy
- Set minimun requirements to a password, password rotation...

## Access keys
- Allow users to interact with AWS service programmatically via AWS CLI or AWS SDK
- Maximum 2 Access keys per user

## MFA
- Managed by users themselves, administrator cannot directly enforce users to have MFA
- Administrator account could create a policy requiring MFA to access certain resources

[IAM CheatSheet](./images/iam/iam_2.png)
