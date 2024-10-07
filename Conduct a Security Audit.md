## Activity Overview

In this activity, I am required to conduct an internal audit for a fictional company named Botium Toys. My task is to review the IT manager’s scope, goals, and risk assessment report. Then, perform an internal audit by completing a controls and compliance checklist.

## Scenario

This scenario is based on a fictional company:

Botium Toys is a small U.S. business that develops and sells toys. The business has a single physical location, which serves as their main office, a storefront, and warehouse for their products. However, Botium Toy’s online presence has grown, attracting customers in the U.S. and abroad. As a result, their information technology (IT) department is under increasing pressure to support their online market worldwide. 

The manager of the IT department has decided that an internal IT audit needs to be conducted. She expresses concerns about not having a solidified plan of action to ensure business continuity and compliance, as the business grows. She believes an internal audit can help better secure the company’s infrastructure and help them identify and mitigate potential risks, threats, or vulnerabilities to critical assets. The manager is also interested in ensuring that they comply with regulations related to internally processing and accepting online payments and conducting business in the European Union (E.U.).   

The IT manager starts by implementing the National Institute of Standards and Technology Cybersecurity Framework (NIST CSF), establishing an audit scope and goals, listing assets currently managed by the IT department, and completing a risk assessment. The goal of the audit is to provide an overview of the risks and/or fines that the company might experience due to the current state of their security posture.

## Scope and goals of the audit

Scope: The scope of this audit is defined as the entire security program at Botium
Toys. This includes their assets like employee equipment and devices, their internal
network, and their systems. You will need to review the assets Botium Toys has and the
controls and compliance practices they have in place.

Goals: Assess existing assets and complete the controls and compliance checklist to
determine which controls and compliance best practices that need to be implemented
to improve Botium Toys’ security posture.


## Current assets

Assets managed by the IT Department include:
● On-premises equipment for in-office business needs
● Employee equipment: end-user devices (desktops/laptops, smartphones),
remote workstations, headsets, cables, keyboards, mice, docking stations,
surveillance cameras, etc.
● Storefront products available for retail sale on site and online; stored in the
company’s adjoining warehouse
● Management of systems, software, and services: accounting,
telecommunication, database, security, ecommerce, and inventory
management
● Internet access
● Internal network
● Data retention and storage
● Legacy system maintenance: end-of-life systems that require human
monitoring

##Risk assessment

#Risk description
Currently, there is inadequate management of assets. Additionally, Botium Toys does
not have all of the proper controls in place and may not be fully compliant with U.S. and
international regulations and standards.

#Control best practices
The first of the five functions of the NIST CSF is Identify. Botium Toys will need to
dedicate resources to identify assets so they can appropriately manage them.
Additionally, they will need to classify existing assets and determine the impact of the
loss of existing assets, including systems, on business continuity.

#Risk score
On a scale of 1 to 10, the risk score is 8, which is fairly high. This is due to a lack of
controls and adherence to compliance best practices.

#Additional comments
The potential impact from the loss of an asset is rated as medium, because the IT
department does not know which assets would be at risk. The risk to assets or fines
from governing bodies is high because Botium Toys does not have all of the necessary
controls in place and is not fully adhering to best practices related to compliance
regulations that keep critical data private/secure. Review the following bullet points for
specific details:
  ● Currently, all Botium Toys employees have access to internally stored data and
    may be able to access cardholder data and customers’ PII/SPII.
  ● Encryption is not currently used to ensure confidentiality of customers’ credit
    card information that is accepted, processed, transmitted, and stored locally in
    the company’s internal database.
  ● Access controls pertaining to least privilege and separation of duties have not
    been implemented.
  ● The IT department has ensured availability and integrated controls to ensure
    data integrity.
  ● The IT department has a firewall that blocks traffic based on an appropriately
    defined set of security rules.
  ● Antivirus software is installed and monitored regularly by the IT department.
  ● The IT department has not installed an intrusion detection system (IDS).
  ● There are no disaster recovery plans currently in place, and the company does
    not have backups of critical data.
  ● The IT department has established a plan to notify E.U. customers within 72
    hours if there is a security breach. Additionally, privacy policies, procedures, and
    processes have been developed and are enforced among IT department
    members/other employees, to properly document and maintain data.
  ● Although a password policy exists, its requirements are nominal and not in line
    with current minimum password complexity requirements (e.g., at least eight
    characters, a combination of letters and at least one number; special
    characters).
  ● There is no centralized password management system that enforces the
    password policy’s minimum requirements, which sometimes affects
    productivity when employees/vendors submit a ticket to the IT department to
    recover or reset a password.
  ● While legacy systems are monitored and maintained, there is no regular
    schedule in place for these tasks and intervention methods are unclear.
  ● The store’s physical location, which includes Botium Toys’ main offices, store
    front, and warehouse of products, has sufficient locks, up-to-date
    closed-circuit television (CCTV) surveillance, as well as functioning fire
    detection and prevention systems.



