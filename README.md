# Amazon DynamoDB IAM Example Policy as Templates

A selection of example Amazon DynamoDB and DAX IAM policies with more restrictive security that you should be using instead of the official AWS Managed policies for DynamoDB. These policy examples are templatized for the moment. Therefore you must full in the template. The three template values you will need to replace are:

* *${AWS::Region}* - Replace with the region you want this policy to be effective in or a wildcard (*) for it to apply to all regions.
* *${AWS::AccountId}* - Replace with your AWS account ID or you can put a wildcard (*) for all accounts.
* *${DDB::TableName}* - Replace with the Amazon DynamoDB table name you wish the policy to apply to or wildcard (*) for the policy to apply to all tables.

Note: Stacking the wildcard values in the resources can give access to a user across entire accounts, geographic regions, etc. Please be careful. You can always take these policies and customize to your own needs.

* ***[AmazonDynamoDBDataFullAccess.json](./AmazonDynamoDBDataFullAccess.json)*** - A templated policy that only allows read access to DynamoDB tables, indexes, and streams as well as write access to base tables.
* ***[AmazonDynamoDBDAXDataOperations.json](./AmazonDynamoDBDAXDataOperations.json)*** - A template policy to allow read/write access to Amazon DynamoDB Accelerator (DAX).
* ***[AmazonDynamoDB+DAXReadWriteAccess.json](./AmazonDynamoDB+DAXReadWriteAccess.json)*** - A template policy for allowing read/write access to both Amazon DynamoDB and Amazon DynamoDB Accelerator (DAX).
* ***[AmazonDynamoDBInfrastructureFullAccess.json](./AmazonDynamoDBInfrastructureFullAccess.json)*** - A template to assign admin access to admin the DynamoDB and DAX infrastructure so they can manage that, but not read or change data in any table, index, stream, or cache.
