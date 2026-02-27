# SOC Level 1
This path introduces a wide array of essential defensive security topics and real-world analysis scenarios. By completing it, you will gain the knowledge and practical skills needed to become a successful SOC Level 1 Analyst, or to better structure your existing expertise if you are already working in the field.

## Introduction

The Security Operations Center (SOC) is a central hub for securing many large organizations, and junior analysts are among the most numerous and demanding roles in a SOC. In the analyst role, you will work with logs, triage and prioritize alerts, collaborate with your teammates and other departments, and be the first line of defense in reacting to cyber incidents. This comprehensive path covers the necessary technical and operational skills to make you a qualified, universal SOC analyst.

Learn the skills needed to jumpstart your career as a SOC Level 1 Analyst or Security Analyst.

Learn SOC tools and operations
Explore network and web attacks
Monitor endpoints for threats
Utilise SIEM to handle incidents

### SOC Role in Blue Team

![Diagram](images/Security-Hierarchy.png).

Looking at the diagram above, top executives like the CEO usually focus on global business objectives and don't manage technical aspects. That's why they hire a Chief Information Security Officer (CISO) or a similar role who knows the business needs and can create the most suitable security departments.

#### Security Departments
In tiny companies, the IT department takes the role of securing the company. Small to medium-sized companies may have a generic "Information Security" team that does all sorts of tasks. For this room, we will focus on bigger companies with a CISO overseeing multiple security teams, each handling a specific task. For example:

**Red Team:** Offensive security experts, pentesters, or ethical hackers who look for security issues

**GRC Team:** Specialists managing policies and ensuring compliance with regulations like PCI DSS

**Blue Team:** Defensive security experts like SOC analysts, engineers, or incident responders


### Security Operations Center (SOC)

Blue Team is about defensive security, meaning it constantly monitors for attacks and tries to respond to them quickly. Depending on a company's size and sector, Blue Team can include a lot of different roles and subdepartments, usually counting 3 to 50 members total. Now, let's explore the most common Blue Team departments.

![Diagram](images/blue1.svg).


That's where you are most likely to start your cyber security journey! SOC is the central hub for an organization's cyber security - they are the first line of defense, work with various alerts, and handle most attacks. You can read more about SOC structure in this room, but an efficient SOC is usually composed of the following roles:

**L1 Analysts:** Junior members who triage alerts and pass complex cases to L2

**L2 Analysts:** Experienced members who investigate more advanced attacks

**Engineers:** Experts in configuring security tools like EDR or SIEM

**Manager:** A person who manages the whole SOC team

### Cyber Incident Response Team (CIRT)

![Diagram](images/blue2.svg).

If SOC expertise is not enough or the incident goes out of control, you urgently call the "firefighters" - CIRT, also called CSIRT or CERT. The members should have a broad knowledge of cyber threats and handle breaches without depending on tools like EDR (Endpoint Detection and Response) or SIEM. A CIRT job is stressful and responsible, but also rewarding. Here are a few CIRT examples:

JPCERT: Japan's CERT handling nation-wide breaches
Mandiant: A private team responding to global cyber incidents
AWS CIRT: Investigates security incidents of AWS customers

### Specialized Defensive Roles

![Diagram](images/blue2.svg).

Large companies, technology-focused startups, and government agencies often require narrow and specialized Blue Team roles - exciting and highly valuable, but requiring deep topic knowledge and broad experience in broader fields like SOC or IT. These narrow roles can include:

**Digital Forensics Analyst:** Uncover hidden threats in disk and memory
**Threat Intelligence Analyst:** Gather data about emerging threat groups
**AppSec Engineer:** Maintain a secure software development lifecycle
**AI Researcher:** Study AI threats and how to defend against them

### SOC Path
Starting as a SOC L1 analyst may be a great option to broaden your cyber world awareness and better understand the more specialized roles. Moreover, even the entry-level SOC L1 role can be fun and engaging: You will deal with real attacks, protect the company from advanced threat groups, and learn a lot during the process. 

#### Internal SOC vs MSSP
Not every organization has the expertise to operate a SOC on its own and relies on a Managed Security Services Provider (MSSP), a company that delivers outsourced security services, most commonly SOC, to its clients. Working at MSSP is typically high-pressure, but it is also a good option to quickstart your career. While we recommend applying for any open SOC position as your first job, it's also important to understand the differences:

Internal SOC vs MSSP Comparison

| Topic | Internal SOC | MSSP |
|-------|-------------|------|
| **Scenario Example** | You work in a SOC team of the bank and protect the bank's systems | You work for a global MSSP protecting its sixty customers in Europe |
| **Working Pace** | You usually have calm shifts without too much time pressure | Your shift usually starts from a queue of urgent alerts to analyze |
| **Security Tools** | You work with just a few tools, but need to know them very well | You have to work with sixty diverse security tools and platforms |
| **Incident Practice** | You saw and learned from just two major cyber attacks last year | Every week, you deal with attacks and breaches, and can learn from it |

### SOC L1 Alert Triage

#### From Events to Alerts

First, an event must occur, like user login, process launch, or file download. Then, the system, like your OS, a firewall, or a cloud provider must log the event. After that, all system logs must be shipped to a security solution like SIEM or EDR. The SOC team can receive millions of logs per day from thousands of different systems, where most of the events are expected, but some require attention. Alert, a notification generated by a security solution when a specific event or sequence of events occurs, is what saves SOC analysts from manual log review by highlighting only suspicious, anomalous events. With alerts, analysts triage just dozens of alerts per day instead of millions of raw logs.

