{{{
  "title": "Getting Started with XtremeData dbX - Blueprint",
  "date": "3-5-2015",
  "author": "Keith Resar",
  "attachments": [],
  "contentIsHTML": false
}}}



### Overview

After reading this article, the user should feel comfortable getting started using the partner technology on CenturyLink Cloud.

### Partner Profile

<img src="../images/xtremedata/xtremelog_wht.png" style="max-width:200px;border:0;float:right;">

XtremeData – “On-Demand Big Data Analytics with real-time ingest."

http://www.xtremedata.com/

#####Customer Support

|Cloud Alias   	|Sales Contact   	|
|:-	|:-	|
|XDTA   	|centurylinkcloud-sales@xtremedata.com   	|


### Description

XtremeData has integrated their dbX technology with the CenturyLink Cloud platform.  The purpose of this KB article is to help the reader take advantage of this integration to achieve rapid time-to-value for this XtremeData solution.

XtremeData delivers high performance, full-featured ANSI SQL database engine designed for performance at all scales, up to 100s of terabytes. ANSI SQL. Simple to deploy, simple to administer, simple to scale up. Any data schema any data location.


### Audience

CenturyLink Cloud Users


### Deploying a New Cluster

Single button deploy of a new cluster including a master host, a standby master for failover, and two nodes.  For best performance these should be deployed on Hyperscale servers.

#### Steps


1. **Locate the Blueprint in the Blueprint Library**

  Determine whether you will be building a test cluster with small nodes or a production cluster whose nodes that have increased CPU and RAM available.

  ![](../images/xtremedata/blueprint_tiles.png)]

  Starting from the CenturyLink Control Panel, navigate to the Blueprints Library. Search for “dbX Cluster” in the keyword search on the right side of the page.

2. **Click the Deploy Blueprint button.**

3. **Set Required parameters.**

  ![](../images/xtremedata/deploy_parameters.png)

  * **EULA** - Click to accept the software end user license agreement
  * **Cluster ID ** - set unique identifier for all hosts in this Greenplum cluster.  This is used to help other hosts find and join into the cluster
  * **Email Address** - Email address to receive build notification and Greenplum access information
  * **gpadmin Password** - Password used for `gpadmin` user in the web Command Center (ssh login directly via gpadmin is not enabled by default)


4. **Set Optional Parameters**

  Password/Confirm Password (This is the root password for the server. Keep this in a secure place).  It is also used to identify the `gpadmin` user for console and Web Control Center access.

  Set DNS to “Manually Specify” and use “8.8.8.8” (or any other public DNS server of your choice).

  Optionally set the server name prefix.

  The default values are fine for every other option.

5. **Review and Confirm the Blueprint**

6. **Deploy the Blueprint**

  Once verified, click on the `deploy blueprint` button. You will see the deployment details stating the Blueprint is queued for execution.

  This will kick off the Blueprint deploy process and load a page where you can track the deployment progress. Deployment will typically complete within 15 to 20 minutes.

7. **Deployment Complete**

  Once the Blueprint has finished execution you will receive an email confirming the newly deployed assets.  If you do not receive an email like the one shown below your cluster may have had a deployment error - review the *Blueprint Build Log* to look for error messages.

  ![](../images/xtremedata/deploy_cluster_complete_email.png)

8. **Access Web Command Center**

  If you elected to install the optional web command center you may access it via http on port 20800.  Authenticate using the `gpadmin` user and your administrative credentials

  ![](../images/xtremedata/web_command_center.png)

9. **Enable public access** (optional)

  Servers are built using private IPs only with access with client or IPSEC VPN.  For access from the Internet at large add a public IP to your master server.

  <a href="../network/how-to-add-public-ip-to-virtual-machine/">
    <img style="border:0;width:50pxsrc="../images/fw_icon.png">
    Adding a public IP to your virtual machine
  </a>



### Pricing

The costs listed above in the above steps are for the infrastructure only.

After deploying this Blueprint, you may secure entitlements to the technology using the following steps:

 * Email: centurylinkcloud-sales@pivotal.com

### Frequently Asked Questions

**Where do I obtain my license?**

*More to come soon*

**Who should I contact for support?**

* For issues related to cloud infrastructure, please open a ticket using the [CenturyLink Cloud Support Process](../Support/how-do-i-report-a-support-issue.md).
* For issues related to deploying the Pivotal Greenplum Blueprints and application operation on CenturyLink Cloud and you have a paid license, please contact centurylinkcloud-sales@pivotal.io or follow your existing Pivotal support process if known.


**How do I learn more about the application?**

View Pivotal's [Getting Started](http://gpdb.docs.pivotal.io/gpdb-434.html) guide and other documentation from the Pivotal documentation hub.

![](../images/pivotal_greenplum/getting_started_pdf.png)


**How do I login to my cluster for the first time?**

Access your new Pivotal Greenplum cluster via ssh as the root user whose password you supplied at create time.  

Best practices are to create non-administrative user access.  This can be done by creating another user or by configuring the gpadmin user for remote access.  This can be done by executing the following commands:

```
# chsh gpadmin bash
# passwd gpadmin
```
