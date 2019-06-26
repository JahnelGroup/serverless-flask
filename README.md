# Serverless Flask

This repository was made by following the article [Flask + Serverless — API in AWS Lambda the easy way](https://medium.com/@Twistacz/flask-serverless-api-in-aws-lambda-the-easy-way-a445a8805028) written by Michal Haták.

## Setup your virtualenv, activate it, install requirements

```bash
$ virtualenv venv -p python3
$ . venv/bin/activate
$ pip install -r requirements.txt
```

## Setup AWS CLI

Install and configure your [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html).

Verify it's working with:

```bash
$ aws sts get-caller-identity
{
    "Account": "<your_account_id>",
    "UserId": "<your_user_id>",
    "Arn": "<your_arn>"
}
```

## Setup AWS IAM Groups / Policies

Create a new group called `Serverless` and add the following policies:

* AWSLambdaFullAccess
* IAMFullAccess
* AmazonAPIGatewayAdministrator

## Setup Serverless

```bash
$ npm install -g serverless
$ npm update -g serverless
```

## Serverless Commands

Test locally with `sls wsgi serve`

Deploy with `sls deploy`

View logs with `sls logs -f app`

Remove it with `sls remove`
