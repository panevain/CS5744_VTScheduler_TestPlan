+++
title = "Test Scope"

sort_by = "weight"
weight = 2
+++

[VT Scheduler](https://sites.google.com/vt.edu/vtscheduler/) is a web-based system which aims to simplify Virginia Tech's course planning and registration process for new and existing students. This website details the integration and validation testing necessary to ensure that VT Scheduler is able to fulfill its functional and non-functional requirements in addition to its ability to adhere to the design presented. 

We believe that there are three areas which warrant the most attention:
* The system must handle thousands of concurrent users during registration periods, so specific emphasis will be placed on testing the system's availability, latency and consistency under load. This will be verified at both the module and system levels.
* Students and administrators must use web interfaces to interact with VT Scheduler. Therefore, it is important to verify that the web interfaces are able to perform all of the operations outlined in the design document. To that end, this document will describe the validation testing which ensures that web interfaces behave as expected. 
* The design document describes an API which receives requests from clients using controllers on the back end. Integration tests will be described which ensure that controllers behave and interact correctly in support of the interface validation testing.