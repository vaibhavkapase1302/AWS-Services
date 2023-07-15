# AWS Lambda:
### Hand Written Notes:
<a href="https://github.com/vaibhavkapase1302/AWS-Services/blob/main/AWS-Lambda/Lambda%20by%20Vaibhav.pdf"> AWS lambda Hand Written Notes

### Event structure for S3
```js

import json def lambda_handler(event, context):
    # TODO implement
    bucketname = event['Records'][0]['s3']['bucket']['name']
    objectname = event['Records'][0]['s3']['object']['key']
    eventtime = event['Records'][0]['eventTime']
    print("The event is happened at: ",eventtime)
    print("The bucket name is: ",bucketname)
    print("Object name is: ",objectname)
    return {
        'statusCode': 200,
        'body': json.dumps('Hello from my first lambda function')
    }

```
