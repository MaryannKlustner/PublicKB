{{{
  "title": "Cloud Platform - Release Notes: March 5, 2015",
  "date": "3-5-2015",
  "author": "Jared Ruckle",
  "attachments": [],
  "contentIsHTML": false
}}}

###New Features (1)

* **Service Catalog.** Selected platform services can now be selectively exposed to chosen subaccounts (as well as child subaccounts). This new capability is ideal for the phased rollout of new features to certain subaccounts. The service catalog currently includes: load balancers, premium backup, and public IP addresses for servers.

![Service Catalog](../images/service-catalog-01.png)

###Minor Enhancements (5)

* **New Domains.** Effective March 5, the default CenturyLink Cloud domain will be updated to control.ctl.io.  The URL for SAML users has also been updated to https://[`account-alias`].cloudportal.io (where `account-alias` is your four-letter account identifier). The legacy domains will continue to operate for 90 days.

* **Subdomains featuring Account Alias.** Along with the new domains listed above, custom subdomains based on account alias are now available, in the form of https://[`account-alias`].cloudportal.io. Use the Site Branding capabilities (under the Account tab) to update the logo that appears on the bottom of the page. This furthers the "white label" capabilities of the platform.

* **Support for Custom Price Lists & Displays.** Administrators who want to show a custom price for services in the Control Portal can now do so. Contact CenturyLink Cloud to learn more.

* **Cloud Network Services in DE1.** CenturyLink Cloud deployments in DE1 can now be connected to other environments using Cloud Network Services.  This capability delivers private, secure, and high-speed connectivity between traditional and cloud environments.

* **MS SQL Server 2014.** Deploy MS SQL 2014 Web, Standard & Enterprise Editions on CenturyLink Cloud via Blueprints.  These SQL instances are unmanaged; licensing is handled under CenturyLink's SPLA relationship with Microsoft.

###Online Tools (4)

* **Cloud Cost Estimator now open source.** Understand and model cloud costs in more depth by viewing and modifying the code behind the [CenturyLink Cloud Cost Estimator](http://www.centurylinkcloud.com/estimator). Details are available in this [blog post](http://www.centurylinkcloud.com/blog/post/cloud-services-estimator-now-open-source), and the Github repository can be found [here](http://www.github.com/CenturyLinkCloud/PriceEstimator).

* **Map of CenturyLink data centers and services.** View CenturyLink's portfolio of capabilities by data center using an [interactive map](http://www.centurylinkcloud.com/data-centers) online.  The tool supports multiple layers of filtering, as well as standard online map controls.

![Online Map of Services & Locations](../images/datacenter-capabilities-map-01.png)

* **CenturyLinkCloud.com is now multi-language.** Browse http://www.centurylinkcloud.com in multiple languages, including German, Japanese, English (UK), English (Canada), and Canadian French. To change the language, simply navigate to the bottom right of any page on the site.

![Multi-language Site](../images/multilanguage-website-01.png)
* **New Knowledge Base.** The CenturyLink Cloud [Knowledge Base](http://www.centurylinkcloud.com/knowledge-base) has been re-designed to be even easier to use. These enhancements include improved organization, layout, and search capabilities.

![Online Knowledge Base](../images/knowledge-base-online-01.png)

###Documentation (1)
* [**Expanded API documentation**](http://www.centurylinkcloud.com/api-docs/v2/) - New knowledge base articles for CenturyLink Cloud's V2 API have been added [here](http://www.centurylinkcloud.com/api-docs/v2/). New actions covered include [Set Server Disks](http://www.centurylinkcloud.com/api-docs/v2/#servers-set-server-disks), [Set Server CPU/Memory](http://www.centurylinkcloud.com/api-docs/v2/#servers-set-server-cpumemory), and [Set Server Credentials](http://www.centurylinkcloud.com/api-docs/v2/#servers-set-server-credentials), among others.

###Ecosystem - New Blueprints (5)

* [**FoundationDB**](../Ecosystem Partners/getting-started-with-foundationdb-blueprint.md) – Next generation database engine that combines the advantages of modern NoSQL databases with the power and reliability of ACID transactions.

* [**Dynatrace**](../Ecosystem Partners/getting-started-with-dynatrace-blueprints.md) – Application Performance Monitoring (APM) software for today's most challenging web, cloud, mobile, enterprise and Big Data applications worldwide.


* [**Datastax**](../Ecosystem Partners/getting-started-with-datastax-blueprint.md) - Enterprise–grade Cassandra solution, enabling customer big data analytics workloads.


* [**Acumatica**](../Ecosystem Partners/getting-started-with-acumatica-erp-blueprint.md) - Cloud–based accounting and ERP software for the small to midsize business looking to streamline management processes and unlock business potential.

* [**Centerity**](../Ecosystem Partners/getting-started-with-centerity-blueprints.md) – Enhanced monitoring solution providing server metrics and a complete business intelligence layer across  server assets in the CenturyLink Cloud.

###Open Source Contributions
Panamax enhancements from CenturyLink Labs - Selected highlights include:

* [**Golang-builder**](http://www.centurylinklabs.com/small-docker-images-for-go-apps/) - creates a slim image from any Go project, dramatically reducing its file size compared to other methods.

* [**Marathon Adapter 0.1.0  and PMX-Agent-Installer 0.1.3**](http://www.centurylinklabs.com/deploy-to-a-mesosphere-cluster-with-the-panamax-marathon-adapter/) – enable deployments of Apache Mesos and Mesosphere DCOS clusters with Panamax.

* [**Panamax API/UI v0.2.12**](http://www.centurylinklabs.com/automated-deployment-endpoint-creation-with-panamax/) – Panamax now supports automated cluster deployments on CenturyLink Cloud and AWS via Kubernetes and Dray. Each cluster includes the appropriate orchestrator, as well as the Panamax Agent/Adapter.

Full release notes from CenturyLink Labs are available [here](https://github.com/CenturyLinkLabs/panamax-ui/wiki/Release-Notes)
