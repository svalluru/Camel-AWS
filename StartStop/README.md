# Schedule to Start / Stop Master and Worker EC2 instances

This example demonstrates how you can use Apache Camel with AWS component on Spring Boot.

### Building

The example can be built with

    mvn clean install

### Running the example


**Pre-requisities :** 

1) You will need AWS access key and Secret key
2) EC2 instance IDs of the Master and Worker nodes.
3) AWS Region name.

**Most of the Configuration Properties are self-explanatory :**

    aws.accesskey=xxxxxxx
    aws.secretkey=xxxxxxx
    aws.region=ca-central-1
    aws.master.ec2.instances=i-xxx,i-xxx,i-xxxx
    aws.worker.ec2.instances=i-xxx,i-xxx,i-xxxxx
    
    aws.ec2.startTime=0+10+21+?+*+MON-FRI  (configure the time when you want to start the EC2 instances)

    aws.ec2.stopTime=0+0+17+?+*+MON-FRI (configure the time when you want to stop the EC2 instances)

**Execution :**

    1) Use mvn clean install (or)
    
    2) From CLI, once you generate the jar file using "mvn compile", use the below command to refer to external spring application.properties file.
         
         java -jar camel-ose-springboot-xml-1.0.0-SNAPSHOT.jar  --spring.config.location=/Users/svalluru/tmp/myec2.properties
         




