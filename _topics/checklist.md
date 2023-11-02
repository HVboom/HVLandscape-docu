---
title: Checklist new Applications
layout: article
show_title: true

modify_date: 02.11.2023
---

Copy this checklist to the documentation of each newly created _[Rails]_ application.

Some specific bullet points allow the smooth integration into the _[HVboom Application Landscape][Home]_.

# Setup

- [ ] Define a name for the application: <mark>XYZ</mark>
- [ ] Create a dedicated mail address for the application - in my case via _[CPanel]_
- [ ] Create the _Development_ & _Demo_ directories
- [ ] Create the dedicated _[User][Production]_ for the application to run the productive version in an isolated environment
- [ ] Retrieve certificates for the new application via _[Let's Encrypt]_
  - [ ] Adjust the non-secure _[Apache]_ include section to serve the newly created application directories
- [ ] Define the necessary _[Apache]_ include sections, that the _[Rails]_ application can be served via _[Phusion Passenger]_
- [ ] Create an empty _[GitHub]_ repository for the new application with a _Readme_ file only, which points to the application documentation
- [ ] Clone that repository into the _Development_ directory
- [ ] Create a new branch to start the creation of the new _[Rails]_ application (see _Branching Model_)
- [ ] ...

# Application creation

- [ ] Create the [new Rails application][Rails Application] (refer to [script][Rails Application Script])
- [ ] Apply following templates to jump start the development process
  - [ ] Adjust the _Gemfile_
    - [ ] Remove _Puma_ dependency, because we use _[Apache]_ and _[Phusion Passenger]_ to run our _Rails_ applications
    - [ ] Setup _RSpec_ & _Cucumber_ test environment
    - [ ] ...
  - [ ] Setup the _Demo_ environment
  - [ ] Define a _Credential_ template file
  - [ ] Ensure the usage of _UUIDs_ as primary DB keys
  - [ ] Create useful _Dot_ files
  - [ ] ...
- [ ] Setup the [Rails Credentials]
- [ ] Create the [PostgreSQL] database
- [ ] Start the browser to check the successful startup of the new application: https://<mark>XYZ</mark>.dev.hvboom.org
- [ ] Commit everything and push it to _[GitHub]_
  - [ ] Merge the branch to the _Main_ stream
- [ ] Switch to the _Demo_ directory
- [ ] Checkout the repository and [update the application][Rails Application Update]
- [ ] Start the browser to check the successful startup of the new application: https://<mark>XYZ</mark>.demo.hvboom.org

---

[Apache]: https://github.com/HVboom/HowTo-DigitalOcean/wiki/Apache
[CPanel]: https://cpanel.hvboom.ch
[GitHub]: https://github.com
[Home]: https://hvlandscape.hvboom.org
[Let's Encrypt]: https://github.com/HVboom/HowTo-DigitalOcean/wiki/HTTPS-via-Let's-Encrypt
[Phusion Passenger]: https://github.com/HVboom/HowTo-DigitalOcean/wiki/Phusion-Passenger
[PostgreSQL]: https://github.com/HVboom/HowTo-DigitalOcean/wiki/PostgreSQL
[Production]: https://github.com/HVboom/HowTo-DigitalOcean/wiki/Productive-Rails-application
[Rails]: https://rubyonrails.org
[Rails Application]: https://github.com/HVboom/HowTo-DigitalOcean/wiki/New-Rails-Application
[Rails Application Script]: https://github.com/HVboom/HowTo-DigitalOcean/wiki/Utilities#create-new-rails-application
[Rails Application Update]: https://github.com/HVboom/HowTo-DigitalOcean/wiki/Productive-Rails-application#update-application
[Rails Credentials]: https://blog.eq8.eu/til/rails-52-credentials-tricks.html
