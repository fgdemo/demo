# Secure Your Infrastructure
Securing your Oracle Enterprise Manager deployment involves securing all layers of the stack starting with the underlying operating system (OS) on which the OMS and Repository reside all the way up to the Enterprise Manager components themselves. These recommendations will increase overall security as well as prevent certain DoS attacks.

# Secure the Infrastructure and Operating System
Harden the machines themselves by removing all unsecure services such as rsh, rlogin, telnet, and rexec on Linux platform (for the list of unsecure services and how to remove them on different platforms, please refer to the CIS benchmarks). It is also recommended to stop non-essential services, this minimizes the ’attack footprint' of the host and reduces resource consumption by services that are not required, freeing up system resources to deliver the best performance from the OMS.

Ensure that all the Oracle Homes are patched with the latest CPU (Critical Patch Update). This is a recommended best practice for securing the Oracle Management Service, Repository, Agents and managed targets. Setup your My Oracle Support credentials to detect new Security Alerts and CPUs from the Patch Advisor.

With the default Security Recommendations for Oracle Products compliance standard, when a target is missing the latest Security patches, a compliance standard violation will be triggered. In addition, the Secure Configuration for Host should be associated to the hosts of the OMS and Repository. There are additional compliance standards for Database and WLS that can be applied depending on your level of security. Review the Oracle Enterprise Manager Cloud Control Administrator's Guide section on Compliance for more information on available compliance standards and how to associate targets.

# Securing the Oracle Management Repository
In addition to the above recommendations, steps are necessary to secure the Oracle Management Repository. Since the Oracle Management Repository resides within an Oracle database, a number of the best practices for securing the Oracle database itself are applicable to securing the Repository as well. For best practices on Oracle database security, please refer to the Oracle Database Security Checklist.

The above document also covers certain Operating System level steps that need to be performed to secure the database. Following are additional recommendations to be implemented in the Enterprise Manager deployment.

#Enable Advanced Security Option
Enable Advanced Security Option (ASO) between the OMS and Repository to ensure that the data between the OMS and Repository is secure both from confidentiality and integrity standpoints. In addition to the ASO configuration required on the Repository database, you will need to configure the OMS and Agent to connect to a secure Repository database. The detailed instructions for implementing ASO for Enterprise Manager can be found in the Enterprise Manager Security section of the Oracle Enterprise Manager Cloud Control Administrator's Guide.

# Restrict Network Access
Restrict network access to the host on which the Repository resides by putting the repository database behind a firewall and checking network IP addresses. The Listener should be configured to accept requests only from OMS nodes by adding the following parameters into TNS_ADMIN/protocol.ora file:
* tcp.validnode_checking =YES
* tcp.excluded_nodes = (list of IP addresses)
* tcp.invited_nodes = (list of IP addresses), list all OMS nodes here)
The first parameter turns on the feature whereas the latter parameters respectively deny and allow specific client IP addresses from making connections to the Oracle listener. Please refer to the Secure the Network Connection section of the Oracle Database Security Guide for more information.

# Securing the Oracle Management Agent
For better security during agent installation, agents should be deployed using Enterprise Manager Enterprise Manager's Agent Deploy which uses the secure SSH protocol. When manually deploying Agents, to protect against the possibility of users installing unauthorized agents, use one-time registration passwords that have a reasonable expiry date instead of persistent registration passwords. Registration passwords can be created in the Console or by using the emctl secure setpwd command.

Install the agent as a separate user from OMS installation and support only impersonation based access to this account such as sudo or PowerBroker post installation to prevent unauthorized changes.
