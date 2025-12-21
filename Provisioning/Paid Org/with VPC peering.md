# Apigee X Paid Org Provisioning with VPC Peering

## Scope of this Document 
This document describes how to install and configure Apigee from the command line with VPC peering. 
Commonly Used Terminologies, Quick-Handy-Notes and many more related to the same are available here.

## FAQ for Beginners on Terminology

### 1. What is VPC Network?


### 2. Why VPC Network?


### 3. What is Network Peering?


### 4. What is Organization Policy Service?


### 5. What is Organization Policy Constraint?


### 6. What is Data Residency?
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

### 7. What is CMEK? 
