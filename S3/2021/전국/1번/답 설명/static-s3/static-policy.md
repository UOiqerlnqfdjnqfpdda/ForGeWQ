# 2021 제 1번 문제 CloudFront 제작시 사용되는 s3 권한

```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "Statement1",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": [
                "arn:aws:s3:::wsi-1234-iost-web-static",
                "arn:aws:s3:::wsi-1234-iost-web-static/*"
            ]
        }
    ]
}
```