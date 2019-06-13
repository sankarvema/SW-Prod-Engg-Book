# SNS vs. SQS

Following are some of the differences

## Entity Type

SQS : Queue (Similar to JMS)
SNS : Topic (Pub/Sub system)
## Message consumption

SQS : Pull Mechanism - Consumers poll and pull messages from SQS

SNS : Push Mechanism - SNS Pushes messages to consumers
## Use Case

SQS : Decoupling 2 applications and allowing parallel asynchronous processing

SNS : Fanout - Meaning allowing same message to be processed in multiple ways
## Persistence

SQS : Messages are persisted for some (configurable) duration is no consumer available

SNS : No persistence. Whichever consumer is present at the time of message arrival, get the message and the message is deleted. If no consumers available then the message is lost.
## Consumer Type

SQS : All the consumers are supposed to be identical and hence process the messages in exact same way

SNS : All the consumers are (supposed to be) processing the messages in different ways
## Sample applications

SQS : Jobs framework. Where the Jobs are submitted to SQS and the consumers at the other end can process the jobs asynchronously. And if the job frequency increases then the number of consumers can be increased for parallel processing

SNS : Image processing. If someone uploads an image to S3 then watermark that image, create a thumbnail and also send a ThankYou email. In that case S3 can send notification to SNS Topic and 3 consumers can be attached to SNS topic. 1st one watermarks the image, 2nd one creates a thumbnail and the 3rd one send a ThankYou email. All of them receiving the same message (image URL) and doing their corresponding processing in parallel.
