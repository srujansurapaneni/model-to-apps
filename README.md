# model-to-apps
various design patterns and sample app implementations

Poll based app - SQS
 * service polls s3 for new pictures uploaded
 * runs a facial recognition for newly added pics and logs the results in the database
 
Push based app - SNS
 * vector takes picture
 * send it to s3 
 * poll based app executes lambda to run facial recognition
 * if a match - publishes a topic in SNS
 * SNS send message to user identified
 
