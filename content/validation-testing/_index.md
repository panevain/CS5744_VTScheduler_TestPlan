+++
title = "Validation Testing"

sort_by = "weight"
weight = 4
+++

## Validation Testing for VT Scheduler

In this section, we present a comprehensive validation testing plan for the VT Scheduler. Our approach is rooted in ensuring that the system not only meets its functional and non-functional requirements but also provides a seamless and efficient experience for all user groups, including students, faculty, and administrators.

### Overview

VT Scheduler is designed to handle a significant user load, particularly during peak registration periods, making performance under stress a critical aspect of our testing. The system's architecture, based on Abstract Data Types (ADT), prioritizes data concurrency, consistency, and low latency, essential for a smooth user experience.

### Test Scope

1. **User Interface Testing**: Ensuring that the interface is intuitive and aligns with the diverse needs of the VT community. This includes testing for accessibility, ease of navigation, and responsiveness.
2. **API Testing**: Verifying the RESTful API's functionality, focusing on the correctness of data exchange between the front-end and back-end systems. This will include testing various API endpoints for course enrollment, unenrollment, and course searching.
3. **Database Testing**: MongoDB, a NoSQL database, is at the core of VT Scheduler. Validation tests will include verifying data integrity, consistency, and security features such as authentication and encryption.
4. **Performance Testing**: Given the high volume of users, particularly during registration periods, we will conduct stress and load testing to ensure that the system maintains performance benchmarks.
5. **Security Testing**: Critical given the sensitive nature of student data. This involves validating authentication mechanisms, authorization checks, and data encryption protocols.

### Test Traceability Matrix

Our testing plan is aligned with both functional and non-functional requirements. The traceability matrix below links test cases to specific requirements.

| Test Case ID | FR/NFR Satisfied                       | Test Description                        | Expected Results                                                                  |
| ------------ | -------------------------------------- | --------------------------------------- | --------------------------------------------------------------------------------- |
| V1.1         | FR1, NFR9                              | User Role Verification                  | Correct data access based on user roles                                           |
| V1.2         | FR2, FR3, FR4, FR5, FR7, NFR5          | Selection and Search Criteria Tests     | Accurate course data based on user input                                          |
| V1.3         | NFR1, NFR2, NFR3, NFR7                 | Performance and Scalability Tests       | System maintains performance under heavy load                                     |
| V1.4         | FR6, FR8, FR10, FR11, FR12, NFR6, NFR7 | Data Manipulation and Consistency Tests | Correct update of course and student information                                  |
| V1.5         | NFR4, NFR8                             | Cross-Platform and Integration Testing  | Consistent user experience across platforms and integration with existing systems |

### Additional Test Cases for VT Scheduler

Building on the provided test scope, we propose the following additional validation test cases, ensuring a thorough and critical assessment of the VT Scheduler:

| Test Case ID | FR/NFR Satisfied    | Test Description                        | Expected Results                                                             |
| ------------ | ------------------- | --------------------------------------- | ---------------------------------------------------------------------------- |
| V2.1         | FR9, NFR2           | Registration and Login                  | Successful user authentication and access to system features                 |
| V2.2         | FR2, FR3, FR4, NFR1 | Course Availability and Enrollment      | Accurate display and functionality of course enrollment under high user load |
| V2.3         | NFR6, NFR9          | Data Privacy and Security               | Secure handling and storage of sensitive user data                           |
| V2.4         | FR5, NFR4           | Multi-campus Functionality              | Effective operation across different campuses and user interfaces            |
| V2.5         | FR10, FR12, NFR5    | User History and Preferences Management | Accurate tracking and reflection of user course history and preferences      |

### Conclusion

The validation tests for VT Scheduler are designed to rigorously assess every aspect of the system, from its user interface to its backend processes. By aligning our tests with the key design decisions and requirements, we aim to deliver a robust, efficient, and user-friendly system for the Virginia Tech community.