## Controls Assessment Checklist

Does Botium Toys currently have this control in place? 

| Yes / No | Control                | Explanation                                                                                         |
|--------------|------------------------|-----------------------------------------------------------------------------------------------------|
| No           | Least Privilege        | Currently, all employees have access to customer data; access privileges should be limited so that employees only have access necessary for their work.      |
| No           | Disaster Recovery Plan  | There are no disaster recovery plans in place. These need to be implemented to ensure business continuity.  |
| Yes          | Firewall               | The existing firewall is in good condition and has been configured according to best practices.      |
| no            | Password Policies       | There are no password policies, employees currently using weak password, making it easier for attackers to access sensitive data through employee accounts.       |
| Yes          | Antivirus              | The antivirus software is active and regularly monitored by the IT team.                            |
| No           | Backups                | The IT department should maintain data backups to ensure that in the event of an attack that compromises data, the company can quickly restore it. |
| No           | Encryption             | Currently, the company does not use encryption. Implementing it would enhance data confidentiality and security of the data.   |                                                 
| No           | IDS                    | The IT department needs an IDS in place to help identify possible intrusions by threat actors. |
| Yes          | Password Management System  | No password management system is currently in place; implementing one would enhance productivity for the IT department and other employees when dealing with password issues. |
| Yes          | CCTV                   | CCTV is installed.           |
| Yes          | Fire Detection         | Botium Toys’ physical location has a functioning fire detection and prevention system.  |


## Compliance Checklist

Does Botium Toys currenly adhrere to this compliance best practice? 

| Yes/ No | Best Practice                                               |
| :---        |    :---:                                                  |
| No | Only authorized users have access to customers’ credit card information.      |
| No | Credit card information is accepted, processed, transmitted, and stored internally, in a secure environment.              |
| No | Implement data encryption procedures                                      |
| No | Adopt secure password management policies.                   |

* GDPR
  
| Yes/ No / ? | Best Practice                                      |
| :---        |    :---:                                         |
| No | E.U. customers’ data is kept private/secured.                     |
| Yes | There is a plan in place to notify E.U. customers within 72 hours if their data is compromised                     |
| Yes | Ensure data is properly classified and inventoried.         |
| No | Enforce privacy policies, procedures, and processes to properly document and maintain data.                     |

* System and Organizations Controls 

| Yes/ No / ? | Best Practice                                       |
| :---        |    :---:                                          |
| No | User access policies are established.              |
| No | Sensitive data (PII/SPII) is confidential/private. |
| Yes | Data integrity is consistent, complete, accurate.   |
| No | Data is available to authorized users.             |


#Recomendations

To enhance Botium Toys' security posture and protect sensitive information, several controls should be implemented, including:
1. Enforce Least Privilege
2. Separation of Duties
3. Create Disaster Recovery Plan
4. Perform regular Backup
5. Establish strong password Policy
6. IImplement an IDS to monitor and respond to suspicious activity.
7. Regularly assess and update legacy systems to address vulnerabilities.
8. Use encryption to protect sensitive data, particularly customer financial information.
9. Deploy a system to manage and securely store passwords.

Additionally, Botium Toys should classify its assets properly to identify any further controls needed to strengthen security and compliance.

