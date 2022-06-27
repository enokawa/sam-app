# sam-cicd-sample

CI/CD sample of AWS SAM using GitHub Actions and OpenID Connect.

## Tests

```bash
# install dependencies
pip install -r tests/requirements.txt --user

# unit test
python -m pytest tests/unit -v

# integration test
AWS_SAM_STACK_NAME=<stack-name> python -m pytest tests/integration -v
```

## Deploy

```bash
sam build
sam deploy --s3-bucket <your-s3-bucket-name>
```

## Cleanup

```bash
aws cloudformation delete-stack --stack-name sam-app
```
