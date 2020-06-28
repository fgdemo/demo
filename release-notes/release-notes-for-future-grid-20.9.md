---
description: >-
  Learn about the new features, enhancements, bugs fixes and known issues in
  this release.
---

# Release Notes for Future Grid 20.9

## Known Upgrade Issues

This section covers issues related to upgrading to Enterprise Manager Cloud Control 12c Release 5 \(12.1.0.5\).

### 2-System Upgrades On Same Host Not Supported

The 2-system upgrade option is not supported if upgrading from Enterprise Manager Cloud Control releases 10.2.0.5/11.1.0.1 to release 12.1.0.x on a host where an existing Oracle Management Service release 10.2.0.5 or 11.1.0.1 instance is already deployed.  
\(Bug 12957922\)

### Agent Upgrade Will Fail If Agent Instance Home Is Inside Agent Oracle Home

Upgrading a Management Agent will fail if the Agent instance home is inside the Management Agent Oracle home.

For example:

* Agent Oracle Home: /myhost/agent/core/12.1.0.3.0
* Agent Instance Home: /myhost/agent/core/12.1.0.3.0/agent\_inst

To avoid the upgrade failure, migrate the Agent instance home outside of the Agent Oracle home before beginning the Agent upgrade.

\(Bug 18286125\)  


