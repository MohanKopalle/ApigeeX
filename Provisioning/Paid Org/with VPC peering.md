# Apigee X Paid Org Provisioning with VPC Peering

## Scope of this Document 
This document describes how to install and configure Apigee from the command line with VPC peering. 
Commonly Used Terminologies, Quick-Handy-Notes and many more related to the same are available here.

## FAQ for Beginners on Terminology
<details>
  <summary><b>1️⃣ What is VPC Network?</b></summary>
  
  **VPC (Virtual Private Cloud)** is a logically isolated, private network inside a public cloud (like Google Cloud, AWS, Azure) that you fully control.

  > **Think of it as:** *Your own private data-center network, built inside Google’s global infrastructure.*<br>
  
  **VPC:**<br>
  ☑️ Provides connectivity for your Compute Engine virtual machine (VM) instances, including Google Kubernetes Engine (GKE) clusters, serverless workloads, and other Google Cloud products built on Compute Engine VMs.<br>
  ☑️ Offers built-in internal passthrough Network Load Balancers and proxy systems for internal Application Load Balancers.<br>
  ☑️ Connects to on-premises networks by using Cloud VPN tunnels and VLAN attachments for Cloud Interconnect.<br>
  ☑️ Distributes traffic from Google Cloud external load balancers to backends.<br>

  **Inside a VPC you control:**<br>
  ☑️ IP address ranges (CIDR blocks)<br>
  ☑️ Subnets & regions<br>
  ☑️ Firewall rules<br>
  ☑️ Routing<br>
  ☑️ Private connectivity<br>
  ☑️ Access boundaries (who can talk to whom)<br>
</details>

<details>
  <summary><b>2️⃣ Why VPC Network?</b></summary>
  
  ##### VPC exists to solve enterprise-grade problems that public internet networks cannot. The Core drivers are:
  * ##### Security
      - Prevents unintended exposure of systems<br>
      - Enables private communication between internal services

  * ##### Compliance
      - Required for financial services, healthcare, telecom, and government<br>
      - Supports auditability and regulatory mandates

  * ##### Control & Predictability
      - Eliminates dependency on the public internet for internal traffic<br>
      - Ensures consistent performance and latency

  * ##### Risk Management
      - Reduces attack surface<br>
      - Enables segmentation and blast-radius containment
   
  <strong>In simple terms, <em>Cloud providers run millions of customers on shared physical infrastructure, so VPC exists to solve four hard enterprise problems:</em></strong>
  
  * ##### Security isolation
      Your workloads:<br>
        - Cannot see other customers’ traffic<br>
        - Cannot be reached unless you explicitly allow it

  * ##### Network control
      You decide:<br>
        - Which services are public<br>
        - Which are private<br>
        - Which talk internally only
    
  * ##### Compliance & governance
      Required for:<br>
        - Banking<br>
        - Healthcare<br>
        - PCI / SOC / ISO<br>
        - Enterprise contracts
      
  * ##### Predictable connectivity
      Private IPs, private DNS, private routing (no dependency on the public internet)

</details>

<details>
  <summary><b>3️⃣ What is Network Peering?</b></summary>

</details>

<details>
  <summary><b>4️⃣ What is Organization Policy Service?</b></summary>

</details>

<details>
  <summary><b>5️⃣ What is Organization Policy Constraint?</b></summary>

</details>

<details>
  <summary><b>6️⃣ What is Data Residency?</b></summary>
  
  For many industry verticals and enterprises, using a cloud offering results in increased scrutiny from security and compliance teams (what data is stored in the cloud, where it is stored, who has access to it, who can see the data, etc.). In addition to this, many countries have passed data privacy laws that prohibit Personally Identifiable Information (PII) data from being stored outside the country or region.

  Data residency for Apigee meets compliance and regulatory requirements by allowing you to specify the geographic locations (regions) where Apigee data is stored. Historically, Apigee allowed you to select the instance region and analytics region; however, Apigee also has global infrastructure, such as an API proxy bundle or other customer data. With data residency, selecting the control plane location ensures that all customer content is stored within the specified region.
  
- **Data residency can be used with the following:**
  - Apigee organizations (Subscription or Pay-as-you-go)
  - Apigee hybrid. See Data residency and Apigee hybrid.
  - Operations Anomalies for non-hybrid Subscription organizations
  - Monetization enabled in Subscription organizations for non-hybrid organizations
  - API analytics
  - Advanced API Security
  - Apigee API hub.
  - Data collector. Data collectors are supported for Subscription and Pay-as-you-go organizations and hybrid versions 1.14.0 and later.

- **Data residency is not currently supported for use with:**
  - Preview- or Beta-release features, such as the preview releases for Looker Studio Integration and Shadow API Discovery
  - Eval organizations
  - Integrated portals
  - Apigee Adapter for Envoy
  - Google Cloud CLI. To provision or manage a data residency-enabled organization, you can use Apigee in the Google Cloud console or the Apigee APIs.

If data residency is enabled for your Apigee installation, **note the following key points**:

  - Data residency must be enabled at the time Apigee is provisioned. You cannot enable data residency for an already-provisioned org.
  - By default, the control plane is a global entity unless you select data residency (regionalization) at the time of Apigee organization creation; it can not be changed later. Once you select data residency and the control plane location, it is cannot be changed. If you later need a different location, you will need to create a new Google Cloud project.
  - When provisioning an org:
    - Without data residency: Specify the region with ANALYTICS_REGION.
    - With data residency: Specify the region with CONTROL_PLANE_LOCATION and the sub-region with CONSUMER_DATA_REGION. <br>See Data residency regions.<br>
      **NOTE:** You select the specific Apigee control plane hosting jurisdiction where your data is stored when you provision your Apigee instance. Note that a jurisdiction refers to a location within a geopolitical boundary that may span more than one region.
  - The admin who provisions Apigee must:
    - Inform Apigee users, such as API developers and other admins, about the data residency configuration
    - Set the location org policy as described in Restricting Resource Locations
  - API developers, admins, or other users of Apigee management APIs must use the new data residency API service endpoint.
</details>
 
<details>
  <summary><b>7️⃣ What is CMEK?</b></summary>

</details>

<details>
  <summary><b>8️⃣ What is CMEK?</b></summary>

</details>

<details>
  <summary><b>9️⃣ What is CMEK?</b></summary>

</details>

<details>
  <summary><b>🔟 What is CMEK?</b></summary>

</details>



