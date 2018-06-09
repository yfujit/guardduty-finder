# guardduty-finder

guardduty_finder will deploy the notification logic completely and automatically on a serverless to make AWS account more secure.

### Automatically deployed components to AWS
* [Amazon GuardDuty](https://aws.amazon.com/guardduty/)
* [Amazon CloudWatch](https://aws.amazon.com/cloudwatch/)
* [AWS Lambda](https://aws.amazon.com/lambda/)


## Installation Guide
First, please clone this repository to your development environment.
```
$ git clone https://github.com/yfujit/guardduty-finder.git
```

### [Slack](https://slack.com/)

Slack is one of the most popular chat tools. guardduty_finder notify team members to use Slack Incoming Webhook.

#### Incoming Webhook
Incoming Webhooks are a simple way to post messages from external sources into Slack. Please show Official page.

#### Configure webhookurl.yml
Create config/webhookurl.yml and configure WEBHOOK_URL.
```
$ cp config/webhookurl.yml.sample config/webhookurl.yml

$ vi config/webhookurl.yml
WEBHOOK_URL: SET_YOUR_SLACK_INCOMING_WEBHOOK_URL #Please Change
```


### [Serverless](https://serverless.com/)
Serverless is toolkit for deploying and operating serverless architectures.

1. Install Serverless Globally
    ```
    $ npm install -g serverless
    ```
2. Check Serverless command
    ```
    $ serverless info
    ```

## How to use
Conguraturation! With just this command your AWS account will be more secure.
```
$ sls deploy --stage {dev,stg,qa,prod} --region {AWS Regions}
```
Default Parameters

* stage : dev
* region : us-east-1

#### example
```
$ sls deploy --stage prod --region ap-northeast-1
```


## Reference
Thank you for Code.
https://gist.github.com/manabusakai/009fe1d77a34f31a0ea9eeab40e78330
