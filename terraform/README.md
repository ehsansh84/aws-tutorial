- terraform init - Initializes a new or existing Terraform working directory, including downloading any required provider plugins.
- terraform plan - Generates an execution plan that shows what actions Terraform will take when you apply your configuration. Review the plan carefully to make sure it matches your intended changes.
- terraform apply - Applies the changes to create the AWS Lambda function and any other resources defined in your Terraform configuration.
- terraform destroy - You will be prompted to confirm the destruction of resources. Type "yes" to confirm.

To run a Terraform configuration `main.tf``, follow these steps:
- Save the Terraform code to a file named main.tf.
- Open a terminal and navigate to the directory containing main.tf.
- Run terraform init to initialize the Terraform working directory.
- Run terraform plan to generate an execution plan.
- Review the execution plan carefully to make sure it matches your intended changes.
- Run terraform apply to apply the changes and create the Lambda function.
- Wait for Terraform to complete the creation of the Lambda function.
- To test the Lambda function, you can either invoke it manually through the AWS Management Console or use the AWS CLI to invoke it. The AWS CLI command to invoke the Lambda function would look something like this:
```commandline
aws lambda invoke --function-name example_lambda --payload '{}' output.json
```
