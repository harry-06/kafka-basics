# kafka-basics
================

Installation Guides (For MacOS)
--------------------------------
1.Install package manager HomeBrew from https://brew.sh/ or alternatively run below command from Terminal window
  /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
  
2. Download and setupo JDK 8
brew tap caskroom/versions
brew cask install java8

3.Download & Extract the Kafka binaries from https://kafka.apache.org/downloads or alternatively run below brew command
  brew install kafka
  
4.Check installation by using kafka commands( for-example:kafka-topic)

5.Edit Zookeeper & Kafka configs using a text editor

	a)zookeeper.properties: dataDir=/your/path/to/data/zookeeper

	b)server.properties: log.dirs=/your/path/to/data/kafka

6.Start Zookeeper in one terminal window: zookeeper-server-start config/zookeeper.properties

7.Start Kafka in another terminal window: kafka-server-start config/server.properties
  
  
Install Kafka in Linux
======================

1.Download and Setup Java 8 JDK:

2.Download & Extract the Kafka binaries from https://kafka.apache.org/downloads

3.Try Kafka commands using bin/kafka-topics.sh (for example)

4.Edit PATH to include Kafka (in ~/.bashrc for example) PATH="$PATH:/your/path/to/your/kafka/bin"

5.Edit Zookeeper & Kafka configs using a text editor

	zookeeper.properties: dataDir=/your/path/to/data/zookeeper

	server.properties: log.dirs=/your/path/to/data/kafka

6.Start Zookeeper in one terminal window: zookeeper-server-start.sh config/zookeeper.properties

7.Start Kafka in another terminal window: kafka-server-start.sh config/server.properties



Install Kafka in Windows
========================
1.Download and Setup Java 8 JDK
2.Download the Kafka binaries from https://kafka.apache.org/downloads
3.Extract Kafka at the root of C:\
4.Setup Kafka bins in the Environment variables section by editing Path
5.Try Kafka commands using kafka-topics.bat (for example)
6.Edit Zookeeper & Kafka configs using NotePad++ https://notepad-plus-plus.org/download/

	a)zookeeper.properties: dataDir=C:/kafka_2.12-2.0.0/data/zookeeper (yes the slashes are inversed)

	b)server.properties: log.dirs=C:/kafka_2.12-2.0.0/data/kafka (yes the slashes are inversed)

7.Start Zookeeper in one command line: bin/zookeeper-server-start.sh config/zookeeper.properties

8.Start Kafka in another command line: bin/kafka-server-start.bat config/server.properties
  
Important commands
==================
1) kafka-topics --zookeeper 127.0.0.1:2181 --list -->To list all topics
2)kafka-topics --zookeeper 127.0.0.1:2181 --topic first_topic --describe -->To retrieve topic details like partitions,replication factor etc...
3)kafka-topics --zookeeper 127.0.0.1:2181 --topic second_topic --delete --> Delete topic
4)kafka-console-producer --broker-list 127.0.0.1:9092 --topic first_topic -->Create producer for topic
5)kafka hiranhari$ kafka-console-producer --broker-list 127.0.0.1:9092 --topic first_topic --producer-property acks=all-->add properties to producer
6)kafka-console-producer --broker-list 127.0.0.1:9092 --topic first_topic . -->create consumer for topic






