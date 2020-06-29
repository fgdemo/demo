---
description: Learn about the policies required for hosting SaaS applications.
---

# Required Policies

## Oracle Management Agent

Oracle Management Agent \(Management Agent\) is an integral software component that is deployed on each monitored host. It is responsible for monitoring all of the targets running on those hosts, communicating that information to the middle-tier Oracle Management Service, and managing and maintaining the hosts and its targets.

## Oracle Management Service

Oracle Management Service is a Web-based application that orchestrates with the Management Agents and the Management Plug-ins to discover targets, monitor and manage those targets, and store the collected information in a repository for future reference and analysis. Oracle Management Service also renders the user interface for Enterprise Manager Cloud Control.

Oracle Management Services is deployed to the Oracle middleware home \(middleware home\), which is the parent directory that contains the Oracle WebLogic Server home, the Oracle Management Service home, the Management Agent home, the plug-in home, the Java Development Kit \(JDK\), the Oracle Management Service instance base directory, the Oracle Web tier directory, the Oracle common directory, and other relevant configuration files and directories.

While deploying the Oracle Management Service, the Enterprise Manager Cloud Control Installation Wizard installs Oracle WebLogic Server if it does not already exist in your environment. As a result, an Oracle WebLogic Server administration console is also installed.

## Oracle Management Repository

The Oracle Management Repository \(Management Repository\) is a storage location where all of the information collected by the Management Agent is stored. It consists of objects such as database jobs, packages, procedures, views, and tablespaces.

Technically, the Oracle Management Service uploads the monitoring data it receives from the Management Agents to the Management Repository. The Management Repository then organizes the data so that it can be retrieved by the Oracle Management Service and displayed in the Enterprise Manager Cloud Control console. Because data is stored in the Management Repository, it can be shared between any number of administrators accessing the Enterprise Manager Cloud Control.

{% embed url="https://youtu.be/5fBAfr36XkE" %}



