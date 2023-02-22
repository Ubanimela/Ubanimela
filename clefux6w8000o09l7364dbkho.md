# How to handle Json-based events on S3 using Amazon Lambda

When used with [Amazon S3](https://aws.amazon.com/s3/), AWS [Lambda](https://en.wikipedia.org/wiki/AWS_Lambda) is a potent tool for creating serverless apps that can handle JSON-based events. It can be useful for several scenarios, such as updating a different database or index depending on changes to S3 items.

You must first build a new Lambda function before setting up the Lambda function to handle S3 events. The Amazon Management Console or the AWS CLI may be used for this.

Next, you must set up your Lambda function to handle S3 events after establishing it.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677080002865/d8894283-10ca-4a0e-af52-de52b86918fa.png align="center")

To do this, you may establish a new S3 bucket and configure event alerts for the bucket using the Amazon Management Console or the AWS CLI. Your Lambda function may be set to be called anytime a new S3 object is created or updated using these event alerts.

Your Lambda function will be given a JSON-based event object as input when called by an S3 event. This event object will provide details about the S3 item, such as the object key, bucket name, and other metadata that caused the event.

You can use the JSON libraries with [Python](https://www.python.org/) or Node.js to parse this JSON-based event object and get the information you need for your Lambda function.

For example, you would want to extract the S3 object key if you wanted to get the contents of an object from S3.

In addition to processing the JSON-based event object, you could run more lambda functions based on what was in the S3 object.

For instance, you could update a different database or index depending on the object's contents, do some data transformation on the object's contents, or perform some analysis.

To do this, you may communicate with other Amazon services using Python or Node.js AWS SDKs.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1677080829145/2c4d0cc3-93f6-4bc1-9377-fe00cf963def.png align="center")

For example, you could use the Amazon SDK for Elasticsearch or the AWS SDK for DynamoDB to index the object's contents so that you can search them.

Based on the contents of the S3 object, you could then update a table.

When building your lambda function to process S3 events, there are a few important best practices to remember.

***First***, to make it simple to grow and try again if required, it's crucial to design your function as stateless and idempotent from the start.\*

***Second***, handling failures and reporting errors or exceptions is important when processing data.

You may use this to identify and address problems with your function.

***Finally***, it's critical to properly test your function before using it.

By simulating S3 events with the AWS Management Console or the AWS Command Line Interface (CLI), you can test your function to make sure it works as expected.

Using Amazon Lambda to handle JSON-based events on S3 is a good way to make serverless apps that respond to changes in S3 objects.

You can also make apps that fully use the Amazon cloud and are reliable and scalable by using the AWS SDKs and following best practices for making Lambda functions.

### [Conclusion](https://mela.hashnode.dev/)

***For developers to create scalable, event-driven apps that react to changes in their S3 buckets in real-time, JSON-based events on S3 with Amazon Lambda is a powerful method.***

***Developers can handle JSON-formatted event data and automate many workflows and business processes using Lambda functions, custom code, and S3 event triggers.***

***Thank you for reading, if you like what you read, please follow me and sign up for my email.***