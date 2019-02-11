# Build a serverless application using AWS SAM

https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-quick-start.html

```
pip install --user aws-sam-cli
sam init --runtime python3.6
cd sam-app
sam build --use-container
cd .aws-sam/build
sam local start-api
curl localhost:3000/hello
```
