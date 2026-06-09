AWS Threat detection lab
A cloud security monotiring lab created in AWS to detect unauthorized login attemps, IAM privalage escalation, and root account compromise with email alerts.

Overview
This project simulates a security operations monitoring setup using native AWS services. CloudTrail captures all account activity, CloudWatch evaluates logs against threat detection rules, and SNS delivers immediate alerts when suspicious behavior is detected. Attack scenarios were simulated to validate detection across critical and high severity findings.

I inplemented the following:

CloudTrail to record every API call, login attempt, and configuration changes made in the AWS account, This is essential because without CloudTrail there would be no detection alerts possible.

CloudWatch's purpose is to read those logs and if they matches a detection rule such as the threashold of 3 failed logins it would trigger an alarm

GuardDuty works alongside this setup to provide machine based threat dection learning, it would flag findings such as EC2 compromise and S3 data exposure attempts that normal rule based alarms would miss.

AWS config enforces compliance rules across the enviroments to ensure resources stay within defined security baselines

I simulated attack scenarios such as:
-Failed console logins attempts that trigger brute force detection
-IAM policy modification to simulate privilege escalation attempts
-EC2 compromise simulation validated against GuardDuty findings
-S3 data exposure attempt validated against GuardDuty findings

Under the screenshots tab you can find the screenshots of verified proof of simulations and brute force attack attempts.

My next lab will consists of recieving real world brute force attacks in order to triange an alert.
