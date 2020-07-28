# Serverless Chaos Monkey

A lambda function that randomly chooses a running EC2 server and terminates it.

## Getting started

1. Generate the package
   
```bash
npm install
npm run package
```

2. upload the package `chaos-monkey.zip` to AWS Lambda.
3. Add and edit `EC2_AWS_REGION` as an env. variable for your function
4. Apply permissions found in `iam-policy.json` (edit it with the correct aws region)
5. Add EventBridge (CloudWatch Events) as a trigger, sending events to the function every 5 minutes.
6. Check the logs `/aws/lambda/chaos-monkey` and the state of your EC2 instances.

## Chaos engineering

[Some reading about this discipline](https://en.wikipedia.org/wiki/Chaos_engineering)
