# DynamoDB Deep Dive

## Introduction

_(Slipped in tracking my progress... been learning/studying for my upcoming Solutions Architect-Associate exam everyday, and beginning to build/code an AWS-hosted website to combine together a number of services. But I failed to document/show social proof, so I'll take the hit in progressed days.)_

Spent today:

- learning more about DynamoDB, watching episodes of AWS's [Build with DynamoDB](https://www.youtube.com/playlist?list=PLoYZGW8AgG1bpxkoVaSDNTff-Zyii-dzH) and [DynamoDB | Office Hours with Rick Houlihan](https://www.twitch.tv/search?term=office%20hours%20with%20rick%20houlihan)
- getting my single-table design/GSIs right using AWS's life-saving [NoSQL Workbench for Amazon DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/workbench.settingup.html)
- giving the new v1.0 release of [Dynobase]() a spin, which _should_ let me browse & query my local [DynamoDB Docker image](https://hub.docker.com/r/amazon/dynamodb-local) in an even easier way than the AWS Console lets me browse & query the cloud version (haven't quite got it working locally yet)
- coding basic setup (create/delete table, load data) and basic CRUD and query functionality using [Boto3](https://boto3.amazonaws.com/v1/documentation/api/latest/reference/services/dynamodb.html) so that I can next wire up the API Gateway-Lambda portions of the project.

## Next Steps

Tomorrow I hope to:

- set up API Gateway and the necessary Lambdas so that my React frontend can query and post to my DynamoDB table

## Social Proof

### Twitter

[Day 03/100](https://twitter.com/quinceleaf/status/1291229769514848262)

### LinkedIn

[Day 03/100](https://www.linkedin.com/posts/brian-ibbotson_100daysofcloud-activity-6696999635904532480-4T0H)
