# @provides on interfaces: Apollo Gateway reproduction

Minimal reproduction for
[apollographql/apollo-server#2987](https://github.com/apollographql/apollo-server/issues/2987):
*"Gateway throws error for @provides-directive on interfaces and objects
implementing interfaces"*, reported by Dennis Dubbert on 4 July 2019 and closed
as completed by the Apollo team on 8 July 2019.

It came out of comparing schema stitching with the then brand-new Apollo
Federation (see
[GraphQL_Microservice_Research](https://github.com/ddubbert/GraphQL_Microservice_Research)).

| Folder | Role |
|---|---|
| `user_service/` | Federated service owning users |
| `product_service/` | Federated service owning products, uses `@provides` on an interface |
| `gateway/` | Apollo Gateway composing both services |

Run `npm install` and `npm start` in each folder, services first, then the
gateway.

> **Status:** reproduction from 2019, kept for reference and not maintained.
> Apollo Federation has changed substantially since.
