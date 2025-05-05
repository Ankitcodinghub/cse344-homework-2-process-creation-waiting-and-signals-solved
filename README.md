# cse344-homework-2-process-creation-waiting-and-signals-solved
**TO GET THIS SOLUTION VISIT:** [CSE344 Homework 2-Process creation, waiting and signals Solved](https://www.ankitcodinghub.com/product/cse344-homework-2-process-creation-waiting-and-signals-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;94779&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSE344 Homework 2-Process creation, waiting and signals Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Process creation, waiting and signals

</div>
</div>
<div class="layoutArea">
<div class="column">
The objective is to have a process read an input file, interpret its contents as coordinates, and forward them for calculations to children processes. Then it will collect their outputs and make a final calculation.

Process P

Process P will read an ASCII file (denoted by inputfilepath) provided as a commandline argument. It will interpret every character in it as un unsigned byte. Consecutively read 3 bytes are interpreted as integer coordinates in a 3-dimensional space. Every i-th group of consecutive 10 coordinates it reads, are forwarded to a child process R_i. The child process R_i will be created by P using the fork+exec paradigm. The 10 coordinates will be passed to the child process as environment variables. Once P reaches the end of the file (or there are less than 10 coordinates left), P will collect the outputs of the calculations of its children processes. The outputs will take place in an output file (denoted by outputfilepath) and will be in the form of one matrix from each R_i. Then P will calculate the two matrices that are closest to each other with respect to the Frobenius norm, and print them on stdout and terminate.

<ul>
<li>The process P must not start collecting the outputs before all the children processes have finished their calculations.</li>
<li>The children processes must not access the output file simultaneously for writing. ./processP -i inputFilePath -o outputFilePath
Process R_i

Each process R_i will receive 10 3d integer coordinates as environment variables. The names of the variables are up to you. It will then calculate their covariance matrix and write it to the output file provided to P (the format is up to you). This means you need to pass the outputfilepath information to the child process from P, I recommend passing it as a commandline argument while creating R_i. Then R_i will terminate.
</li>
</ul>
• If P receives SIGINT, it will forward the signal to all of its children, free all of its resources, close open files, and remove the output file, clean-up after its children and terminate. When the children receive the forwarded signal, they will terminate after freeing their resources as well. Be careful with the signal handler, remember what I told you during the lectures. Use the polling based paradigm I showed you for graceful exiting.

Output

Process P reading hw2/inputFile.dat

Created R_1 with (66,77,81),(110,91,34),…,(63,90,91)

…

Created R_34 with (61,17,11),(210,51,54),…,(33,60,75)

Reached EOF, collecting outputs from hw2/outputFile.dat

The closest 2 matrices are … and …, and their distance is 0.5.

Evaluation rules

1) Compilation error: grade set to 1; if the error is resolved during the demo, then evaluation continues.

2) Compilation warning (with respect to the -Wall flag); -1 for every warning until 10. -20 points if there are more than 10 warnings; no chance of correction at demo.

3) No makefile: -30

</div>
</div>
<div class="layoutArea">
<div class="column">
March 24th, 2022

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
4) No pdf report submitted (or submitted but insufficient, e.g. 3 lines of text with no design explanation, etc): -20. Other file formats are not admissible.

5) If the required command line arguments are missing/invalid, your program must print usage information and exit. Otherwise: -10

6) The program crashes or doesn’t produce expected output with normal input: -100

7) The program doesn’t satisfy a requirement: -100

8) Presence of memory leak (regardless of amount – checked with valgrind) -30

9) Late submissions will not be accepted

10) In case of an arbitrary error, exit by printing to stderr a nicely formatted informative message. Otherwise: -10

11) Cleanup after the children processes, no zombie processes, -50 otherwise.

12) All file I/O must be done using system calls. Take precautions against signals interrupting your operations. -30 otherwise.

Is my homework submission valid?

If P reads the input, creates the children processes and passes them the proper information, then yes.

</div>
</div>
</div>
