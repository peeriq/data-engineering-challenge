# PeerIQ Data Challenge

## Background
PeerIQ is growing and we are seeking exceptional candidates to build out our data operations team! We have created this test as an alternative to traditional coding challenges. We believe that artificial problems with no connection to our subject matter given under artificial conditions (no internet access, unrealistic time constraints) aren't useful in evaluating candidates. Instead, we've created this test to let you show off your problem solving skills!

The test is designed to give us a lot of the information we need to know about you!

## Challenge Summary

1. Write a program that reads CSV files from a S3 bucket and stores data into a postgres database.  (We currently use Spark but you can use any framework you like).
 Path of S3 bucket should be accepted as an environment variable.
Data in CSV contains loans information like loan amount, funded amount, loan grade, term etc.
We need to filter out data in CSV before storing it:

    a. Amount should be rounded up to two digits after decimal.
    
    b. If `loan_status` is `Charged Off` filter out those records.
    
    c. If `purpose` is `other` filter out those records.
    
    d. If `credit score` is less than 700 filter out those records.
    
2.
Option A: Configure this program to spin up on an AWS EMR cluster.
You can refer to this article how to run a program on AWS. 
https://aws.amazon.com/emr/getting-started/

Option B: Containerize your application using a platform such as Docker (https://docs.docker.com/).  Extra credit if the containers can be scaled to run multiple applications at once. 


## Writing Clean, Scalable, and Well-tested Code

As a data engineer, it’s important that you write clean, well-documented code that scales for large amounts of data. For this reason, it’s important to ensure that your solution works well for a large number of logged events, rather than just the simple examples above.

It's also important to use software engineering best practices like unit tests, especially since log data is not clean and predictable. For more details about the implementation, please refer to the FAQ below. If further clarification is necessary, email us at <cc@peeriq.com>

Before submitting your solution you should summarize your approach, dependencies and run instructions (if any) in your `README`.  
You may write your solution in any mainstream programming language such as Java, Python,  or Scala. Once completed, submit a link to a Github repo with your source code.

If your solution requires additional libraries, environments, or dependencies, you must specify these in your `README` documentation.

 
