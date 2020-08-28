# Amazon DynamoDB IAM Policies

A selection of example Amazon DynamoDB and DAX IAM policies with more restrictive security that you should be using instead of the official AWS Managed policies for DynamoDB.

* ***AmazonDynamoDBDataFullAccess.json*** - A templated policy that only allows read access to DynamoDB tables, indexes, and streams as well as write access to base tables.
* ***AmazonDynamoDBDAXDataOperations*** - A template policy to allow read/write access to Amazon DynamoDB Accelerator (DAX).
* ***AmazonDynamoDB+DAXReadWriteAccess.json*** - A template policy for allowing read/write access to both Amazon DynamoDB and Amazon DynamoDB Accelerator (DAX).
