# About the Assignment
This is the Assignment on Performance test using JMeter where
**Task1** is for performance test with the JMeter collection (booking.jmx) and
**Task2** is with D-money which is a transactional system where deposit money,send money and make payment transactions were performed.

# Technology used:
- postman
- JMeter
- GIT

# How to run?
- Clone this project
- Run the .jmx collection file in JMeter for Task1 and Task2 separately
- Give following command for testing through cmd:
- ``` jmeter -n -t yourFile.jmx -l yourFile.jtl ```
- Generate Report by ``` jmeter -n -t yourFile.jmx -l yourFile.jtl -e -o yourFolder ```

# Test Details:
**Task1** a. For Load Test please follow below for creating own collection:
Pre-condition:
User with time period should be known.
Test Steps:
1. To limit the load and saving time breakdown the total time into "minute" and "second" values.
2. Calculate the Expected TPS according to the formula User/Time given.
3. Input the user count and calculated time in thread group section in JMeter and save it.
4. From the .jmx file location run the test from cmd and save the test report by the command mentioned in "How to run?".
5. Take the throughput result from the report and input in the excel column as "Actual TPS".
6. Take the error percentage from the report and input in the excel column.
7. Start the test with Average user count with calculated expected time in seconds and continue the test until there is 0 errors to get the Load Test Final Result as **Pass**.
   b. For Stress Test please follow below:
Pre-condition:
a. Load Testing for the given condition must be completed.
b. After completing the load test the time with users count should be taken for Stress Testing.
c. For this assignment Load Test Passed in 60 seconds with 166 users, hence stress testing will be started by increasing the user count from this level.
Test Steps:
1. Input the user count as 500 and  time as 60 seconds in thread group section in JMeter and save it.
2. Calculate the Expected TPS according to the formula User/Time given.
3. From the .jmx file location run the test from cmd and save the test report by the command "JMeter -n -t [jmx file] -l [results file] -e -o [Path to web report folder]".
4. Take the throughput result from the report and input in the excel column as "Actual TPS".
5. Take the error percentage from the report and input in the excel column.
6. Also calculate the deviation.
7. Start the test with the time and user count where load test get Passed and increase the load continuously at least for 4 iterations.
8. Then Give the system and server a break as the it was continuously ping with increased load and also to check if there is any change in improved deviation.
9. Continue increase the Load as user count, until error appears.
10. Repeat step-9 again and for next 2-3 iterations decrease the load.
11. Note all the observation to check at which Load and deviation server is getting error and to finalize the stress point and mark that as RED.
    
**Task2** a. Create separate thread groups under one test plan to cover the scenarios for:
○ 5 agents perform deposits for 10 customers.
○ 5 customers send money to another 10 customers.
○ 5 customers make payments to 2 merchants.
          b. Create separate thread group for user creation for different roles.
          c. Please make sure of the Agents are already deposited with enough money from the SYSTEM.
          d. Use small amounts for Send Money and Make Payment, so that balance can't become empty.
          e. From the .jmx file location run the test from cmd and save the test report by the command "JMeter -n -t [jmx file] -l [results file] -e -o [Path to web report folder]" for each thread group according to the needs.

# Test Reports:
# Task1: **Load Test Images** 
![LoadTest5](https://github.com/user-attachments/assets/c3573874-4563-4bc6-addc-d544bb4a1204)
![LoadTest4](https://github.com/user-attachments/assets/3d7fe8ae-87e5-4caa-aea5-7f6c0a145c82)
![LoadTest3](https://github.com/user-attachments/assets/12283b1a-5a65-4fa4-87b6-affae1cdf487)
![LoadTest2](https://github.com/user-attachments/assets/3777645e-1247-4253-a2ba-a120647f5da4)
![LoadTest1](https://github.com/user-attachments/assets/4d90fbab-f973-41d7-908e-26347c9702c7)

**Stress Test Images**
![StressTest12](https://github.com/user-attachments/assets/6e227927-9416-4ee4-a64b-ad9b178ba9fe)
![StressTest11](https://github.com/user-attachments/assets/39ec3fac-92c9-4ffa-8897-17e96a16cdf2)
![StressTest10](https://github.com/user-attachments/assets/60841113-fb79-4449-8dda-07df1f8aa9d7)
![StressTest9_FailCase](https://github.com/user-attachments/assets/6be9b473-68fe-4fca-980e-2a6c30cd6ae8)
![StressTest8_FailCase](https://github.com/user-attachments/assets/f4c4000e-841e-45ee-9698-229179195a09)
![StressTest7](https://github.com/user-attachments/assets/bccc000f-ea87-4100-ad3b-14ace1204bbe)
![StressTest6](https://github.com/user-attachments/assets/6b1efd63-73e0-41e2-a67b-50119a430d2b)
![StressTest5](https://github.com/user-attachments/assets/0751ef81-d066-4aab-9c35-dbe49dabf029)
![StressTest4](https://github.com/user-attachments/assets/6bcc37d0-af14-421a-b5b8-0f8a3dfabc29)
![StressTest3](https://github.com/user-attachments/assets/90cfd747-0158-4743-a4f2-4c93b5636be4)
![StressTest2](https://github.com/user-attachments/assets/7336ca83-1ab1-407e-9759-93051b8bd746)
![StressTest1](https://github.com/user-attachments/assets/722328ae-6b4a-4a9a-9e84-21e4ff8afefa)

Test Report with Test Steps for Task1: [Booking_TestReport_T1FRL.xlsx](https://github.com/user-attachments/files/18387049/Booking_TestReport_T1FRL.xlsx)


# Task2: **Generated HTML report**
![SendMoney](https://github.com/user-attachments/assets/d0ccc107-f22e-404f-ba82-06bab9774e80)
![MakePayment](https://github.com/user-attachments/assets/8493b8ea-624d-4268-b85d-e254cbdd1502)
![DepositMoney](https://github.com/user-attachments/assets/820d1721-d590-4baa-80fd-15ed9631fdac)
