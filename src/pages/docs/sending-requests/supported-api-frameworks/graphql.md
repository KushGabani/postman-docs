---
title: "Querying with GraphQL"
order: 37
page_id: "graphql"
contextual_links:
  - type: section
    name: "Prerequisites"
  - type: link
    name: "Installing and updating"
    url: "/docs/getting-started/installation-and-updates/"
  - type: section
    name: "Additional Resources"
  - type: subtitle
    name: "Related Blog Posts"
  - type: link
    name: "Postman v7.2 Supports GraphQL"
    url: "https://blog.postman.com/postman-v7-2-supports-graphql/"
  - type: link
    name: "Working with GraphQL template"
    url: "https://www.postman.com/postman/workspace/postman-team-collections/collection/1559645-c0dd3eb3-5258-4ddd-a6e4-2780c5212e33?ctx=documentation"
  - type: subtitle
    name: "Video"
  - type: link
    name: "GraphQL in Postman Demo"
    url: "https://youtu.be/7pUbezVADQs"
  - type: section
    name: "Next Steps"
  - type: link
    name: "Grouping requests in collections"
    url: "/docs/sending-requests/intro-to-collections/"

warning: false

---

Many people think of Postman as an advanced REST client. Beyond REST, Postman is a tool that handles any calls sent over HTTP. This means that you can use Postman to interact with protocol-agnostic APIs - such as [SOAP](/docs/sending-requests/supported-api-frameworks/making-soap-requests/) and GraphQL, which can both utilize HTTP, just like REST.

Learn how Postman supports working with GraphQL.

* Sending GraphQL queries in request body as POST requests
* Support for GraphQL variables
* Creating APIs in Postman with GraphQL schema type
* Query autocompletion integrated with user defined GraphQL schemas

Try it out in Postman with this [example template](https://www.postman.com/postman/workspace/postman-team-collections/collection/1559645-c0dd3eb3-5258-4ddd-a6e4-2780c5212e33?ctx=documentation).

[![graphql template](https://i.imgur.com/Ic70c1G.png)](https://i.imgur.com/Ic70c1G.png)

## Sending a GraphQL query

<iframe loading="lazy" width="560" height="315" src="https://www.youtube-nocookie.com/embed/7pUbezVADQs" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<br/>

There's a few ways for you to author and send a GraphQL query in Postman. The following screen illustrates one way to send a GraphQL query using Postman's inbuilt support.

[![graphql body](https://assets.postman.com/postman-docs/GraphQL-Body.png)](https://assets.postman.com/postman-docs/GraphQL-Body.png)

Under the **Body** tab, select the **GraphQL** body type. Enter your GraphQL query in the **Query** editor. This editor enables you to author both queries and variables separately, as described in the following section.

## Working with GraphQL variables

Postman provides a separate interface to author GraphQL variables. After defining your GraphQL query in the **Query** editor, you can author and edit GraphQL variables in the adjacent variables editor.

You can also [use Postman variables](/docs/sending-requests/variables/) as data inputs for GraphQL variables using `{{variable}}` syntax.

[![edit variables](https://assets.postman.com/postman-docs/GraphQL-Body-Variables.png)](https://assets.postman.com/postman-docs/GraphQL-Body-Variables.png)

## Importing GraphQL schemas

To [create or import a GraphQL schemas](/docs/designing-and-developing-your-api/the-api-workflow/) into Postman, complete the following steps.

1. Under the **APIs** tab, click **+ New API**.

    <img src="https://assets.postman.com/postman-docs/create-api-v9.jpg" alt="New API" width="350px" />

1. Enter a name and version for your API.
1. Choose **GraphQL** from the **Schema type** dropdown list.
1. Choose either **JSON** or **GraphQL SDL** from the **Schema Format** dropdown list.
1. You can optionally select the **Import** tab to import an API specification directly from either a local file or a GitHub or Bitbucket repo. If you don't import a schema, Postman will populate your API with a sample specification you can edit at any time.
1. Click **Create API**.
1. Open the new API's version page, and navigate to the **Definition** tab to edit your schema.

## Autocomplete for GraphQL

Once you create or import a GraphQL schema as described above, you can enable autocompletion within the **GraphQL** query editor.

1. Under the **Collections** tab, return to your **GraphQL** body. Select your schema from the dropdown list. You may need to refresh by clicking on the adjacent icon.
[![schema selection](https://i.imgur.com/bhesWgs.png)](https://i.imgur.com/bhesWgs.png)
1. Begin editing your query, and now Postman will suggest autocomplete options from the data within your GraphQL schema.
[![autocomplete](https://i.imgur.com/Ai5cW4q.png)](https://i.imgur.com/Ai5cW4q.png)
