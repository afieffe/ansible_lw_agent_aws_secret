# terraform_agent_aws_secret
Install Lacework Agent using a token stored in AWS Secret Manager

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
                "arn:aws:secretsmanager:eu-west-1:807828924102:secret:lacework/token-eZgPLc"
            ]
        },
        {
            "Effect": "Allow",
            "Action": "secretsmanager:ListSecrets",
            "Resource": "*"
        }
        
  
