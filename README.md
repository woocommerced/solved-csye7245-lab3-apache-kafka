Download Link: https://assignmentchef.com/product/solved-csye7245-lab3-apache-kafka
<br>
This lab demonstrates leveraging and implementing Kafka services for static data alongwith  real-timeTwitter streaming.

Apache Kafka is a streaming message platform. It is a publish-subscribe based durable messaging system. Kafka is designed to be high performance, highly available, and redundant. It is used to collect, process, store, and integrate data at scale. A messaging system sends messages between processes, applications, and servers.

It’s basic use cases includes:

<ul>

 <li>Stream Processing</li>

 <li>Messaging</li>

 <li>Website Activity Tracking</li>

 <li>Log aggregation</li>

 <li>Event Sourcing</li>

 <li>Application health monitoring</li>

</ul>




These are four main parts in a Kafka system:

<h1>●     <strong>Broker</strong>: Handles all requests from clients (producer, consumer and metadata) and keeps data replicated within the cluster. There can be one or more brokers in a cluster</h1>

<h1>●     <strong>Zookeeper</strong>: Keeps track of status of the Kafka clusters (brokers, topics, users)</h1>

<h1>●     <strong>Producer</strong>: Sends records to a broker</h1>

<h1>●     <strong>Consumer</strong>: Consumes batches of records from the broker</h1>

<h1>Experiment setup</h1>




<strong><u>Prerequisites:</u></strong>




<ol>

 <li>Installing Oracle Virtual VM Box</li>

</ol>




<strong>Specifications: </strong>

<ul>

 <li>4 GB RAM</li>

 <li>25 GB Hard Drive</li>

 <li>Downloading ubuntu iso file</li>

</ul>




<strong>Oracle VM Virtual Box Manager</strong>




<ol>

 <li><strong>Installing Ubuntu Guest Edition</strong></li>

</ol>




sudo apt install build-essential dkms linux-headers-$(uname -r)




<ul>

 <li>Able to copy/paste the contents easily</li>

 <li>Full screen mode available</li>

 <li>Certain in-built headers/packages available for additional functionalities</li>

</ul>







<ol start="2">

 <li><strong>Installing Python</strong></li>

</ol>

<strong> </strong>

Installing the latest version of Python




sudo apt install python3




sudo apt install python3-pip




python3 –version










<ol start="3">

 <li><strong>Installing AWS CLI</strong></li>

</ol>

<strong> </strong>

AWS CLI helps to access multiple AWS services and functionalities from the command line.




sudo apt install curl




curl “https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip” -o “awscliv2.zip”




unzip awscliv2.zip




sudo ./aws/install




/usr/local/bin/aws –version










<ol start="4">

 <li><strong>Connecting with AWS</strong></li>

</ol>

<strong> </strong>

Connecting the server with AWS account by entering the Access and Secret keys




aws configure




aws s3 ls

<strong> </strong>




<strong> </strong>

<strong> </strong>

<ol start="5">

 <li><strong>Installing Java jdk</strong></li>

</ol>

<strong> </strong>

Java jdk is required for starting the Kafka broker and services

<strong> </strong>

sudo apt update




sudo apt list




sudo apt install default-jre




sudo apt install default-jdk




javac –version




<strong> </strong>

<ol start="6">

 <li><strong>Installing Pycharm in Ubuntu</strong></li>

</ol>

<strong> </strong>

<h1>Test Results</h1>

<strong> </strong>

<ol>

 <li><strong>Installing Kafka</strong></li>

</ol>

<strong> </strong>

Download Apache Kafka from <a href="https://kafka.apache.org/downloads">here </a>

<strong> </strong>

Unzip Kafka binaries by using  tar -xzvf




pip3 install kafka-python




<strong> </strong>

<ol start="2">

 <li><strong>Starting the Zookeeper service and Kafka broker</strong></li>

</ol>

<strong> </strong>

Navigate to the directory where the downloaded files are unzipped and start the Zookeeper service

bin/zookeeper-server-start.sh config/zookeeper.properties

Start the Kafka broker in a new terminal

bin/kafka-server-start.sh config/server.properties

<strong> </strong>

<h1>Use Cases</h1>




<strong>Collecting real time sampled tweets from </strong><a href="https://github.com/holladileep/CSYE7245-Spring2021-Labs/blob/main/kafka/twitter.com"><strong>Twitter</strong></a><strong> and publishing them to our Kafka Broker</strong>

<strong> </strong>

<strong> </strong>

<ol>

 <li><strong>py</strong></li>

</ol>

<strong> </strong>

Running the script <strong>producer.py</strong> for generating events

<strong> </strong>

<strong> </strong>

<ol start="2">

 <li><strong>py</strong></li>

</ol>

<strong> </strong>

<strong>    </strong>Running the script <strong>consumer.py</strong> to consume the events published by the producer.

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<ol start="3">

 <li><strong>twitter-stream.py</strong></li>

</ol>

<strong> </strong>

Using the twitter-stream.py script to  fetch tweets from Twitter’s API in real-time.

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

<strong> </strong>

Entering our bearer token in the twitter.py script under the <strong>BEARER_TOKEN </strong>parameter.

<strong> </strong>

Tweets are published to the Kafka Broker.

<strong> </strong>




On running <strong>consumer.py </strong>again, we can see all the published events that are collected by the consumer.

<strong> </strong>

<strong> </strong>

<strong> </strong>

<h1>Lessons learned</h1>




<ol>

 <li>Learnt configuration of Oracle Virtual Box with Ubuntu operating system</li>

 <li>Learnt the basic fundamentals of Apache Kafka</li>

 <li>Implemented real-time data streaming using Twitter API in Apache Kafka</li>

</ol>




<h1> References</h1>




<a href="https://docs.cloudera.com/documentation/enterprise/6/6.1/PDF/cloudera-kafka.pdf">https://docs.cloudera.com/documentation/enterprise/6/6.1/PDF/cloudera-kafka.pdf</a>




<a href="https://www.cloudkarafka.com/blog/2016-11-30-part1-kafka-for-beginners-what-is-apache-kafka.html">https://www.cloudkarafka.com/blog/2016-11-30-part1-kafka-for-beginners-what-is-apache-kafka.html</a>