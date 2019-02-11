# Build a serverless application using AWS SAM

https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-quick-start.html

Install the AWS SAM CLI
```
pip install --user aws-sam-cli
```

Initialize
```
sam init --runtime python3.6
cd sam-app
sam build --use-container
cd .aws-sam/build
```

Test Locally
```
sam local start-api
curl localhost:3000/hello
```

Package
```
aws s3 mb s3://bucketname

sam package \
    --output-template-file packaged.yaml \
    --s3-bucket bucketname
```

Deploy
```
sam deploy \
    --template-file packaged.yaml \
    --stack-name sam-app \
    --capabilities CAPABILITY_IAM \
    --region us-east-1
```
