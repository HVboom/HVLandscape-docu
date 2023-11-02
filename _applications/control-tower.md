---
title: Control Tower
layout: article
show_title: false

modify_date: 02.11.2023
---

# HVControlTower

This application provides a central view of all _Applications_ belonging to the landscape.

- Dev environment (unstable): [hvcontroltower.dev.hvboom.org](https://hvcontroltower.dev.hvboom.org)
- Demo application: [hvcontroltower.demo.hvboom.org](https://hvcontroltower.demo.hvboom.org)
- Productive application: [hvcontroltower.hvboom.org](https://hvcontroltower.hvboom.org)

# Requirements

1. All applications must be registered
2. Each application need a dedicated and validated email address
3. The _HVControlTower_ provides an overview of all applications
   - regularly ping the registered applications to provide a state
     - `green`{:.success} if the pong is fast
     - `yellow`{:.warning} if the pong is slow
     - `red`{:.error} if the pong times out
4. The request to register a new _Application_ is achieved by sending an email to the _Control Tower Owners_
5. After _Mail_ and _URL_ validation a _Member_ having the necessary access rights (see [Entitlement](entitlement)) registers the application
   - it should be possible to support multiple versions of the same application
6. It is possible, that the _Owner_ of a registered application revoke the app
7. Provide detailed information of the registered app by calling the _Info_ service
8. Provide the possibility to open the registered apps in a new browser window
9. ...

# Changelog

| Version | Who                             | When       | Change          | Release       |
| ------- | ------------------------------- | ---------- | --------------- | ------------- |
| 1.0     | [Mario](mailto:Mario@HVboom.ch) | 29.10.2023 | Initial Version | November 2023 |
