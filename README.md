# Amazon DynamoDB IAM Example Policy as Templates

A selection of example Amazon DynamoDB and DAX IAM policies with more restrictive security that you should be using instead of the official AWS Managed policies for DynamoDB. These policy examples are templatized for the moment. Therefore you must full in the template.

in the region you want, or wildcard (*) for all regions, an AccountId or w
* *${AWS::Region}* - Replace with the region you want this policy to be effective in or a wildcard (*) for it to apply to all regions.
* *${AWS::AccountId}* - Replace with your AWS account ID or you can put a wildcard (*) for all accounts.
* *${DDB::TableName}* - Replace with the Amazon DynamoDB table name you wish the policy to apply to or wildcard (*) for the policy to apply to all tables.

Note: Stacking the wildcard values in the resources can give access to a user across entire accounts, geographic regions, etc. Please be careful. You can always take these policies and customize to your own needs.

* ***AmazonDynamoDBDataFullAccess.json*** - A templated policy that only allows read access to DynamoDB tables, indexes, and streams as well as write access to base tables.
* ***AmazonDynamoDBDAXDataOperations*** - A template policy to allow read/write access to Amazon DynamoDB Accelerator (DAX).
* ***AmazonDynamoDB+DAXReadWriteAccess.json*** - A template policy for allowing read/write access to both Amazon DynamoDB and Amazon DynamoDB Accelerator (DAX).
* ***AmazonDynamoDBControlPlaneFullAccess.json*** - A template to assign admin access to an ops focused person/team so they can manage DynamoDB and DAX, but not read or change data.
