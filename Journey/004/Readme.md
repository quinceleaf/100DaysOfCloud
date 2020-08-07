## Introduction

Spent today:

- re-wrote my Python CRUD and query functions, written locally and tested against my local [DynamoDB Docker image](https://hub.docker.com/r/amazon/dynamodb-local), into AWS Lambda functions calling on my production DynamoDB table
- setting up API Gateway to trigger these lambdas as a result of HTTP requests
- set up all of the routes as individual lambda functions, and then wondered if there was a best practice to do so or to combine them into larger, monolithic functions – Yan Cui's
  [blog post on HackerNoon](https://hackernoon.com/aws-lambda-should-you-have-few-monolithic-functions-or-many-single-purposed-functions-8c3872d4338f) was helpful in sketching out the considerations to weigh in choosing which approach to take.
- As he points out, by properly naming the functions and diligently tagging them, you shouldn't have any issues _organizing_ or _finding_ functions.

## Obstacles

Been trying to resolve a problem with the APIs:

- The methods test fine, both at the lambda level and testing the API within the AWS console.

- Despite the methods being listed as `Authorization: None` and `API Key: Not required`, trying to call them from outside the console – via `curl`, Postman, Insomnia or the browser – results in the following:

```
{
  "message": "Missing Authentication Token"
}
```

- Found numerous posts on the AWS Support Forums and elsewhere from people with same symptoms, with many suggestions for resolving the problem (such as, the problem can occur if you call a route by a method that you haven't yet defined), but so far have not had any luck resolving the issue.

## Next Steps

Tomorrow I _plan_ to:

- resolve the authorization problem and finish setting up API Gateway
- continue studying for the SAA-CO2 exam

## Resources

- [AWS / Best practices for working with AWS Lambda functions](https://docs.aws.amazon.com/lambda/latest/dg/best-practices.html)
- [Yan Cui / AWS Lambda - should you have few monolithic functions or many single-purposed functions?](https://hackernoon.com/aws-lambda-should-you-have-few-monolithic-functions-or-many-single-purposed-functions-8c3872d4338f)

## Social Proof

### Twitter

[Day 04/100](https://twitter.com/quinceleaf/status/1291579008631676928)

### LinkedIn

[Day 04/100](https://www.linkedin.com/feed/update/urn:li:activity:6697346223818571776/)
