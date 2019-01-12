# A website for online exam

- All codes are available on https://github.com/I-mm/OnlineExam

- Meanwhile, it is also deployed on a server provided by [Aliyun](https://cn.aliyun.com/), and you can access this system on http://www.youhear.me:8080/ (Or directly IP address: http://39.105.165.114:8080/). *(**Note:** The server will expire at the end of Jan, 2019, and the domain name provided in the GitHub Student Developer Pack will also expire at Mar, 2019, so it may be not available after that time.)*

- The time limit of each exam has been set to 10 seconds to show the re-exam logic of this system. 

  <br>

## Configuration

- Server: 1 Intel(R) Xeon(R) CPU E5-2682 v4 @ 2.50GHz, RAM 2GB, Ubuntu 16.04
- Container: Apache Tomcat 9.0.13
- Database: MySQL Ver 14.14 Distrib 5.7.24, for Linux (x86_64) using  EditLine wrapper

<br>

## Overview

This website TMP (Test Make Perfect) is an online English testing platform. Users can log in and register before conducting online English testing. Before the test, users can set the pass line to gratify their personal needs. During the test, the website will randomly call up a series of questions from the database, and timing the answering process. The website has the corresponding re-exam mechanism and the corresponding score algorithm for the time-out behaviour of the first test. After finishing the test, the website will generate the user's scores, answer time, correct answers and so on. Users can also go back to the home page to see the results report.

<br/>

## Function implementation

1. **Question Library**

   The question library contains 25 questions and the correct answers based.

   ![Figure1](Figures/Figure1.png)



   ![Figure0](Figures/Figure0.png)

<br>

2. **Exam generation**

   Five questions and the corresponding choices are selected randomly from the question library. 

![Figure2](Figures/Figure2.png)

<br>

3. **Setting of the score threshold**

   Before starting the exam, the user can set the score threshold as his wishes by clicking the element, whose default value is 60.
   

![Figure3](Figures/Figure3.png)

<br>

4. **Logic of the first attempt**

   In the course of an exam, five questions are selected randomly to generate the test page and the exam is limited within fixed minutes. After finishing the exam on time, the score will be calculated automatically.
   

![Figure4](Figures/Figure4.png)

<br>

5. **Re-exam logic** 

   If the participator doesn't submit the exam within the timeframe, a re-exam can be taken with the same timeframe and same score threshold. The final score is generated as the average of the two scores. *(**Note:** The time limit of each exam has been set to 10 seconds to show the re-exam logic of this system. )*

![Figure5](Figures/Figure5.png)

<br>

6. **Exam report**

   After the exam, two reports are generated for the whole exam (including re-exam activities). One for the statistical analysis, another focuses on the detailed analysis report for each question and corresponding answer.

![Figure6](Figures/Figure6.png)

<br>

7.  **Previous report**

   Users can also view their previous exam reports by clicking the `My Previous Exam Report` button at `home_page.jsp`, then a table of previous reports will be generated as shown below. 

![Figure7](Figures/Figure7.png)

<br>

## User Interface

1. **Login**

   This is the first page of TMP. In this page, users can enter the username and password to login. If he/she doesn’t have an account, a button named ‘Create an account’ can be clicked and the page will jump to another one to complete register.
   

![Figure7](Figures/Figure8.png)

<br>

2. **Register**

   In this page, users need to enter the corresponding information and agree to our terms and policy to finish register. After that, users can go back to the last page to login.

![Figure9](Figures/Figure9.png)

<br>

3. **Home page**

   When users enter the home page of TMP, they can see the following page which contains the user’s personal information, the start-test button, the watch-report button and the other blocks in our website.

![Figure10](Figures/Figure10.png)

<br>

4. **Set the score threshold**

   After clicking the `Start a New Exam` button, users can see a modal box where the pass line can be set by clicking the round. 


![Figure11](Figures/Figure11.png)

<br>

5. **Exam page**

   When user starts an exam, the backend will select the questions randomly from the database and generate the test page. Users are required to complete the test within the specified time. If the user fails to complete the first test within the specified time, another chance will be given. 
   
     

![Figure12](Figures/Figure12.png)

<br>

6. **Exam report page**

   In this page, users can see the mark, the exam time and so on. Following the summary, users can see the user's answer and the correct answer.
   

![Figure13](Figures/Figure13.png)

<br>

7. **Previous report page**

   Users can view their previous report by clicking the `My Previous Exam Report` button. In this page, users can see some information and statistics from previous exams.


![Figure14](Figures/Figure14.png)

<br>

## Group Member

赵屹铭，赵春宇，井长源，张丙驰，夏昕