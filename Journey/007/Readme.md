## Introduction

Spent today:

- continued studying/reviewing **networking** and moved on to **EC2** for my upcoming Solutions Architect – Associate exam, including the various documentation pages, whitepapers and guides.
- Re-wrote several of the lambdas for my project to utilize **transactions**:
  - I've traditionally used SQL databases, and am a big fan of transactions in general.
  - When you use a transaction, you require that a **series** of database actions – typically writes such as creating, updating or deleting – must **all complete successfully**, or else **all of the actions are rolled-back** in tandem.
  - My DynamoDB table involves several (simulated) many-to-many relations, across which data consistency is not managed directly at the database level. Moreover, my single-table database is designed so that there are fields duplicated across several records/record types.
  - This is a perfect use case for transactions, as you would want to ensure that an update to a field in one record be matched by the same update to the duplicate of that field in another record.
  - Originally I did not implement create/update/delete lambdas as transactions, as this would require [provisioning more read-capacity units (RCUs) and write-capacity units (WCUs)](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/ProvisionedThroughput.html), either directly or via auto-scaling, and I was leery of adding to the cost of the project.
    - It's an inconsequential, demonstration side project and I'm currently unemployed. While I am currently using the [AWS Free Tier](https://aws.amazon.com/free/), I'm planning to have this project running long after I've "graduated" from the free tier and so I'd rather be cost-conscious from the beginning.
  - Instead, I had planned to "follow up" with a lambda that would check for and correct orphaned relations on a frequent schedule, say every 1 minute or 5 minutes. This would obviously be less efficient or ideal than using transactions, and this approach quickly became more complicated than I had anticipated.
  - I decided to try to implement transactions to both guarantee data consistency and to slim down the amount of code needed.
  - So far, I'm happy with the result:
    - I've provisioned higher (but still within the limits of the free tier - 2 RCU/4 WCU per table/index), though as this project goes live that might prove too low a capacity.
    - while transactions impose a performance penalty (as [Alex DeBrie demonstrates](https://www.alexdebrie.com/posts/dynamodb-transactions-performance)), at the scale of my project during development I don't find the increased latency a burden.

## Next Steps

Tomorrow I _plan_ to:

- continue studying for the SAA-CO2 exam

## Resources

- [AWS / Managing Complex Workflows with DynamoDB Transactions](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/transactions.html)
- [Alex DeBrie / DynamoDB Transactions: Use Cases and Examples](https://www.alexdebrie.com/posts/dynamodb-transactions/)
- [Alex DeBrie / DynamoDB Transactions Performance Testing](https://www.alexdebrie.com/posts/dynamodb-transactions-performance/)

## Social Proof

### Twitter

[Day 07/100](https://twitter.com/quinceleaf/status/1292880485744508935)

### LinkedIn

[Day 07/100](https://www.linkedin.com/posts/brian-ibbotson_managing-settings-on-dynamodb-provisioned-activity-6698649214198652928-nPVn)
