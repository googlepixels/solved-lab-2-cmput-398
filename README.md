Download Link: https://assignmentchef.com/product/solved-lab-2-cmput-398
<br>
<h1>Objective</h1>

The purpose of this lab is to introduce you to the CUDA API by implementing vector addition. You will implement vector addition by writing the GPU kernel code as well as the associated host code.

All parts of this lab will be submitted as one zipped file through <a href="https://eclass.srv.ualberta.ca/portal/">eclass</a><a href="https://eclass.srv.ualberta.ca/portal/">.</a> Details for submission are at the end of the lab.

<h1>Instructions</h1>

Edit the code where the TODOs are specified and perform the following:

<ul>

 <li>Allocate device memory</li>

 <li>Copy host memory to device</li>

 <li>Initialize thread block and kernel grid dimensions</li>

 <li>Invoke CUDA kernel</li>

 <li>Copy results from device to host</li>

 <li>Free device memory</li>

 <li>Write the CUDA kernel</li>

</ul>




<h1>Local Setup Instructions</h1>

Steps:

<ol>

 <li>Download “Lab2.zip”.</li>

 <li>Unzip the file.</li>

 <li>Open the Visual Studios Solution in Visual Studios 2013.</li>

 <li>Build the project. Note the project has three configurations.

  <ol>

   <li>Test</li>

   <li>Debug</li>

   <li>Submission</li>

  </ol></li>

</ol>

For testing it is recommended that you run the “Debug” configuration.







But make sure you have the “Submission” configuration selected when you finally submit.

<ol start="5">

 <li>Run the program by pressing the following button:</li>

</ol>







Don’t try to run the program when the “Test” configuration is selected.

<h1>Vector Add Testing</h1>

<ol>

 <li>The “Debug” configuration will show “false” in the last line of the programs output If your code is incorrect.</li>

</ol>







The outputted vector can be seen in “DatasetVectorAddTest[0-9]”. For example, “DatasetVectorAddTest myOutput.raw”. The first line is the size of the array. The “Debug” configuration will run the first test “DatasetVectorAddTest ”.

<ol start="2">

 <li>You can also run the program from the Command Prompt (cmd).</li>

</ol>




VectorAdd -e &lt;expected.raw&gt; -i &lt;intput1.raw&gt;,&lt;input2.raw&gt; 

-o &lt;output.raw&gt; -t vector




Make sure you are in the directory with the executable before trying to run the command.

<ol start="3">

 <li>If you want to run all tests, then you can run the “Test” configuration. To do this simply build the program, with the “Test” configuration selected, and without running the debugger.</li>

</ol>




Build -&gt; Build Solution




In the Build Output window you should see the following:

<table width="198">

 <tbody>

  <tr>

   <td colspan="3" width="198">“Vector Add Testing Test 0…”</td>

  </tr>

  <tr>

   <td colspan="2" width="46">COMMAND</td>

   <td rowspan="2" width="152"> </td>

  </tr>

  <tr>

   <td width="26">Same</td>

   <td width="20"> </td>

  </tr>

  <tr>

   <td width="26"></td>

   <td width="20"></td>

   <td width="152"></td>

  </tr>

 </tbody>

</table>

Note that if the test fails you see “Different or error” instead of “Same”

<strong>Alternatively, you can just run the file “Test.bat” provided to you instead. </strong>

<h1>Using NSIGHT To Analyze Performance Instructions</h1>

This is complemented by the file “Guide on Debugging, Testing, Submitting and Profiling CUDA Project” on e-class, please read the file if you have not done so.

In Application Setting, enter:

<strong>Application</strong>: &lt;Pathtotheproject&gt;TestVectorAdd.exe

<strong>Arguments</strong>: -e output.raw -i input0.raw,input1.raw -o myOutput.raw -t vector

<strong>Working</strong> <strong>Directory</strong>: &lt;Pathtotheproject&gt;DatasetVectorAddTest&lt;Test Number&gt;




Then do the other steps like outlined in the guide file.

Submit an image called “cuda_summary.jpg” contain the screenshot of the CUDA Summary page that you get from running NSIGHT. For example:




<h1>Questions</h1>

Assume that the input vectors to your program has length N. <strong>Answers for the following questions</strong> <strong>must be based on N</strong>.

<ol>

 <li>How many floating operations are being performed in your vector add kernel? EXPLAIN.</li>

 <li>How many global memory reads are being performed by your vector add kernel? EXPLAIN.</li>

 <li>How many global memory writes are being performed by your vector add kernel? EXPLAIN.</li>

 <li>In the vector add project, how many bytes are transferred from the Host to the Device? EXPLAIN.</li>

 <li>In the vector add project, how many bytes are transferred from the Device to the Host? EXPLAIN.</li>

</ol>