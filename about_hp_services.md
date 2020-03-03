---

copyright:
  years: 2018, 2019
lastupdated: "2019-08-09"

---

{:external: target="_blank" .external}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}


# About Hyper Protect services

{{site.data.keyword.cloud}} {{site.data.keyword.hsplatform}} integrates a set of Hyper Protect services.


## **{{site.data.keyword.cloud_notm}} {{site.data.keyword.hscrypto}}**  

{{site.data.keyword.hscrypto}} offers cryptography on your keys and data with industry's highest security level. It brings the security and integrity of System z to the cloud. The same state-of-the-art cryptographic technology that banks and financial services rely on is now offered to cloud users via {{site.data.keyword.cloud_notm}}.

{{site.data.keyword.hscrypto}} offers network addressable hardware security modules (HSMs) to provide safe and secure cryptography via PKCS#11 application programming interfaces (APIs). You can access to the highest level attainable of security for cryptographic hardware, that is, FIPS 140-2 Level 4.  Hyper Protect Crypto Services also leverages the IBM Advanced Crypto Service Provider (ACSP) solution that enables remote access to the IBM’s cryptographic coprocessors.

{{site.data.keyword.hscrypto}} is also the key store for the Key Protect service.

For more information about {{site.data.keyword.hscrypto}}, see [Getting started with {{site.data.keyword.cloud_notm}} {{site.data.keyword.hscrypto}}](/docs/services/hs-crypto?topic=hs-crypto-get-started).


## **{{site.data.keyword.cloud_notm}} {{site.data.keyword.keymanagementserviceshort}}**

{{site.data.keyword.keymanagementserviceshort}} helps you provision encrypted keys for apps across IBM Cloud services. As you manage the lifecycle of your keys, you can benefit from knowing that your keys are secured by cloud-based hardware security modules (HSMs) that protect against the theft of information. Together with {{site.data.keyword.hscrypto}}, your keys are secured at the highest security level of FIPS 140-2 Level 4 certificate.

For more information about {{site.data.keyword.keymanagementserviceshort}}, see [Getting started with Key Protect](/docs/services/key-protect).


## **{{site.data.keyword.cloud_notm}} Hyper Protect DBaaS**  

{{site.data.keyword.cloud_notm}} Hyper Protect DBaaS provides databases on demand in {{site.data.keyword.cloud_notm}} to offer a flexible and scalable platform that allows you to quickly and easily provision and manage your database. Hyper Protect DBaaS offers MongoDB database clusters or PostgrepSQL database clusters with two database instance replicas to back up one primary database instance. You can create database clusters in the {{site.data.keyword.cloud_notm}}, manage database instances, administer database users, and create and monitor databases.

Hyper Protect DBaaS secures your data at rest, in use, and in flight in a highly available and secure environment. It prevents IBM or a third party from being able to access your data. Access to the system is restricted and is only enabled through well-defined RESTful APIs. The system hardware, the system configuration, and the database setup ensure high availability.

For more information about Hyper Protect DBaaS, see the following documentation:
- [Getting started with Hyper Protect DBaaS for MongoDB](/docs/services/hyper-protect-dbaas-for-mongodb?topic=hyper-protect-dbaas-for-mongodb-gettingstarted)
- [Getting started with Hyper Protect DBaaS for PostgreSQL](/docs/services/hyper-protect-dbaas-for-postgresql?topic=hyper-protect-dbaas-for-postgresql-gettingstarted)

## **{{site.data.keyword.cloud_notm}} {{site.data.keyword.hpvs}}**  

{{site.data.keyword.cloud_notm}} {{site.data.keyword.hpvs}} provides highly secure virtual servers that can run Linux applications and containerized workloads. It offers a flexible and scalable framework that you can use to quickly and easily provision and manage the created virtual servers.

For more information about {{site.data.keyword.cloud_notm}} {{site.data.keyword.hpvs}}, see [Getting started with {{site.data.keyword.cloud_notm}} {{site.data.keyword.hpvs}}](/docs/services/hp-virtual-servers?topic=hp-virtual-servers-getting-started).

<!--
## **{{site.data.keyword.cloud_notm}} {{site.data.keyword.hscontainers}}**  

{{site.data.keyword.cloud_notm}} Container delivers powerful tools by combining Docker and Kubernetes technologies, an intuitive user experience, and built-in security and isolation to automate the deployment, operation, scaling, and monitoring of containerized apps in a cluster of compute hosts.

**Note**: {{site.data.keyword.hscontainers}} is now available to only sponsor users. If you expect dedicated security support, register as sponsor users with the [IBM Z Client Feedback Program](https://www-01.ibm.com/marketing/iwm/iwmdocs/web/cc/earlyprograms/zcustomer.shtml) to deploy your application to the {{site.data.keyword.hscontainers}} cluster.

For more information about {{site.data.keyword.cloud_notm}} Container, see [Getting started with {{site.data.keyword.cloud_notm}} Container Service](https://console.bluemix.net/docs/containers/container_index.html#container_index).
-->
