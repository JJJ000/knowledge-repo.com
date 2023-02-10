---
title: In graphql, what do "edges" and "node" represent?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Edges represent the relationships between nodes, which are the individual data points in the JSON structure.
---

**Contents**

[TOC]

#### Edges

Edges are the connections between two nodes in a graph. They are used to represent relationships between objects. Edges can have properties associated with them, such as weight or direction, and can be used to represent the strength of a relationship between two objects.

#### Nodes

Nodes are the objects in a graph. In a GraphQL JSON response, nodes are the individual records that are returned from a query. Each node has a unique identifier and can contain properties that provide additional information about the record. Nodes can also have edges connecting them to other nodes, which allows for the representation of relationships between records.