**Alert Management Platforms**

| Solution        | Examples                     | Description |
|----------------|------------------------------|------------|
| SIEM System    | Splunk ES, Elastic           | SIEM systems have solid alert management capabilities and are a perfect choice for most SOC teams. |
| EDR or NDR     | MS Defender, CrowdStrike     | While EDR and NDR provide their own alert dashboards, it is preferred to use SIEM or SOAR for centralized alert management. |
| SOAR System    | Splunk SOAR, Cortex SOAR     | Larger SOC teams can use SOAR to aggregate and centralize alerts from multiple security solutions. |
| ITSM System    | Jira, TheHive                | Some teams may have a custom ticket management (ITSM) setup using a dedicated solution. |

### L1 Role in Alert Triage
SOC L1 analysts are the first line of defence, and they are the ones who work with alerts the most. Depending on various factors, L1 analysts may receive zero to a hundred alerts a day, every one of which can reveal a cyberattack. Still, everyone in the SOC team is somehow involved in the alert triage:

* SOC L1 analysts:  Review the alerts, distinguish bad from good, and notify L2 analysts in case of a real threat
* SOC L2 analysts:  Receive the alerts escalated by L1 analysts and perform deeper analysis and remediation
* SOC engineers:  Ensure the alerts contain enough information required for efficient alert triage
* SOC manager:  Track speed and quality of alert triage to ensure that real attacks won't be missed

Now that you know how alerts are generated, it's time to review their content. While the details differ for every SIEM or security solution, the alerts generally have a few main properties you must understand before taking them. Don't worry if you find some confusing, as you will hear more about some in the upcoming tasks.

![Diagram](images/sco01.png).

## Alert Properties

| No | Property            | Description | Examples |
|---|---------------------|------------|----------|
| 1 | Alert Time          | Shows alert creation time. The alert usually triggers a few minutes after the actual event. | Alert Time: March 21, 15:35 <br> Event Time: March 21, 15:32 |
| 2 | Alert Name          | Provides a summary of what happened, based on the detection rule's name. | Unusual Login Location <br> Email Marked as Phishing <br> Windows RDP Bruteforce <br> Potential Data Exfiltration |
| 3 | Alert Severity      | Defines the urgency of the alert. Initially set by detection engineers, but can be altered by analysts if needed. | 🟢 Low / Informational <br> 🟡 Medium / Moderate <br> 🟠 High / Severe <br> 🔴 Critical / Urgent |
| 4 | Alert Status        | Indicates whether someone is working on the alert or if triage is completed. | 🆕 New / Unassigned <br> 🔄 In Progress / Pending <br> ✅ Closed / Resolved <br> (Custom statuses may exist) |
| 5 | Alert Verdict       | Also called alert classification. Explains whether the alert is a real threat or false alarm. | 🔴 True Positive / Real Threat <br> 🟢 False Positive / No Threat <br> (Custom verdicts may exist) |
| 6 | Alert Assignee      | Shows the analyst assigned to review the alert. The assignee takes responsibility for handling it. | Assignee may also be called Alert Owner |
| 7 | Alert Description   | Explains what the alert is about, usually structured in three parts. | Detection rule logic <br> Why the activity may indicate an attack <br> Optional triage guidance |
| 8 | Alert Fields        | Contains SOC analyst comments and values that triggered the alert. | Affected Hostname <br> Entered Command Line <br> Other relevant technical fields |


Okay, you can now read and understand the alert. What's next? Recall the second task, where you see hundreds of alerts but have to choose which to pick up first. The process of deciding which to take is called Alert Prioritisation, and it is crucial to ensure timely detection of a threat, especially with many alerts in the queue.

Finally, you are ready to review the chosen alert! The process is quite operationally heavy, but you will soon see why every step is important. Also, note that the alert review by SOC analysts can also be called alert triage, alert handling, alert processing, alert investigation, or alert analysis. During this module, we will stick to the Alert Triage option.

![Diagram](images/blue2.svg).

#### Initial Actions
The initial steps are designed to ensure that you take ownership of the assigned alert and avoid interfering with alerts being handled by other analysts, and confirm that you are fully prepared to proceed with the detailed investigation. You achieve it by first assigning the alert to yourself, moving it to In Progress, and then familiarising yourself with the alert details like its name, description, and key indicators.

#### Investigation
This is the most complex step, requiring you to apply your technical knowledge and experience to understand the activity and properly analyse its legitimacy in SIEM or EDR logs. To support L1 analysts with this step, some teams develop Workbooks (also known as playbooks or runbooks) - instructions on how to investigate the specific category of alerts. If workbooks are not available, below are some key recommendations:

Understand who is under threat, like the affected user, hostname, cloud, network, or website
Note the action described in the alert, like whether it was a suspicious login, malware, or phishing
Review surrounding events, looking for suspicious actions shortly after or before the alert
Use threat intelligence platforms or other available resources to verify your thoughts

#### Final Actions
Your decisions here determine whether you found or missed the potential cyberattack. Some actions like Escalation or Commenting will be explained in the following rooms, so don't worry if they sound complex right now. First, decide if the alert you investigated is malicious (True Positive) or not (False Positive). Then, prepare your detailed comment explaining your analysis steps and verdict reasoning, return to the dashboard and move it to the Closed status.

