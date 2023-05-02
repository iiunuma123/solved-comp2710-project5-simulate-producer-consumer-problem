Download Link: https://assignmentchef.com/product/solved-comp2710-project5-simulate-producer-consumer-problem
<br>



<ol>

 <li>Complete the source code to simulate producer/consumer problem.</li>

 <li>Understand the basics of the POSIX thread library.</li>

 <li>Build a binary program on a Linux machine.</li>

 <li>Run the program and record the result of the simulation.</li>

</ol>

<strong>Requirements<em>: </em></strong>

<ul>

 <li>Each student should <strong>independently</strong> accomplish this project assignment. You may discuss with other students to solve the coding problems.</li>

 <li>Important! Read and follow the I/O format specification carefully. We are using an autograde script to grade this project. It is very important for your final grade of this project! Any submission violating the format may not be correctly recognized.</li>

 <li>You are highly recommended to use a Linux operating system, because “pthread.h” is a header for the Unix/Linux (POSIX) API for threads.</li>

</ul>

<ol>

 <li><strong> Introduction to producer and consumer model </strong></li>

</ol>

The producer and consumer model is to schedule how concurrent processes and threads access the resources. It contains:

<ol>

 <li><strong>Producer</strong>: One or multiple processes/threads that produce data or release hardware resource.</li>

 <li><strong>Consumer</strong>: The one process/thread that takes in data or uses hardware resource to do computations.</li>

</ol>

A producer could also be relatively a consumer to the output of another producer and vice versa.

<ol start="3">

 <li><strong>Buffer</strong>: The destination to store the output from producers or resources and later accessed by another consumer.</li>

</ol>

<strong>Other concepts involved in our project</strong>:

<ol start="4">

 <li><strong>POSIX thread</strong>: Threads mechanism that satisfy POSIX standard (most operating system).</li>

 <li><strong>Mutex</strong>: A “lock” that guarantee that only one person has the access.</li>

</ol>

In this project we use POSIX threads. The “pthread” is a POSIX thread library written in C++ and provides the basic functions.

To simplify our simulation, we assume there are only 2 POSIX threads. One is the consumer, the other is the producer. The producer generates 1 unit data each time to the buffer, and the consumer takes 1 unit data from the buffer each time. The size of the buffer is 1. One unit data is just one integer. The producer generates integers 7, 14, 21 …. into the buffer and consumer read them out from the buffer.

<ol start="2">

 <li><strong> Follow the Format Specification </strong></li>

</ol>

In the source file “<strong>project5_LastName_UserID.cpp</strong>“, you will find first four comment lines:

<strong>// #0#BEGIN# DO NOT MODIFY THIS COMMENT LINE! </strong>

<strong>// </strong>Firstname

<strong>// </strong>Lastname

<strong>// #0#END# DO NOT MODIFY THIS COMMENT LINE! </strong>

Your first task is modifying the two lines <strong>between</strong> the beginning line and end line. Change them into your first name and last name. Remember the strings are case-sensitive, so capitalize the first letter of the word and follow exactly the syntax of the example.

You can see lots of similar code blocks in the file. You are supposed to fill your answer between those special beginning and ending comment lines. You can insert and edit multiple lines between special comment lines in anyways, however (Important!), as the comment indicated, do not modify the special begin and comment lines <strong>themselves</strong>!

Let’s do the second task. Scroll down to the bottom of the file and find those lines (press “shift + g” if you are using vi/vim):

<strong>// #8#BEGIN# DO NOT MODIFY THIS COMMENT LINE! </strong>int banner_id = 0<strong>; </strong>

<strong>// #8#END# DO NOT MODIFY THIS COMMENT LINE!</strong>

Look at your student ID card, check your banner ID. Again, change <strong>ZERO</strong> to <strong>your own ID</strong>. Your unique student id will be compiled into the program, and the input of the experiment also uniquely depends on your ID.

Warning: Since every student has a unique id number, the later compiled binary file is also unique. Copy binary file from other students will be easily detected!

<ol start="3">

 <li><strong>Complete Source Code </strong></li>

</ol>

Read the source code and the rest comments, try to understand the function of each line of code, the basic usage of “<strong>pthread</strong>” library function and semaphore from the example code of producer and from the main function.

Follow the instructions in the comments and insert proper code into the rest 7 blocks to implement a producer/consumer model.

<ol start="4">

 <li><strong>Run and Record Simulation Result (10 Points)</strong></li>

</ol>

Your correct file name should be: <strong>project5_LastName_UserID.cpp </strong>

For example, project5_Liu_tzl0031.cpp. <strong>Please remember to change the lastname and userID to your own ones before you continue the following steps</strong>.

Compile your source code into a binary program. For example, use following command to include the pthread library:

<strong>$ g++ project5_Lastname_UserID.cpp -o project5_LastName_UserID -lpthread </strong>

After you compile the C++ source code successfully, please use the script command to record the running result of the program Firstname_Lastname:

<strong>$ script project5_LastName_UserID.script </strong>

Script started, file is project5_LastName_UserID.script

./project5_LastName_UserID

After you run the program, you will have the following results:

Banner id: 90…….

producer produce item 7 consumer consume item 7 producer produce item 14 consumer consume item 14 producer produce item 21 consumer consume item 21 producer produce item 28 consumer consume item 28 producer produce item 35 consumer consume item 35 producer produce item 42

consumer consume item 42

…<strong>  </strong>

You should have the same result except the different in the banner ID. Then exit recording and save it into typescript file “<strong>project5_LastName_UserID.script</strong>” by the following command:

<strong>$ exit  </strong>

<strong>exit Script done, file is project5_LastName_UserID.script </strong>

Warning: Since every student has a unique id number, the result of the simulation is also unique. Copy simulation results from other students will be easily detected!

<ol start="5">

 <li><strong> Deliverables</strong></li>

</ol>

Since you have generated multiple script files, please save all the script files in one directory. Make sure all the three files are into this folder. You should have those following files inside the folder:

<ol>

 <li>Commands recording file: <strong>script</strong></li>

 <li>Executable binary file: <strong>project5_LastName_UserID</strong></li>

 <li>Source code file: <strong>cpp</strong></li>

</ol>

Change the folder name to “<strong>project5_LastName_UserID</strong>“. Please make sure the <strong>folder name</strong> is in a correct form. You can use the command <strong>mv</strong> to rename the folder: <strong>$ mv your-current-folder-name project5_LastName_UserID</strong>

Achieve all the folder into a single tarred and compressed file with a tar command.

<strong>tar -zcvf project5_LastName_UserID.tar.gz project5_LastName_UserID </strong>

You need to submit one tarred file with a format <strong>project5_LastName_UserID.tar.gz</strong> through Canvas.