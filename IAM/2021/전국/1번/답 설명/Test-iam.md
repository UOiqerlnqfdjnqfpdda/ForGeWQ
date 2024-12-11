# 테스트용

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "Statement1",
            "Effect": "Deny",
            "Action": [
                "s3:PutObject"
            ],
            "Resource": [
                "*"
            ]
        },
        {
            "Sid": "Statement2",
            "Effect": "Allow",
            "Action": [
                "cloudwatch:*",
                "ec2:*",
                "logs:*",
                "s3:*"
            ],
            "Resource": [
                "*"
            ]
        }
    ]
}
```