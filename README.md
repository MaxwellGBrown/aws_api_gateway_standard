# aws_api_gateway_standard 

This is an example of an HTTP API Gateway Cloudformation Template.

## Quickstart

1. Deploy the cloudformation template
   ```
   aws cloudformation deploy --template-file template.yml --capabilities CAPABILITY_IAM --stack-name api-gateway-standard
   ```

2. Send a request to the deployed API
   ```
   curl $(aws cloudformation describe-stacks --stack-name api-gateway-standard --query "Stacks[0].Outputs[?OutputKey=='Url'].OutputValue" --output text)
