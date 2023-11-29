+++
title = "Integration Testing"

sort_by = "weight"
weight = 3
+++

# Test Plan

VT Scheduler's components will be integration tested in three phases. VT Scheduler can best be described as a three-layer architecture, and each phase roughly aligns with ensuring that the given layer integrates with the layer below it. Each phase of testing will utilize a bottom-up approach. The source documentation does not specify the deployment locations or platforms upon which MongoDB nor the backend run, so the integration tests will instead focus on the desired functionality and behaviors.

The first phase of integration testing is concerned with the MongoDB instance and the ability to create <abbr title="Object Relational Mapping" >ORM</abbr>-like system wherein Course objects can be read from and written to the database via backend logic. The ability to consistently and correctly move objects from the database into heap RAM and vice-versa is the foundation upon which the controllers and frontend are built. In the second phase, the controllers are integrated with the database via the ORM-like system. This build allows a partial end-to-end test wherein API endpoints can be used and the effects of each call can be measured. Further, a first performance test of the system can occur at this point. Finally, the third phase incorporates both the student and administrator interfaces. This allows for a full end-to-end test which verifies that the web interface is correctly dispatching calls to the backend's API interface.

The decision to follow a bottom-up testing approach ultimately stems from the design of VT Scheduler. The application is primarily built a backend which is tightly integrated with a database. All of the system's functionality is implemented on the backend, and creating stubs for each controller or database connection if working from the frontend downward would be extremely time consuming. Instead, minimal stubs can be created which exercise the functionality provided by that layer and the layers below it.