
![[rk_sqs_alerter.drawio.png]]

I created a Terraform remote module that has a variety of alert types configured. e.g.

1. Lambda - error rate %
2. Duration
3. Memory
4. API Gateway 4xx/5xx
5. ECS Cluster (Memory & CPU)

Various Terraform consumers can feed in the names of resources they created into the remote module so that alerts would be (re)provisioned for that resource every time it was (re)deployed.

I also created an alert client (listens to SQS) that could send alerts to any arbitrary MS Teams channel with a graph depicting the error that triggered the alert via the `GetMetricWidgetImage` API.

