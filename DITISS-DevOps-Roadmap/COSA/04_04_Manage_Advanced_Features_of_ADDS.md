# Introduction
---
Learn about advanced Active Directory Domain Services administration tasks, including creating trust relationships, implementing Enhanced Security Administrative Environment (ESAE) forests, monitoring and troubleshooting AD DS replication, and creating custom AD DS partitions.

---
## Scenario

Contoso, Ltd. is a financial services company in Seattle with major offices located throughout the world. Most of its compute environment runs on-premises on Windows Server. This includes virtualized workloads on Windows Server 2016 hosts.

Contoso's IT staff are migrating Contoso on-premises servers to Windows Server 2025. As part of the migration, Contoso plans to expand into additional sites and use virtualization to help expedite bringing a new site online. The company is also generating larger volumes of data with plans for even more data in the future. Because of this, the company needs flexible storage options. Finally, Contoso plans to increase the use of virtualization to optimize their computing environment because many physical servers are underutilized.

As part of its technology expansion and modernization initiative, Contoso plans to consolidate its existing AD DS environment comprising several isolated AD DS forests, starting with the creation of trust relationships between them. Another major change that’s scheduled to take place in the upcoming months is a setup of an ESAE forest. Additionally, to facilitate deployment of a new in-house developed suite of applications, it’s necessary to create a custom AD DS partition.

As an experienced Windows Server administrator, you’re responsible for planning and implementing these changes. Throughout their implementation, you also need to ensure that the environment you manage remains fully operational. This includes monitoring and troubleshooting AD DS replication.

### Learning objectives
After completing this module, you'll be able to:

* Identify the purpose, types, and the process of creating trust relationships.
* Describe the purpose and the process of implementing ESAE forests.
* Monitor and troubleshoot AD DS replication.
* Identify the purpose and the process of creating custom AD DS partitions.

### Prerequisites
To get the best learning experience from this module, you should have knowledge and experience of the following areas:

* Windows Server administration.
* Core networking technologies.
* Implementing and managing AD DS.

---
# Create trust relationships

An AD DS forest represents a security boundary, providing secure authentication and authorization for its users, computers, and applications. Sometimes, it might be necessary to extend this boundary to include other AD DS domains and forests. This, for example, might result from mergers and acquisitions between organizations, or from consolidation initiatives, as is the case with Contoso.

### What is a trust relationship?
AD DS trusts enable access to resources in a multiple-domain and multiple-forest AD DS environment. In a single-domain forest, all users and resources, such as file shares, printers, or applications share the same domain, so access management is straightforward and readily available. When you have multiple domains or forests, you need trusts to provide users in one domain with secure access to resources in another domain.

In a multiple-domain AD DS forest, by default, domains form a tree-like structure with a two-way transitive trust relationship between directly adjacent domains. Trust transitivity implies that a path of trust exists between all the AD DS domains in the same forest. Additionally, you can create other types of trusts. The following table describes the main trust types.

| Trust Type | Trust Characteristics | Direction | Description |
|------------|----------------------|-----------|-------------|
| **External** | Nontransitive | One-way or two-way | Enables resource access with an individual AD DS domain in another forest. |
| **Realm** | Transitive or nontransitive | One-way or two-way | Establishes an authentication path between a Windows Server AD DS domain and a Kerberos v5 realm implemented using a directory service other than AD DS. |
| **Forest (complete or selective)** | Transitive | One-way or two-way | Allows two forests to share resources. |
| **Shortcut** | Nontransitive | One-way or two-way | Reduces the time required to authenticate between two non-adjacent domains in the same multi-domain AD DS forest. |

![Diagram](images/m9-shortcut-trust-cafa4e1c.png).

> [!NOTE]
> Forest trust relationships provide most flexibility from the authentication standpoint. They're also easier to establish, maintain, and administer than separate trust relationships between external, domain-level trusts and individual domains across the two forests.

![Diagram](images/m9-forest-trust-5cc921f4.png).
