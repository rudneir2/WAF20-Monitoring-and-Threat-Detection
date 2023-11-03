# WAF20 - Monitoring and Threat Detection

**NOTE:** 
This content below is supposed to be part of the WAF 20 document, to be embedded in the chapter "WAF > Recommendations > SE:10 Monitoring and Threat Detection".

https://review.learn.microsoft.com/en-us/azure/well-architected/security/monitor-threats?branch=release-waf-2-0-1

## Introduction / Use case

Well-Architected Framework for **Monitoring and Threat Detection** provides a holistic perspective regarding monitoring and how to use different solutions to help you detect threats in your IT environment. It will also help you with best practices to be applied in your strategy to plan your entire monitoring solution and understand how to integrate solutions that are available.

![image](https://github.com/rudneir2/WAF20-Monitoring-and-Threat-Detection/assets/97529152/6f50c249-d1ce-4830-98c7-91cfca25bd6b)

Let's consider the following use case in the diagram above:

1. in a hybrid IT environment we have different "personas" accessing different resources, and as always, any persona may become a bad actor and make use of different tactics and tools to compromise your IT environment.

2. Azure allows you to send logs from different sources to Log Analytics, which is used as a central repository for all your logs, that you will use to monitor your environment and detect potential threats.

3. logs from different resources on your on-premises environment such as Virtual Machines, network security appliances, applications, and Domain Controllers may be sent to Azure and then used to detect potential threats

4. you will be able to collect information from native Azure resources as well, including Virtual Networks, Public IPs, VMs, Storage, Azure subscription activities, and Entra ID logs

5. not only from primary infrastructure services as mentioned above, but logs from Security services may also be collected, and they are very helpful to be correlated with others' logs to get a better insight into your environment

6. all logs stored on Log Analytics may be integrated with an SIEM solution such as Microsoft Sentinel, so you may build alerts that become incidents that can be treated by a SOC team. The SIEM will be able to add Threat Intelligence indicators to be correlated with your logs and an automated solution (SOAR) to respond to the incidents identified in your environment. Microsoft SIEM (Sentinel) still offers different ways to identify anomalies in your logs through Machine learning algorithms as well.

7. besides logs from different resources, other types of information may be collected and aggregated according to the type of solution. Inbound and Outbound packets to your Azure Network may be aggregated by NSG and analyzed by Traffic Analytics.

8. Different types of applications may have logs aggregated and filtered through Application Insights, part of Azure Monitor solution, which also uses Log Analytics to store those application logs.

9. capturing changes made in your operating systems, such as etc files on Linux or register files on Windows is very important to keep your VMs consistent and secure. Microsoft Defender for Cloud offers a solution to monitor those system file changes in case they occur.

10. most companies have a hybrid identity environment, such as Active Directory Domain Services (ADDS) using Kerberos tickets and Azure AD (now Entra ID) that uses Oauth protocol to provide authentication, both synchronized through solutions such as ADFS or ADConnect. Those providers need a layer of security, that in most case are delivered by solutions such as Microsoft Defender for Identity that works to secure ADDS and Azure AD Identity Protection.

The use case above is just some examples so you may understand that your monitoring strategy to detect threats may be integrated among different solutions to provide you with better insights.
Some companies use other Microsoft solutions as well, such as Microsoft Defender for Endpoint, as shown in the diagram, part of XDR solution and sometimes third part solutions integrated with Log Analytics.


**NOTE:**
If you'd like to understand more about any solution described in the diagram, including acronyms, please refer to this table of contents, from the Baseline chapter.
(table to be built)

**From this point on, we could add the current draft content for Monitoring and Threat Detection**
