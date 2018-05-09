# server
httpServer.js for questionapp and quizapp


Technical Report

In the Ubuntu window, type "git clone https://github.com/vvvicky210/server.git" to download the whole repository.The server can support both Question Setting App and Location-Based QUiz App. Type "node httpServer.js &" to process the server and then you can change directory to specific file and process "phonegap serve". After that, you can type "developer.cege.ucl.ac.uk:31272" in a browser to open the app. The function of the httpServer.js file is to connect the databse with the server. So both two apps can extract data from tables in the database or upload data to the database. 

The Quiz App is to run on an Android phone using PhoneGap. Users can scan QR code to download the app. The Question Setting App can be used in a browser. The description of each function in codes of two applications is in the report. And the functions of two applications are described in User Guide in each repository.

P.S. Create table in the database

Question Setting App/ create the table to store questions in the database
CREATE TABLE public.questionapp
(
  clientid character varying(100),
  questionid character varying(100),
  question character varying(100),
  answer1 character varying(100),
  answer2 character varying(100),
  answer3 character varying(100),
  answer4 character varying(100),
  answernumber character varying(100),
  geom geometry
)

Quiz App// create the table to store question id and user's answers in the database

CREATE TABLE public.quizapp
(
  questionid character varying(100),
  answernumber character varying(100)
)

