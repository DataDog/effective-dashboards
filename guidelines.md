# Dashboarding best practices

The main goal of "Effective Dashboards" is to create a set of best practices and guidelines on what makes a dashboard effective and useful. 

You can read the current guidelines and best practices, and/or contribute to improve the guide.

## The goal of the dashboard

When designing an effective dashboard it is important to think about the goal of that dashboard. Is the goal to have an overview of a particular service? Is it to help debugging a specific issue? Is a way for its consumers to learn better about their resources?

Thinking about the goal for the dashboard helps deciding what type of widgets and what data needs to be part of the dashboard. A dashboard with just a couple of widgets is perfectly valid, if it has a clear goal and that goal only needs a couple of widgets. There is no need to clutter the dashboard.

## Types of dashboard

When creating a new dashboard, there are three types of dashboards to select from "Dashboards", "Timeboards" or "Screenboards". "Dashboards" is the new grid layout that has nice features like coloured groups or high density mode. For new dashboards the recommendation is to use the "Dashboards" layout.

![Screenshot of the new dashboard window](/assets/img/new_dashboard.png)

## The dashboard description field

When creating a new dashboard there is an option to add a description to the dashboard, hidden under the down arrow to the right of the dashboard title:

![Image highlighting the arrow to show the dashboard description](/assets/img/description_arrow.png)

The description field will be very useful for teams that are not that familiar with the dashboard and don't use it on a daily basis, so adding a clear description is a must for an effective dashboard. The description fields accepts Markdown, so you can add headers, lists, links, etc.

![Example of a description of a dashboard](/assets/img/discounts_service_overview.png)

## Template variables

[Template variables](https://docs.datadoghq.com/dashboards/template_variables/) allow you to dynamically filter one or more widgets in a dashboard. Although this feature is useful in many dashboards, it is particularly useful on dashboards aimed to be as generic and resuable as possible, like the dashboard for integrations or the ones shared in this repository.

![Example of template variables in a dashboard](/assets/img/template_variables.png)

When adding a template variable to a dashboard, describe it in the dashboard description.

## Groups

Widget grouping allows to nicely group related widgets together, with a nice header color coded header. It is recommended to always group related widgets together (even without a header), and even to always add widgets to a group, even if they are the only widget in the group, as [that will affect how those widgets are displayed in low and high density modes](#high-density-mode).

![Example of a group in a dashboard](/assets/img/groups.png)

## Column Layout

The recommended "Dashboards" layout is a 12-column layout, where you can place and resize widgets.

![12 column layout](/assets/img/12_column.png)

### High Density Mode

When using Datadog in large screens, Datadog activates the "High Density Mode". This mode displays group widgets in a dashboard side-by-side for increased widget density.

![High density mode](/assets/img/high_density_mode_example.png)

When activated, a new button appears in the top right corner of the dashboard, that allows to manually deactivate it:

![High density mode button](/assets/img/high_density_mode.png)

This mode basically duplicates the layout into a 2 x 12 column grid, but not a 24 column grid. This means that the widget maximum width continues to be 12 column.

### Widget recommended minimum width

* Timeseries widgets should be at least 4 columns wide in order not to appear squashed on smaller displays.
* Stream widgets (like logs) should be at least 6 columns wide (half the dashboard width) for readability. 
