# 2021 제 1번 문제 웹서버 제작시 사용되는 s3 권한

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::339712924586:role/wsi-supper-user"
            },
            "Action": [
                "s3:GetObject",
                "s3:ListBucket"
            ],
            "Resource": [
                "arn:aws:s3:::wsi-1234-iost-artifactory",
                "arn:aws:s3:::wsi-1234-iost-artifactory/*"
            ]
        },
        {
            "Effect": "Deny",
            "Principal": {
                "AWS": "arn:aws:iam::339712924586:role/wsi-supper-user"
            },
            "Action": "s3:PutObject",
            "Resource": [
                "arn:aws:s3:::wsi-1234-iost-artifactory",
                "arn:aws:s3:::wsi-1234-iost-artifactory/*"
            ]
        }
    ]
}
```