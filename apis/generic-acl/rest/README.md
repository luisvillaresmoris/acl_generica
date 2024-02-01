# Purchase Categories

## 📜 Summary

This services tries to resolve de problem of translate categories from IOP to ITX.

## 🚀 Getting started

Understand the concepts and play around with the API in order to get the values that you need

## About

This should be able to allow the ACL services to change from ITX to IOP language and vice versa.

### Main Goal

This should be able to allow the ACL services to change from ITX to IOP language and vice versa.

### Context

Literally we are going to maintain a Database with the translations. this context only allows strings,
so you should check by the exact string that the legacy provides to you.

### Specifics

RestFull API to provide the data

## Usage

The authorization phase should be done in the BFF, so all our data is not authorize, if you request the data, you can reach any structure data.

There is no sensitive data in this service, it is all about hierarchies and categories, it contains the business language but not business data.

### Configuration

Just get the token to access the service and test it!

Once we deploy de service, we are not allow to configure Bots in the api gateway, so only nominal user are allow to reach the endpoints.

### Example

Given a list of Categories we provide the equivalent production filters:
request:

```json
["urn:BUYERSUBGROUP:25f91691-10fc-400a-9ce0-0d99416a4ecc", "urn:BUYERSUBGROUP:41e24c9a-515e-4064-8ffb-5558ee70d406"]
```

return:

```json
["article.brand: 1, article.section: 1, article.buyer: 5137, article.buyerGroup: 5116, article.buyerSubgroup: 17687", 
"article.brand: 1, article.section: 1, article.buyer: 5137, article.buyerGroup: 5116, article.buyerSubgroup: 17691"]
```

Given a list of Production filters we provide the equivalent categories:
request:

```json
["article.buyerSubgroup: 17687", "article.buyerSubgroup: 17691"]
```

return:

```json
["urn:BUYERSUBGROUP:25f91691-10fc-400a-9ce0-0d99416a4ecc", "urn:BUYERSUBGROUP:41e24c9a-515e-4064-8ffb-5558ee70d406"]
```

## 🧰 Support

Add a link to the support section in the product's documentation. If no documentation exists yet, make sure you specify how users can contact you/the team.

## Documentation

We do not have any more documentation of this process.
