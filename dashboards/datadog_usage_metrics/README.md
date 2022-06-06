# Datadog Usage Metrics

This dashboard provides an overview of the different usage metrics for Datadog. These are usage metrics, not billing metrics, and they do not correlate 100% to billing. These should only be used as a proxy to identify trends.
Those metrics can also be used to identify the biggest consumers with a selected tag.

![Screenshot of the Datadog Usage Dashboard](/img/datadog_usage_metrics.png)

Credits to [Nicolas Narbais](https://github.com/nxnarbais), who created the first version of this dashboard.

# How to use the dashboard

This dashboard will give you an overview of the different usage metrics of Datadog, per product. These are usage metrics, not billing metrics, and they **do not correlate 100% to billing**. These should only be used as a proxy to identify trends.

For billing information, read the official documentation on [Datadog billing](https://docs.datadoghq.com/account_management/billing).

## Template variables

With the Datadog Usage Metrics dashboard template variables you are able to select the usage coming only from one environment, service and/or team. 

The `service` and `env` variables correspond to the `service` and `env` tags, part of [unified service tagging](https://docs.datadoghq.com/getting_started/tagging/unified_service_tagging/).

The `team` tag is not a Datadog reserved tag, but it is recommended to split usage per team. If your organization uses a different tag to identify the team owning a particular metric, edit the dashboard after importing.

# Additional resources

* [Datadog billing documentation](https://docs.datadoghq.com/account_management/billing/)
