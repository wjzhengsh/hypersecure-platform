---

copyright:
  years: 2018
lastupdated: "2018-03-16"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# How it works

{{site.data.keyword.cloud}} {{site.data.keyword.hsplatform}} simplifies and automates your process to configure a highly-secure evironment for iOS application development. It creates the Mobile Backend as a Service (MBaaS) and Backend for Frontend (BFF) for your application, and instantiates a set of Hyper Protect services.
{:shortdesc}

The **Backend for IBM Hyper Protect Services starter** ((referenced as **backend** below)) kit is a server-side starter kit that hosts additional services for your application with a Backend For Frontend (BFF) architecture pattern. Step 9-ii in [Developing with Backend for IBM Hyper Protect Services](index.html#backend) is to run the `.build/debug/BackendforIBMHyperProtectServicesyyyyy` script where **yyyyy** is your project name suffix.

This script ensures hyper protection by performing data lifecycle management by using {{site.data.keyword.cloud_notm}} Key Protect that is enhanced by {{site.data.keyword.cloud_notm}} {{site.data.keyword.hscrypto}}. A Centralized Root Key (CRK) that is backed by a FIPS 140-2 Level 4 compliant HSM is linked to {{site.data.keyword.cloud_notm}} Hyper Protect DBaaS cluster. This CRK is used for encrypting the data and in the event of key deletion, access to the data is revoked and the data, securely erased. The keys are never in the clear and only the CRK ID is used. <!--For complete protection of business logic and data in use, deploy your containers that consume Key Protect APIs in [{{site.data.keyword.cloud_notm}} {{site.data.keyword.hscontainers}}](https://console.bluemix.net/docs/containers/container_index.html){:new_window}.-->

The `.build/debug/BackendforIBMHyperProtectServicesyyyyy` script automates the following tasks to your project with {{site.data.keyword.cloud_notm}} Hyper Protect Services. You can also execute the each and every command in your terminal window.
1. Navigate to the root directory of the backend starter kit project.
    `cd BackendforIBMHyperProtectServicesyyyyy`
2. Log into {{site.data.keyword.cloud_notm}} with the `bx login --sso` command. For more options of the `bx` command, such as changing endpoints, see [{{site.data.keyword.cloud_notm}} (bx) commands](https://console.bluemix.net/docs/cli/reference/bluemix_cli/bx_cli.html#bluemix_cli){:new_window}.
3. Create {{site.data.keyword.cloud_notm}} platform API key with the `bx iam api-key-create ServiceLinker -f ServiceLinker.apikey` command.
4. Install software dependencies with the `npm install` or `npm install --python=python2.7 on OSX High Sierra` command.
5. Navigate to the `Sources/Application` folder and run the service linking Node.js script with the `node link-services.js <apikey from ServiceLinker.apikey> -v` command. The `<apikey from ServiceLinker.apikey>` is the API key that you create in step 3. Ensure that you select the correct {{site.data.keyword.cloud_notm}} account, DBaaS instance, and other prompts that appear while running the script.
    Note that this service linking will be automated as part of Starter Kit creation when the Hyper Protect services move from Experimental to Production.

<!--
 The `xxx` script automates the following tasks to set up a hyper secure development environment that is garanteed by a set of Hyper Protect services.
1. Collects your {{site.data.keyword.cloud_notm}} credentials including user name and password. The iOS starter kit uses this credentails to instantiate Hyper Protect services in your {{site.data.keyword.cloud_notm}} accout.
2. Downloads the {{site.data.keyword.cloud_notm}} {{site.data.keyword.hscrypto}} credentials and Advanced Cryptography Service Provider (ACSP) client libraries. The The iOS starter kit configures credentials in the ACSP client at your backend. You application can then use the ACSP client libraries to access the z Hardware Security Module (zHSM) that is the cryptographic hardware with the highest security certificate level of FIPS 140-2 Level 4.
3. Creates an {{site.data.keyword.cloud_notm}} {{site.data.keyword.keymanagementserviceshort}} service instance that is associated to {{site.data.keyword.hscrypto}}. {{site.data.keyword.hscrypto}} stores the keys that {{site.data.keyword.keymanagementserviceshort}} generates on LinuxONE.
4. Creates a key in Key Protect for Hyper Protect DBaaS. This key serves as the root key to initiate the database. 
5. Creates a {{site.data.keyword.cloud_notm}} Hyper Protect DBaaS instance.  Hyper Protect DBaaS stores and protects your data in a MongoDB database cluster with hyper secure and isolation.
6. Associates the Hyper Protect DBaaS instance to the key in Key Protect. After the database is ready, the root key that {{site.data.keyword.keymanagementserviceshort}} generates can be dropped to prevent access to the database from privileged users.
-->

*Figure 1* shows the architecture of the backend service that the iOS starter kit provides you and the relationship among the Hyper Protect services.  For more information about how the backend and these Hyper Protect services work together for an iOS application, see [Sample iOS application](sample.html). 

![How it works](image/how.png "How it works")  
*Figure 1. How it works*
  
You can then start your application development in this development environment. After you develop your application, you can debug and test it on your local file system or deploy it to a service container cluster in {{site.data.keyword.cloud_notm}}. In {{site.data.keyword.cloud_notm}}, your backend and each of these Hyper Protect services run in a service container that ensures safty and privacy. 
