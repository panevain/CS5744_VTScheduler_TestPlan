+++
title = "Integration Testing"

sort_by = "weight"
weight = 3
+++

Plan for integration builds

Devise and present a series of integration phases and corresponding partial system builds for incrementally testing identifiable pieces of the system. You need to present the phases, describe what portions of the system each one contains, and then give a brief argument for why this is the best way to carry out the integration testing for the design you have chosen. For projects of the size pursued in this class, a handful (3-5) phases may be appropriate, but you are welcome to divide phases into subphases if that seems necessary for the project you have chosen.

Focus is placed on the design and construction of the software.

Likely bottom up:
* Reduce the number of stubs/drivers needed to simulate supermodules
* The VTScheduler design is built entirely on the connection to the DB and subsequent Course objects
* Can sidestep generating data for UI/controllers if the DB connection already is tested
* Easier to 

Weaknesses:
* No good way to have an early prototype
* Have to plan ahead what the next module will need, and thus what should be tested

Describe 3 phases:
* DB <-> ORM-like Objects
* DB/ORM-like <-> Controllers
* Controllers <-> Web UI


VT Scheduler can best be described as a three-layer architecture 