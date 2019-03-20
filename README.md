# Kafka LDAP Security Hook
Kafka LDAP Security

Introduction:
To enable security in Kafka we can use SASL. SASL is a pluggable implementation where different mechanisms like PLAIN, SCRAM, GSSAPI, OAUTHBEARER or custom implementations can be used.

SASL allows Kafka to authenticate producers & consumers. ACLs allows these clients to perform different operations like read, write, describe etc on topics.

Kafka LDAP Security Hook is an extension of SASL PLAIN mechanism which enables following:
1. Allow Kafka to authenticate clients against LDAP
2. Perform group level ACLs authorizations

# Installation
1. To enable this hook we have to download the kafka-ldap-hook.jar file in Kafka library folder.
2. Provision LDAP properties like URL, Bind DN user and password, base DN for users and groups

# Testing
Install InsightLake LDAP example docker from Docker Hub.
This docker image contains following users: producer_client1, producer_client2 and consumer_client1 etc.
It also includes groups like AppConsumers, AppProducers etc.

Install Kafka manually or using Docker image. Pass the LDAP configuration file in KAFKA_OPTS.

Create a topic test

Create ACLs for producer_client1, group: AppProducers using KafkaAcls command like:

Use Kafka Console producer and consumer to test the permissions.

License
------
InsightLake Data Explorer is a commercial product but distributed to be used freely. Please contact contact@insightlake.com for details.

Getting Help
----------

You can get help easily :
Community - Google Groups
Slack Channel
Twitter
Facebook
Email: contact@insightlake.com

