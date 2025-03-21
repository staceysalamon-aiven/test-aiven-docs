---
title: Enable and manage OpenSearch® Audit logs
---

import RelatedPages from "@site/src/components/RelatedPages";

Aiven for OpenSearch® enables audit logging functionality via the OpenSearch Security dashboard, which allows OpenSearch Security administrators to track system events, security-related events, and user activity.
These audit logs contain information about user actions, such
as login attempts, API calls, index operations, and other
security-related events.

Learn how to enable, configure, and
visualize OpenSearch audit logs through the OpenSearch Security
dashboard.

## Prerequisites

-   Aiven for OpenSearch® service
-   [OpenSearch Security management enabled](/docs/products/opensearch/howto/enable-opensearch-security) for the Aiven for OpenSearch service

After enabling audit logs in the service's advanced configuration,
proceed to enable them in the OpenSearch® Security dashboard.

## Enabling audit logs in Aiven for OpenSearch

By default, audit logs are disabled in Aiven for OpenSearch. To enable
them:

1.  Access your Aiven for OpenSearch service in the Aiven Console.
2.  From the left sidebar, click **Service settings**
3.  Scroll to the **Advanced configuration** and click **Configure**.
4.  In the **Advanced configuration** dialog, click **Add configuration
    to options**.
5.  Use the search function to locate the `enable_security_audit`
    configuration and switch it to the **Enabled** position.
6.  Click **Save configuration** to save your changes and enable audit
    logging.

After enabling audit logs in the service's advanced configuration,
proceed to enable them in the OpenSearch® Security dashboard.

## Enable audit logs in OpenSearch® Security dashboard

To enable audit logs in OpenSearch® Security dashboard, follow these
steps:

1.  Log in to the OpenSearch® Dashboard using OpenSearch® Security admin
    credentials.
2.  Select **Security** from the left-side menu.
3.  Select **Audit logs**.
4.  Toggle the switch next to **Enable audit logging** to the on
    position.

:::note
The storage location for audit logs on your Aiven for OpenSearch service
is configured to be stored on the cluster's storage and cannot be
changed.
:::

## Audit log event types

OpenSearch® enables audit logging for HTTP requests(REST) and the
transport layer, capturing various events related to user
authentication, privileges, security, and more.

The following are the types of audit events recorded by OpenSearch:

-   `FAILED_LOGIN`: User authentication failure.
-   `AUTHENTICATED`: User authentication success.
-   `MISSING_PRIVILEGES`: User does not have request privileges.
-   `GRANTED_PRIVILEGES`: User's privileges successfully granted.
-   `SSL_EXCEPTION`: Invalid SSL/TLS certificate in request.
-   `opensearch_SECURITY_INDEX_ATTEMPT`: Unauthorized security plugin
    modification attempt.
-   `BAD_HEADERS`: Attempted request spoofing with internal security
    headers.

## Configure audit logging

Customize the audit logging settings in OpenSearch® Security to align
with your organization's specific requirements. The configuration
process involves two primary sections: General and Compliance settings,
each offering distinct options:

-   **General settings:** Adjust logging for REST and Transport layers,
    tailor log data for each event, and set preferences to selectively
    exclude specific users or requests, ensuring log relevance and
    operational efficiency.
-   **Compliance settings:** Enable compliance mode to meet regulatory
    standards and activate tamper-evident logging. You can also enable
    logging for internal and external configuration changes as well as
    metadata logging options for a robust security posture.

:::note
-   You cannot modify the name of the audit log index for your Aiven for
    OpenSearch service as it is set to the default name
    `auditlog-YYYY.MM.dd`.
-   You cannot change the size of the thread pool using
    `OpenSearch.yml`.
:::

### Optimize audit log configuration

Optimize audit log configuration in OpenSearch Security to protect
sensitive data from unauthorized access.

-   Exclude irrelevant event categories.
-   Consider disabling logging for Rest and Transport layers.
-   Disable request body logging for sensitive information.
-   Regularly review and maintain audit log configuration.

## Visualize audit log

Visualizing audit logs is an effective way to understand the extensive
data generated by these logs. Visualization can help identify patterns
or anomalies that may indicate security risks or system issues by
presenting the information in user-friendly graphical formats.

To access and visualize audit logs in OpenSearch:

1.  **Create an index pattern**: In the **Stack Management** section,
    establish an index pattern to organize your log data.
2.  **Create a visualization**: Go to the **Visualize** section,
    where you can design and tailor visualizations to suit your analysis
    needs.
3.  **Save and modify visualization**: Once you've created a
    visualization, save it for future reference. You can always return
    to modify and update it as your requirements evolve

<RelatedPages/>

-   [OpenSearch audit logs
    documentation](https://opensearch.org/docs/latest/security/audit-logs/index/)
