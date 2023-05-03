Download Link: https://assignmentchef.com/product/solved-cs372-project-1
<br>
<strong><u>Objectives:</u> </strong>

<ol>

 <li>Implement a client-server network application</li>

 <li>Learn to use the <em>sockets</em> API</li>

 <li>Use the <em>TCP</em> protocol</li>

 <li>Refresh programming skills</li>

</ol>




<strong><u>The Program:</u></strong>

Design and implement a simple chat system that works for one pair of users, i.e., create two programs: a chat server and a chat client.  The final version of your programs must accomplish the following tasks:

<ol>

 <li><em>chatserve</em> starts on host A.</li>

 <li><em>chatserve</em> on host A waits on a port (specified by command-line) for a client request.</li>

 <li><em>chatclient</em> starts on host B, specifying host A’s hostname and port number on the command line.</li>

 <li><em>chatclient</em> on host B gets the user’s “handle” by initial query (a one-word name, up to 10 characters). <em>chatclient</em> will display this handle as a prompt on host B, and will prepend it to all messages sent to host A.  g.,  “ <strong>SteveO&gt; Hi!!”</strong></li>

 <li><em>chatclient</em> on host B sends an initial message to <em>chatserve</em> on host A : PORTNUM. This causes a connection to be established between Host A and Host B.  Host A and host B are now peers, and may alternate sending and receiving messages.  Responses from host A should have host A’s “handle” prepended.</li>

 <li>Host A responds to Host B, or closes the connection with the command “quit”</li>

 <li>Host B responds to Host A, or closes the connection with the command “quit”</li>

 <li>If the connection is not closed, repeat from 6.</li>

 <li>If the connection is closed, <em>chatserve</em> repeats from 2 (until a SIGINT is received).</li>

</ol>




<strong><u>Requirements:</u></strong>

<ul>

 <li><em>chatserve </em>must be implemented in Java or Python</li>

 <li><em>chatclient </em>must be implemented in C/C++.</li>

 <li>Of course, your program <strong><u>must be well-modularized and well-documented</u></strong>.</li>

 <li>Your programs must run on an OSU <em>flip</em> server (for example: flip1.engr.oregonstate.edu). Specify your testing machine in the program documentation.</li>

 <li>Your programs should be able to send messages of up to 500 characters.</li>

 <li>Use the directories in which the programs are running. Don’t hard-code any directories, since they might be inaccessible to the graders.</li>

 <li>Be sure to cite any references, and credit any collaborators.</li>

 <li>Provide a README.txt with <strong><u>detailed</u></strong> instructions on how to compile, execute, and control your program.</li>

 <li>Combine all program files into one *.zip archive (no .7z or .gz allowed). The .zip file should not contain any folders – only files!</li>

</ul>

page 1 of 2




<strong><u>Notes:</u></strong>

<ul>

 <li>For your <em>C</em> implementation<em>,</em> read <em>Beej’s Guide</em>. It has everything you need for this assignment.  You will probably learn the most about socket programming by using C.</li>

 <li>If you are using <em>Python</em>, check <a href="https://docs.python.org/release/2.6.5/library/internet.html">http://docs.python.org/release/2.6.5/library/internet.html</a><a href="https://docs.python.org/release/2.6.5/library/internet.html">,</a></li>

 <li>If you are using <em>Java</em>, check <a href="https://docs.oracle.com/javase/tutorial/networking/sockets/index.html">http://docs.oracle.com/javase/tutorial/networking/sockets/index.html</a><a href="https://docs.oracle.com/javase/tutorial/networking/sockets/index.html">.</a></li>

 <li>It’s OK to hard-code host A’s handle.</li>

 <li>It’s OK to implement this system so that it requires the two users to take turns sending messages, i.e., when a user sends a message, s/he must wait for a response before sending the next message.</li>

 <li>When debugging, don’t use the well-known port numbers, because these will already be in use. I’d suggest using 30020 or 30021, though other students may be using these when you’re on the servers.</li>

 <li>If you use additional include-files or make-files, be sure to include them in your .zip file.</li>

 <li>You can test these programs using just one computer. Start the server, then start the client in a new window.  You can then switch back and forth between the two terminal windows.</li>

 <li>Project #1 will be accepted up to one week late with a penalty of up to 10% per day.</li>

</ul>

<strong> </strong>

<strong><u>Extras:</u></strong>

<ul>

 <li>If you implement extra credit features, be sure to describe those features in your program documentation and README.txt or you will not receive any credit.</li>

 <li>There are many possibilities for extra credit. Be sure that your program satisfies the requirements first, and then do the extra credit in separate files.</li>

 <li>Extra credit possibilities include (but are not limited to) … Set up your programs so that either host can make first contact.

  <ul>

   <li>Make it possible for either host to send at any time (while the connection is active) without “taking turns”.</li>

   <li>Make your server multi-threaded.</li>

   <li>Split the screen to show host B’s typing in one panel, and host A’s responses in the other panel.</li>

   <li>Make the characters appear on the receiving host as they are being typed on the sending host (instead of waiting for the entire line to be sent).</li>

  </ul></li>

</ul>