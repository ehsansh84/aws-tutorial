### Hello world using Python, FastAPI and Lambda
To create a "Hello, World!" application for Python FastAPI using AWS Lambda, you can follow these general steps:

- Create a virtual environment for your project and install the necessary dependencies, including fastapi and uvicorn.
- Write your FastAPI code. Here's a basic example:
```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
async def read_root():
    return {"Hello": "World"}

```
- Save the code in a file named `app.py`.
- Install the `awscli` package and configure it with your AWS credentials.
- Create a deployment package by running the following command:
```bash
pip install awscli --upgrade --user
cd <path_to_your_project_directory>
zip -r9 <name_of_your_deployment_package>.zip .
```
- Go to the AWS Lambda console and create a new Lambda function. Choose the Python 3.7 (or higher) runtime, and select the "Upload a .zip file" option.
- Upload your deployment package by clicking on the "Upload" button, and select the `.zip` file you created in step 5.
- In the "Handler" field, enter `app.handler`. This refers to the name of your file (`app.py`) and the name of the function that should be invoked (handler).
- Save the function and test it by clicking on the "Test" button. You should see a response like `{"Hello": "World"}`.

That's it! You've created a "Hello, World!" application using FastAPI and AWS Lambda.