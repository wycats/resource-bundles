# Application Development

This document outlines a soup-to-nuts workflow for application development. It provides a reference for how we expect tooling to interact with the proposals in this repository, in an effort to explain design decisions that we made in the core format and protocol.

> This document is not normative. While the core format and protocols are web specifications, this document provides a higher-level view of the kinds of workflows that we're hoping to enable in other contexts. Among other things, this document focuses on a workflow for developing applications that uses today's package registry, in an effort to explain how we intend things to work in the near term. The core format and protocol is intentionally agnostic to such details, and this document also explains how alternatives, such as the Skypack CDN, could be used instead.

A quick outline of the rest of this document follows.

- **Authoring Format**
- **Package Management**. How application developers will consume third-party packages from registries such as `npmjs.org` and `skypack`.
- **Bundling**. How an application and its dependencies will be converted into a resource bundle.
- **Transformations**. How general-purpose tools could transform resource bundles to apply production optimizations and other policies.
- **Deployment**. How resource bundles could be deployed to production, including CDNs.
- **Static Serving**. How resource bundles could automatically configure static file servers, and how they could be served.
- **Browser Consumption**. How resource bundles could be consumed by browsers without native support for resource bundles, and how custom tooling could interact with them in Service Workers.

## Authoring Format
