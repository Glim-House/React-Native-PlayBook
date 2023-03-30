---
sidebar_position: 1
---

# Manual Testing

## General Testing process

Smoke testing, also called build verification testing or confidence testing, is a software testing method that is used to determine if all critical functionalities of a software are working fine.

## How to do Smoke testing?

- Create the smoke test either using manual or automated processes.
  If the process followed is Manual testing then the tester should prepare test cases which include all important scenarios for a stable system/application which should cover all the critical functionalities for smoke testing .
  Tester should keep a record of the test cases passed or failed to determine whether the system/application is stable
  If the process followed is Automation testing then the tester should prepare test suites which include code to cover all important scenarios which should test all the critical functionalities .
  Tester should generate a report of the scenarios/suites passed/failed to determine whether the system/application is stable
- Analyze smoke test results. If the software fails, it's returned to the development team for more testing. If the build is stable,the tester can do the sanity testing.
- Sanity testing is to make sure that the proposed modifications or new functionality works as intended.
- Prepare test cases for the newly added functionality/scenario and if necessary add them to the smoke testing test case folder
- Once the newly added functionality is integrated with the stable build/system,the tester has to do regression testing,
- Regression testing is a software testing practice that ensures an application still functions as expected after any code changes, updates, or improvements. Regression testing is responsible for the overall stability and functionality of the existing features.
- If the process followed is Manual testing then the tester should prepare test cases which include happy paths of all important scenarios for a stable system/application which should cover all the critical functionalities for regression testing .
- Testers should keep a record of the test cases passed or failed to determine whether all the existing functionalities before integrating new functionalities are working fine.
  If the process followed is Automation testing then the tester should prepare test suites which include code to cover happy paths of all important scenarios which should test all the critical functionalities .
  Tester should generate a report of the scenarios/suites passed/failed to determine whether all the existing functionalities before integrating new functionalities are working fine
- If there are defects after regression testing,tickets are created or re-opened if they are already existing bugs.They are sent to the developer and the tester has to do Retesting once the tester is provided a new application with all the bugs/defects fixed.
