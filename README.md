# AWS-security-monotoring
Tracking and detecting for unauthorized/failed login attempts

I created an AWS tracking and detection system that sent notifications when a login attempt was attempted

I used a few aws services in order to achieve this.

Cloutrail, I created a trail in cloudtrail specifically to track any security violation such as failed login attempts and security risks

Cloudwatch, I created 3 alarms that would send notification to root user.
    1. Failed login attempts 
    2.IAM policy changes
    3.Root account usage

Cloudtrail simply keeps track of the login attempts while cloudwatch will send a notification to user that something is wrong, IAM policy changes is meant to track is someone is attempting to escalate their privelages when they might not be allowed to, And Root account changes are for when anything changes in the root account this could mean the root account was compromised requiring immediate action.

