---
title: View your environments
linkTitle: View your environments
weight: 10
date: 2020-12-14
description: All of your environments displayed in one place.
---

{{< alert title="Public beta" color="warning" >}}This feature is currently in **public beta** and not yet available for production use.{{< /alert >}}

The environments page contains all of your environments in a searchable and sortable list. This list contains:

* Axway Cloud SaaS environment
* Environments using a service mesh gateway
* Environments using the API service model
    * AWS Gateway environments
    * API Manager environments
    * Environments that have been defined manually using the AMPLIFY Central CLI or APIs

To add a new environment, click **+ Environment**.

![Environment List Page](/Images/central/EnvironmentListPage.png)

This page can be sorted by an environment's logical name, title, or by the time that they were created or last modified. To sort the list, select the desired option from the dropdown menu.

You can search the environments by their logical name, title, or any tags that are attached to it.

Each environment in the list contains some basic information, describe as follows:

![Environment Results Details](/Images/central/EnvironmentListResult.png)

1. Title.
2. Logical name.
3. An icon.
4. The connection status of any AWS Gateway or API Manager discovery and traceability agents that you have connected to the environment.  It will display MANUAL SYNC if there is not an agent connected.
5. Description.
6. Tags.
7. The number of service assets housed in the environment.
8. The user who last modified the environment, and when.
9. Menu with an option to delete the environment.

You can click the title or logical name of the environment to view additional details.

## View environment details

For environments created using the API service model, the details page lists the title of the environment along with the status of any connected discovery and traceability agents; and sections Environment Information, Activity Report, and Services Table.

For more information about other types of environments, see:

* [Mesh Environment Management](/docs/central/mesh_management/)
* [Axway Cloud SaaS: Get Started](/docs/central/quickstart/)

![Environment Details Page](/Images/central/EnvironmentDetailsPage.png)

* **Environment Information**: This section contains general information and any tags or attributes that are specific to the environment asset. Attributes in this context are key and value pairs used for extending functionality and integrations with third-party systems.
* **Activity Report**: Dashboard, which shows the aggregated values for how your environment assets are distributed and how many subscriptions exist across all of those assets.
    * Services: The total count of services represented in the environment.
    * Catalog Items: The total count of published catalog items.
    * Subscriptions: The total count of subscribers to all the published catalog items.
* **Services Table**: This table is a representation of all of the services that exist within the environment. It is sortable by title, logical name, and when the service was created or last modified. You can search by title, name, or tag. For each service, it shows the number of versions, the user who last modified the service, and when. Click a service from the list to see its details.

## Delete a service

To delete a service, click the **Ellipsis** icon, at the far right of the service's row, then click **Delete** on the menu that is shown.

## View the details of an API Service

To view the details of your API Service and its versions, click a service from the **Service Table** list.

Select which version of your API service to view by using the dropdown selector located beside the name of your service.  The most recent version is displayed by default.

![Service Details Page](/Images/central/ServiceDetailsPage.png)

The following describes the sections on the API Service details page:

* **Service Information**: Contains general information and any tags or attributes that are specific to the service asset. Attributes in this context are key and value pairs used for extending functionality and integrations with third party systems.
* **Activity Report**: Dashboard, which shows the aggregated values for how your service version assets are distributed and how many subscriptions exist across all of those assets.
    * Endpoints: The total count of endpoints associated with this service version.
    * Catalog Items: The total count of successfully published items in the Unified Catalog. This number might differ from the number of items available in the **Catalog Items** table. This count only recognizes items that are available in the Unified Catalog, whereas the table also contains items that were not published or that are in an error state.
    * Subscriptions: The total count of subscribers to all the published catalog items.
* **Version Information**: Contains information specific to the version that you have selected from the dropdown menu. Includes the type of specification represented by the service version (OAS2, OAS3, WSDL, Protobuf, and so on.)
* **Specification tab**: Displays the contract or methods for your selected API service version. Some specification types provide a visualization of your API methods, and some fields are collapsible. You can see additional information by clicking to open relevant methods or models.
* **Endpoints tab**: Contains a table listing the URLs pointing to deployed instances of the API service.
* **Catalog Items tab**: Contains a table listing both successfully published and unpublished items in the Unified Catalog. Each entry contains the state of the item (PUBLISHED, UNPUBLISHED, or IN ERROR).

## Delete endpoints and catalog items

To delete an endpoint or catalog item, click the **Ellipsis** icon, at the far right of the item's row, then click **Delete** on the menu that is shown.
