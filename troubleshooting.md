# Troubleshooting
https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_Troubleshooting.html

## Cannot connect to Amazon RDS DB Instance
    1. The local firewall is stopping the communication traffic
    2. The port cannot be used to send or receive communication for inbound and outbound
    3. The security groups for the DB are not properly configured
    4. DB instance is still being created and is not yet available.