# AWS Lambda S3 and Image Rekognition Function Project

This starter project consists of:
* Function.cs - class file containing a class with a single function handler method
* aws-lambda-tools-defaults.json - default argument settings for use with Visual Studio and command line deployment tools for AWS

You may also have a test project depending on the options selected.

The generated function handler responds to S3 events on an Amazon S3 bucket and if the object is a png or jpg file uses 
Amazon Rekognition to detect labels. Once the labels are found it adds them as tags to the S3 Object.

## Here are some steps to follow from Visual Studio:

To deploy your function to AWS Lambda, right click the project in Solution Explorer and select *Publish to AWS Lambda*.

To view your deployed function open its Function View window by double-clicking the function name shown beneath the AWS Lambda node in the AWS Explorer tree.

To perform testing against your deployed function use the Test Invoke tab in the opened Function View window.

To configure event sources for your deployed function, for example to have your function invoked when an object is created in an Amazon S3 bucket, use the Event Sources tab in the opened Function View window.

To update the runtime configuration of your deployed function use the Configuration tab in the opened Function View window.

To view execution logs of invocations of your function use the Logs tab in the opened Function View window.

## Here are some steps to follow to get started from the command line:

Once you have edited your function you can use the following command lines to build, test and deploy your function to AWS Lambda from the command line (these examples assume the project name is *PetsLamda*):

Restore dependencies
```
    cd "PetsLamda"
    dotnet restore
```

Execute unit tests
```
    cd "PetsLamda/test/PetsLamda.Tests"
    dotnet test
```

Deploy function to AWS Lambda
```
    cd "PetsLamda/src/PetsLamda"
    dotnet lambda deploy-function
```
