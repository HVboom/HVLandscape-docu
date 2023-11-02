---
title: Authentication
layout: article
show_title: false

modify_date: 02.11.2023
---

# HVMembership

This application provides a central authentication of _Members_.

- Dev environment (unstable): [hvmembership.dev.hvboom.org](https://hvmembership.dev.hvboom.org)
- Demo application: [hvmembership.demo.hvboom.org](https://hvmembership.demo.hvboom.org)
- Productive application: [hvmembership.hvboom.org](https://hvmembership.hvboom.org)

# Requirements

1. All application users must have a registered account
   - the _Members_ are identified by a validated email address
   - each _Member_ can choose their own nickname
1. Only the _Owners_ of the _HVMembership_ application can create a new account
   - the request to create a new membership is achieved by sending an email to the _Owners_
1. Provide necessary login, logout or password change forms as web components via public service calls
1. ...

# Changelog

| Version | Who                             | When       | Change          | Release       |
| ------- | ------------------------------- | ---------- | --------------- | ------------- |
| 1.0     | [Mario](mailto:Mario@HVboom.ch) | 29.10.2023 | Initial Version | November 2023 |
