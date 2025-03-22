# Security Policy

## Supported Versions

Use this section to tell people about which versions of your project are
currently being supported with security updates.

| Version | Supported          |
| ------- | ------------------ |
| 5.1.x   | :white_check_mark: |
| 5.0.x   | :x:                |
| 4.0.x   | :white_check_mark: |
| < 4.0   | :x:                |

## Reporting a Vulnerability

Use this section to tell people how to report a vulnerability.

Tell them where to go, how often they can expect to get an update on a
reported vulnerability, what to expect if the vulnerability is accepted or
declined, etc.

{     "Version": "2012-10-17",     "Statement": [         {             "Effect": "Deny",             "Action": [                 "codecommit:GitPush",                 "codecommit:DeleteBranch",                 "codecommit:PutFile",                 "codecommit:MergePullRequestByFastForward"             ],             "Resource": "arn:aws:codecommit:us-east-1:834303415169:Repodemo",                       // Give your repos ARN which you can find in settings             "Condition": {                 "StringEqualsIfExists": {                     "codecommit:References": [                         "refs/heads/master"                        ]                 },                 "Null": {                     "codecommit:References": false                 }             }         }     ] } 
