Download Link: https://assignmentchef.com/product/solved-cse325-computer-project-9
<br>
<h1>Assignment Overview</h1>

<strong> </strong>

This assignment focuses on memory management within an operating system, and is the first milestone in a larger simulation.  You will design and implement the C/C++ program which is described below.




It is worth 20 points (2% of course grade) and must be completed no later than 11:59 PM on Thursday, 4/2.




<h1>Assignment Deliverables</h1>




The deliverables for this assignment are the following files:




<strong>proj09.makefile</strong> – the makefile which produces <strong>proj09</strong> <strong>proj09.student.c</strong> – the source code file for your solution




Be sure to use the specified file names and to submit your files for grading via the CSE Handin system before the project deadline.




<h1>Assignment Specifications</h1>




The program will simulate the steps to manage primary storage using paging.  The system to be simulated contains 1,048,576 bytes of RAM which is divided into 256 page frames.  Virtual addresses are 16 bits in length.




<ol>

 <li>Your program will accept command-line arguments to specify the file which contains the memory references (the “-refs” option), and to control the display of debugging information (the “-debug” option).</li>

</ol>




<ol start="2">

 <li>The “-refs” option will be followed by the name of the file which contains zero or more memory references. Each line of the file will contain the following information:</li>

</ol>




<ol>

 <li>virtual address being referenced (four hexadecimal digits, with leading zeroes)</li>

 <li>operation being performed (one character; ‘R’ for read and ‘W’ for write)</li>

</ol>




Items in the line will be separated by exactly one space, and the line will terminate with a newline.  For example:




<strong>3608 R </strong>

<strong>0e90 W </strong>

<strong>10d4 R </strong>




<ol start="3">

 <li>For each memory reference in the file, your program will display one line with the following information:</li>

</ol>




<ol>

 <li>virtual address being referenced (four hexadecimal digits, with leading zeroes)</li>

 <li>operation being performed (one character; ‘R’ for read and ‘W’ for write)</li>

 <li>page number (one hexadecimal digit)</li>

 <li>page offset (three hexadecimal digits, with leading zeroes)</li>

</ol>




Items in the line will be separated by exactly one space, and the line will terminate with a newline.  For example:




<strong>3608 R 3 608 </strong>

<strong>0e90 W 0 e90 </strong>

<strong>10d4 R 1 0d4 </strong>

<ol start="4">

 <li>After the simulation is completed, your program will display the contents of the page table. The display will contain one line for each page table entry:</li>

</ol>




<ol>

 <li>index of the page table entry (one hexadecimal digit)</li>

 <li>V bit (one character; ‘0’ for not valid, ‘1’ for valid)</li>

 <li>P bit (one character; ‘0’ for not present, ‘1’ for present)</li>

 <li>R bit (one character; ‘0’ for not referenced, ‘1’ for referenced)</li>

 <li>M bit (one character; ‘0’ for not modified, ‘1’ for modified)</li>

 <li>frame number stored in that page table entry (two hexadecimal digits, with leading zeroes)</li>

</ol>




Items within a line will be separated by exactly one space, and each line will terminate with a newline.  The page table display will begin and end with a blank line, and will include appropriate column headers.




<ol start="5">

 <li>After the simulation is completed, your program will display the following counts:</li>

</ol>




<ol>

 <li>total number of memory references</li>

 <li>total number of read operations</li>

 <li>total number of write operations</li>

</ol>




The summary information will be appropriately labeled and formatted.




<ol start="6">

 <li>If the “-debug” option has been selected, your program will display:</li>

</ol>




<ol>

 <li>the contents of the page table at the start of the simulation</li>

 <li>the contents of the page table after each memory reference is processed</li>

</ol>




<ol start="7">

 <li>The program will include appropriate error-handling.</li>

</ol>




<h1>Assignment Notes</h1>




<ol>

 <li>As stated above, your source code file will be named “proj09.student.c”; that source code file may contain C or C++ statements.</li>

</ol>




<ol start="2">

 <li>You must use “g++” to translate your source code file in the CSE Linux environment.</li>

</ol>




<ol start="3">

 <li>Valid executions of the program might appear as follows:</li>

</ol>




<strong>proj09 -refs test1 -debug proj09 –debug –refs test2 proj09 –refs test3 </strong>




<ol start="4">

 <li>Your program must create a data structure representing the page table and set all of the entries to zero at the start of the simulation.</li>

</ol>




For this assignment, your program will not update the page table.  Therefore, all entries in the page table should be zero in every page table display.  In subsequent assignments, your program will actively manage the page table (and thus the page table display will change over time).


