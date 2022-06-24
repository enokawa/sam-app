# sam-app

## Deploy

```bash
sam build
sam deploy　--s3-bucket <your-s3-bucket-name>
```

## Tests

Tests are defined in the `tests` folder in this project. Use PIP to install the test dependencies and run tests.

```bash
# install dependencies
sam-app$ pip install -r tests/requirements.txt --user

# unit test
sam-app$ python -m pytest tests/unit -v
# integration test

sam-app$ AWS_SAM_STACK_NAME=<stack-name> python -m pytest tests/integration -v
```

## Cleanup

```bash
aws cloudformation delete-stack --stack-name sam-app
```