```sh
eksctl create iamserviceaccount \
--name fluentd \
--namespace amazon-cloudwatch \
--cluster aqt-dev-cluster \
--attach-policy-arn arn:aws:iam::aws:policy/CloudWatchAgentServerPolicy \
--profile aqt-dev-sts \
--approve
eksctl create fargateprofile --namespace amazon-cloudwatch --cluster aqt-dev-cluster --region ap-southeast-1 --profile aqt-dev-sts
```
