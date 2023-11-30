+++
title = "Phase 2"

sort_by = "weight"
weight = 2
+++

Phase 2 of integration testing will be adding in the backend functionality to the toolies and database system that has already been constructed. The tests for this phase will be focused on ensuring that the current system interacts with the backend correctly, that the API methods that connect the backend, toolies, and database function correctly, and that the system handles concurrent actions correctly.


| Test Case ID | Test Objective                                                                       | Test Description                                             | Expected Results                                                                                                                                    |
|--------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| I2.1a        | Check the interface link between the enrollCourse API and the database               | Send Post request with student, coruse, and forceAdd: false. | Response 200 (Request was successful) and course has been successfully added to the corresponding student's course list.                            |
| I2.1b        | Check the interface link between the enrollCourse with forceAdd API and the database | Send Post request with student, course, and forceAdd: true.  | Response 200 (Request was successful) and course has been successfully added to the corresponding student's course list.                            |
| I2.2         | Check the interface link between the unenrollCourse API and the database             | Send Post request with student and CRN.                      | Response 200 (Request was successful) and course with corresponding CRN has been successfully removed from the corresponding student's course list. |
| I2.3a        | Check the interface link between the searchCourse by CRN API and the database        | Send Post request with CRN.                                  | Response 200 (Request was successful) and a JSON object containing all courses with that CRN is returned.                                           |
| I2.3b        | Check the interface link between the searchCourse by subject API and the database    | Send Post request with subject.                              | Response 200 (Request was successful) and a JSON object containing all courses with that subject is returned.                                       |
| I2.3c        | Check the interface link between the searchCourse by timeslot API and the database   | Send Post request with timeslot.                             | Response 200 (Request was successful) and a JSON object containing all courses with that timeslot is returned.                                      |
| I2.4         | Check the interface link between the viewCourses API and the database                | Send Post request with student                               | Response 200 (Request was successful) and student's course list has been returned as a JSON.                                                        |
| I2.5         | Check the interface link between the addCourse API and the database                  | Send Post request with newCourse                             | Response 200 (Request was successful) and newCourse record has been created in the database.                                                        |
| I2.6         | Check the interface link between the deleteCourse API and the database               | Send Post request with CRN                                   | Response 200 (Request was successful) and course record with corresponding CRN has been removed from the database.                                  |