---
description: Learn how to deploy SaaS applications on the cloud.
---

# About SaaS Applications

A SaaS application is an application that a vendor offers as a service in the cloud. Customers of the vendor subscribe to the service and use the application when they need it. To a SaaS vendor, each subscriber \(or customer\) is a tenant.

## Architectural Patterns

A SaaS application can be deployed in the cloud by using the following architectural patterns:

* A single, tenant-aware application instance In this pattern, the SaaS vendor deploys a single application instance, which all the tenants use. The application handles the separation of the tenant-specific workloads and data.

All the tenants get the same application version, built from a common code base. Because all the application deployments are based on the same code, the vendor can configure, patch, and upgrade the service efficiently. Scaling and operating the service is easy.  
However, building a tenant-aware application environment requires more effort initially. And this deployment pattern is not suitable for SaaS customers that require complete isolation.

* Multiple tenant-specific application instances This pattern is the focus of the solution.

The SaaS vendor deploys and manages multiple isolated application instances. Each deployment is for a specific tenant. The SaaS vendor manages the individual tenant application instances through a common management layer.

The vendor can choose to either build all the tenant application instances from a single code base or offer customized versions of the application to each tenant. This pattern is ideal for SaaS customers that require complete isolation of the application environment.

## Architecture

This architecture shows an Oracle Cloud Infrastructure tenancy that hosts multiple tenants of a SaaS vendor. All the resources in the architecture are in a single region.

The SaaS vendor's management infrastructure and the application resources of each tenant are isolated in separate compartments and virtual cloud networks \(VCNs\). Network isolation ensures that the applications and data are segregated from the other deployments in the tenancy. Compartments ensure logical isolation of the resources and enable granular access control.  


