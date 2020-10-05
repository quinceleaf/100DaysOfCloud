## Today

- Worked on authentication for my CloudCalendar and MES projects

- Successfully set up AWS Cognito as pool for my frontend user/group authentication and management & as a Lambda-based authorizer for my API Gateway.

- I'm not using AWS Amplify, which is being pushed as the all-inclusive way to get started with Cognito and other services, but rather using Cognito directly as a user pool/directory against which JWTs can be issued to the frontend, and as a Lambda-based authorizer for the API.

- As such, I set up my own frontend interface (login, etc) rather than use the hosted-UI components Amplify offers.

- Next I'll work on weaving authentication through rest of frontend routes, pages, and queries, and into the Lambdas that read and write to the DynamoDB tables for each project.

- Learned a lot of good lessons on implementing frontend (React) and API authentication from a paid [egghead](egghead.io) workshop I took back in May from Ryan Chenkie (of [reactsecurity.io](reactsecurity.io), and formerly at [Auth0](https://auth0.com)). Glad to put the lessons to use!

## Next Steps

- Working further on the MES project

## Resources

- None today

## Social Proof

### Twitter

[Day 22/100](https://twitter.com/quinceleaf/status/1312910910395232257)

### LinkedIn

[Day 22/100](https://www.linkedin.com/posts/brian-ibbotson_react-security-activity-6718680753472970752-44Q6)
