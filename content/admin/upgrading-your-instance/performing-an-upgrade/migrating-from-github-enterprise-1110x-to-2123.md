---
title: Migrating from GitHub Enterprise 11.10.x to 2.1.23
redirect_from:
  - /enterprise/admin/installation/migrating-from-github-enterprise-1110x-to-2123
  - /enterprise/admin-guide/migrating
  - /enterprise/admin/articles/migrating-github-enterprise
  - /enterprise/admin/guides/installation/migrating-from-github-enterprise-v11-10-34x
  - /enterprise/admin/articles/upgrading-to-a-newer-release
  - /enterprise/admin/guides/installation/migrating-to-a-different-platform-or-from-github-enterprise-11-10-34x
  - /enterprise/admin/guides/installation/migrating-from-github-enterprise-11-10-x-to-2-1-23
  - /enterprise/admin/enterprise-management/migrating-from-github-enterprise-1110x-to-2123
  - /admin/enterprise-management/migrating-from-github-enterprise-1110x-to-2123
  - /admin/enterprise-management/updating-the-virtual-machine-and-physical-resources/migrating-from-github-enterprise-1110x-to-2123
  - /admin/monitoring-managing-and-updating-your-instance/updating-the-virtual-machine-and-physical-resources/migrating-from-github-enterprise-1110x-to-2123
  - /admin/monitoring-and-managing-your-instance/updating-the-virtual-machine-and-physical-resources/migrating-from-github-enterprise-1110x-to-2123
intro: To migrate from {% data variables.product.prodname_enterprise %} 11.10.x to 2.1.23, you'll need to set up a new appliance instance and migrate data from the previous instance.
versions:
  ghes: '*'
shortTitle: Migrate from 11.10.x to 2.1.23
contentType: how-tos
category:
  - Back up and upgrade your instance
---

> [!NOTE]
> {% data variables.product.prodname_ghe_server %} 11.10 is an unsupported release from 2014. For a list of supported releases, see [AUTOTITLE](/admin/all-releases).

Migrations from {% data variables.product.prodname_enterprise %} 11.10.348 and later are supported. Migrating from {% data variables.product.prodname_enterprise %} 11.10.348 and earlier is not supported. You must first upgrade to 11.10.348 in several upgrades. For more information, see the 11.10.348 upgrading procedure, [Upgrading to the latest release](/enterprise/11.10.340/admin/articles/upgrading-to-the-latest-release/).
