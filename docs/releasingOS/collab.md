### Collaboration and governance models 

Open-sourcing a project allows others to leverage the code, but the ultimate goal is often that the open-source community adopts and helps extend and evolve the project. How projects govern this shared development is diverse. A commonality across all projects is that the repository, and it’s main/production branch, will have some form of write access control, meaning a level of governance is present even if it’s not formalised. 

#### What different governance models exist for open source? 

There is no definitive definition of open-source governance models. The following models are based on mapping Redhat (https://www.redhat.com/en/blog/understanding-open-source-governance-models and https://opensource.com/article/20/5/open-source-governance) and Linux Foundation (https://www.linuxfoundation.org/tools/open-source-reading-list/) notes to the packages relevant to clinical reporting. 

#### Single Entity 

This category refers to a project where a single entity is the final decision maker, regardless of whether that single entity is an individual, a company or other legal entity. This governance model is sometimes referred to as the “privately open source”, “founder-leader”, or “benevolent dictator” model. The single entity controls which pull requests go to master and provides instruction on how new code should integrate in order to be accepted. Famous examples are Python until 2018 and Linux. Within pharmaverse.org, diffdf and many of the single company governed packages are an example of this governance model. 

#### Steering Group 

This category refers to a project where the ultimate decision-making capacity is shared between more than one entity. The structure of the group and manner in which the group makes decisions can vary. The name used to refer to the group can also vary, examples include “governing board”, “steering group”, and “council”. A famous example includes the relatively oligarchical Python Steering Council from 2018, however many projects prefer simple democracies, or merely that a sufficient number of approvals from among the contributing entities are sufficient to approve acceptance to the production branch. Within pharmaverse.org, admiral is an example of this governance model. 

#### Do-ocracy 

This category refers to a project where access to the production branch is given out fairly freely, usually based on prior interactions with the primary contributors, or actual contributions via external pull requests. Trust is placed in the community to come to an agreement regarding acceptance to the production branch. This category is sometimes also referred to as a “self-governed” or “non-governed” governance model. Within pharmaverse.org, visR is an example of this governance model. 

#### Foundation governed 

A legal body (e.g., non-profit) assumes control - an example organisation is the Linux Foundation which governs many projects, while in Pharma there are parallels to efforts like Transcelerate and OHDSI. There are no examples of this model within pharmaverse.org, but R/Pharma repositories do follow this model, where the registered non-profit Open Source in Pharma governs the github organisation.   

If two or more companies want to formally collaborate on an open-source project, what is the role of legal contracts between the companies when the code is open-source? 

Contributions to open-source code can come in many forms, and there is a great deal of diversity in projects relevant to clinical reporting. This is an emerging area for pharma companies, and so we will focus on promoting awareness, rather than giving firm guidelines.  

### When do we need contracts?  

When initiating a project like an R package, or when another company is considering investing in collaboration to an existing project, there could be a discussion on having a legal framework layered on top of the collaboration. To help contextualise this, we will use four example projects. 

`dplyr`: The dplyr project is a ubiquitous in pharma, but is a generic data science package for data munging. The code owners are listed as an individual from a vendor, academia and a consultancy and it’s released under a permissive license. This package is extensively consumed, and a core dependency in data related packages like admiral. This package is heavily depended on Pharma, but no legal agreement exists beyond the permissive licencing on the project. 

`gt`: There is a large spread of table generation packages in Pharma, but several Pharma companies (Roche and GSK – add links to their issues before pub) have publicly been exploring extensions that would allow the use of gt in TLG generation for CSRs. No legal agreement exists beyond the permissive licencing on the project. 

`pkglite`: Submitting code to the FDA requires collapsing the contents into text files with restrictive formats. pkglite exists to collapse and reconstitute an R package before and after the eCTD submission portal. pkglite uses a copy-left license, and copyright is owned by Merck. No legal agreement exists beyond the copy-left licencing on the project. 

`admiral`: admiral is an R package for creating ADaM datasets. The copyright is held between Roche and GSK, and it is permissively licensed. A contract exists between Roche and GSK on their collaboration model. Other Pharma’s have contributed and offered to extend admiral without legal contracts in place on the original codebase. 

The examples above were intended to highlight that the majority of R packages used by Pharma companies are done so without legal contracts in place, beyond the license of the project, even when some collaboration takes place.  

It remains a discussion point though whether licenses are required, and the decision to create a license may become relevant if companies want to formally pool resources. It’s important to note that with permissively license projects, it is possible that if two entities want to take a package in different directions, they are able to by forking the project. So, contributions to another entities package are not lost to the contributing company. 