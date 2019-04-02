# AWS Lambda Concepts<a name="lambda-application-fundamentals"></a>

AWS Lambda lets you run *functions* in a serverless environment to process events in the language of your choice\. Each instance of your function runs in an isolated execution context and processes one event at a time\. When it finishes processing the event, it returns a response and Lambda sends it another event\. Lambda automatically scales up the number of instances of your function to handle high numbers of events\.
+ **Function** – A script or program that runs in AWS Lambda\. Lambda passes invocation events to your function\. The function processes an event and returns a response\. For more information, see [Working with Lambda Functions](lambda-introduction-function.md)\.
+ **Runtimes** – Lambda runtimes allow functions in different languages to run in the same base execution environment\. You configure your function to use a runtime that matches your programming language\. The runtime sits in\-between the Lambda service and your function code, relaying invocation events, context information, and responses between the two\. You can use runtimes provided by Lambda, or build your own\. For more information, see [AWS Lambda Runtimes](lambda-runtimes.md)\.
+ **Layers** – Lambda layers are a distribution mechanism for libraries, custom runtimes, and other function dependencies\. Layers let you manage your in\-development function code independently from the unchanging code and resources that it uses\. You can configure your function to use layers that you create, layers provided by AWS, or layers from other AWS customers\. For more information, see [AWS Lambda Layers](configuration-layers.md)
+ **Event source** – An AWS service, such as Amazon SNS, or a custom service, that triggers your function and executes its logic\. For more information, see [AWS Lambda Event Source Mapping](intro-invocation-modes.md)\.
+ **Downstream resources** – An AWS service, such as DynamoDB tables or Amazon S3 buckets, that your Lambda function calls once it is triggered\. 
+ **Log streams** – While Lambda automatically monitors your function invocations and reports metrics to CloudWatch, you can annotate your function code with custom logging statements that allow you to analyze the execution flow and performance of your Lambda function to ensure it's working properly\.
+ **AWS SAM** – A model to define [serverless applications](https://aws.amazon.com/serverless)\. AWS SAM is natively supported by AWS CloudFormation and defines simplified syntax for expressing serverless resources\. For more information, see [What Is AWS SAM?](https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/) in the *AWS Serverless Application Model Developer Guide*\.