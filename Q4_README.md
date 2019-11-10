# JGU WEKA Rest Service

The following is a summary of the commands that must be executed to run load tests on Weka REST.

## Prerequisites
- JGU weka is deployed. (See Q2_README.md for more information)
- JMeter is installed

## Runnig JMeter
```
- Browse the JMeter application folder inside the / bin folder.
- Run the script "jmeter" and the application will open
```

### JMeter
- Open the test plan via File-> Open
- Click on the "Test Users" tab
  - It is then possible to adjust the number of users (Number of threads), the period of creation (Ramp-Up Period) and the number of iterations (loop count).
- Under "Recording Controller", it is possible to see the 5 requests / tests executed by iteration by user.
- Still under "Test Users", it is possible to see the results of the tests in "View Results Tree"
- To run the tests, Run-> Start

- To know the input parameters of each test case, please refer to the report submitted in this work.
