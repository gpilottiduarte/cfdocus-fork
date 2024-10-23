## Metadata_Start 
## code: en
## title: Connect an AWS account 
## slug: cloud-iam-connect-an-aws-account 
## seoTitle: Connect an AWS account 
## description:  
## contentType: Markdown 
## Metadata_End
This document explains the steps to integrating Amazon Web Services (AWS) with  to provision, manage, and monitor access to the Cloud Service Provider (CSP).

 also supports Google Cloud Services (GCP) and Microsoft Azure. If you want to integrate other CSPs, check the documentation  or .

## Requirements

- An  account.  
- A  or account with IAM permissions.

## Create a custom policy in the AWS Console

1. In the AWS Console, navigate to the  page.  
2. Go to the  page.  
3. Click .  
4. In the Policy , click the  option.  
5. Copy the JSON content below and paste it into the policy editor.

`
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "opsworks:DescribeStacks",
                "iam:DeleteAccessKey",
                "opsworks:DescribePermissions",
                "iam:CreateUser",
                "iam:CreateAccessKey",
                "iam:CreateLoginProfile",
                "opsworks:UpdateUserProfile",
                "iam:RemoveUserFromGroup",
                "iam:AddUserToGroup",
                "iam:ListAttachedUserPolicies",
                "iam:DetachUserPolicy",
                "opsworks:CreateUserProfile",
                "iam:DeleteLoginProfile",
                "iam:ListAccessKeys",
                "iam:GetPolicyVersion",
                "iam:ListPolicies",
                "iam:GetPolicy",
                "iam:AttachUserPolicy",
                "iam:DeleteUserPolicy",
                "opsworks:DescribeUserProfiles",
                "iam:UpdateAccessKey",
                "iam:ListRoles",
                "iam:DeleteUser",
                "iam:ListUserPolicies",
                "opsworks:DeleteUserProfile",
                "iam:ListGroupsForUser",
                "opsworks:DescribeInstances",
                "iam:ListUsers",
                "iam:ListGroups",
                "iam:GetUser",
                "iam:GetLoginProfile",
                "iam:GetAccountAuthorizationDetails"
            ],
            "Resource": "*"
        }
    ]
}
`

6. Click .  
7. Give your policy an easily identifiable name.  
8. Configure optional settings if needed.  
9. Click .

For more details, check the AWS documentation on .

## Create a user with the custom policy in the AWS Console

1. In the AWS Console, navigate to the  page.  
2. Go to the  page.  
3. Click .  
4. Attribute a username and click .  
5. Select the option .  
6. Select the policy you created in the previous steps from the list  
7. Click .

For more details, check the AWS documentation on .

## Create an access key for the user in the AWS Console

1. In the AWS Console, navigate to the  page.  
2. Go to the  page.  
3. Click the user you created in the previous steps.  
4. Navigate to the  tab.  
5. In the  section, click .  
6. Select the  option.  
7. Add a tag if needed.  
8. Click .  
9. Copy the access key value and the secret access key and paste them into a text editor. You can also click the  button to download the credentials. You’ll need these values when you integrate your account with senhasegura.

For more details, check the AWS documentation on .

## Integrate AWS with Cloud IAM

1. In the top left corner of the senhasegura platform, click on the , represented by the nine squares, and select .
2. In the side menu, select .
3. Click the  icon, represented by the three vertical dots, and select the option .
4. In the pop-up window, give a  for the account.
5. Click .
6. Click the  tab.
7. Paste the user access key in the  field.
8. Paste the secret key in the  field.
9. Select the .
10. Click the  button.

Once you’re done, the senhasegura  page will refresh with your newly integrated AWS account.

---
Do you still have questions? Reach out to the .