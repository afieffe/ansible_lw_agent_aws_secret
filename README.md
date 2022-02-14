# playbook ansible lacework agent
Install Lacework Agent using a token stored in AWS Secret Manager under lacework/token

Add permission to acess the secret manager:

        {
            "Effect": "Allow",
            "Action": [
                "secretsmanager:GetResourcePolicy",
                "secretsmanager:GetSecretValue",
                "secretsmanager:DescribeSecret",
                "secretsmanager:ListSecretVersionIds"
            ],
            "Resource": [
                <Secret arn>
            ]
        },
        {
            "Effect": "Allow",
            "Action": "secretsmanager:ListSecrets",
            "Resource": "*"
        }
        
  Update lacework-config.json.j2 with http proxy.
