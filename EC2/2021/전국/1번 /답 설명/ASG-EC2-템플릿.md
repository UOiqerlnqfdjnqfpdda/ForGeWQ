# 2021년도 제 1번 문제 
# private subnet에 위치하는 ASG를 만들때 템플릿의 user script


```
#!/bin/bash

sudo yum install -y jq
sudo yum install -y curl

sudo yum install -y python3
sudo yum install -y python3-pip
sudo pip3 install Flask

aws s3 cp s3://wsi-1234-iost-artifactory/app.py ./

sudo mkdir -p /var/log/app
sudo chmod 777 /var/log/app
sudo touch /var/log/app/app.log
sudo chmod 777 /var/log/app/app.log
sudo yum install -y amazon-cloudwatch-agent

echo '{
    "logs": {
        "logs_collected": {
            "files": {
                "collect_list": [
                    {
                        "file_path": "/var/log/app/app.log",
                        "log_group_name": "/aws/ec2/wsi",
                        "log_stream_name": "api_{instance_id}",
                        "timezone": "UTC"
                    }
                ]
            }
        }
    }
}' | sudo tee /opt/aws/amazon-cloudwatch-agent/etc/amazon-cloudwatch-agent.json > /dev/null

nohup python3 app.py &

sudo systemctl start amazon-cloudwatch-agent
sudo systemctl enable amazon-cloudwatch-agent
```

