## Today

- Worked on my MES project

### Cognito

- Working towards getting Cognito set up, via SAM, to provide JWT authentication in my project. I've set up JWT-issuing servers before for other projects, and a managed service like Cognito seems like a great option.

- Ran into trouble as the default out-of-the-box configuration for Cognito is to protect all routes and their methods. For programmatic access, this doesn't present a problem - I can generate signups and log in via the appropriate routes. Running through the browser (my application is based on Next.js), however, encounters CORS issues.

- Specifically, the requests are `blocked by CORS policy: Response to preflight request doesn't pass access control check: It does not have HTTP ok status.`

- A GitHub comment by Sébastien Stormacq (on a related Cognito/API Gateway issue) has pointed to the problem likely being that, under the default configuration, Cognito is rejecting the `OPTIONS` method call as unauthorized - so tools like Postman/Insomnia and direct program requests can succeed, but browser-based requests fail.

- Still working on re-tooling my SAM template to properly get Cognito and API Gateway to allow `OPTIONS` calls.

- Once I get this working, I can apply the solution to both the MES project and my Cloud Calendar, so I'm eager to knock it out.

## Next Steps

- Working further on the MES project

## Resources

- GitHub: [Amplify REACT fails to call REST API protected by Cognito User Pool (unauthorized OPTIONS call)](https://github.com/aws-amplify/amplify-js/issues/3456#issuecomment-502028330)

## Social Proof

### Twitter

[Day 21/100](https://twitter.com/quinceleaf/status/1312216029150363648)

### LinkedIn

[Day 21/100](https://www.linkedin.com/feed/update/urn:li:activity:6717979839367909376/)
