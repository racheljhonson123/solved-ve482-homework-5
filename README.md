Download Link: https://assignmentchef.com/product/solved-ve482-homework-5
<br>
<h1><strong>Ex. 1 — </strong>Simple questions</h1>

<ol>

 <li>A system has two processes and three identical resources. Each process needs a maximum of two resources. Can a deadlock occur? Explain.</li>

 <li>A computer has six tape drives, with n processes competing for them. Each process may need two drives. For which values of <em>n </em>is the system deadlock free?</li>

 <li>A real-time system has four periodic events with periods of 50, 100, 200, and 250 msec each. Suppose the four events require 35, 20, 10, and x msec of CPU time, respectively. What is the largest value <em>x </em>for which the system is schedulable?</li>

 <li>Round-robin schedulers normally maintain a list of all runnable processes, with each process occurring exactly once in the list. What would happen if a process occurred more than once in the list? Would there be any reason for allowing this?</li>

 <li>Can a measure of whether a process is likely to be CPU bound or I/O bound be detected by analyzing the source code. How to determine it at runtime?</li>

</ol>

<h1><strong>Ex. 2 — </strong>Deadlocks</h1>

Assuming three resources consider the following snapshot of a system.

<table width="285">

 <tbody>

  <tr>

   <td width="71">Process</td>

   <td width="74">Allocated</td>

   <td width="77">Maximum</td>

   <td width="62">Available</td>

  </tr>

  <tr>

   <td width="71"><em>P</em><sub>1</sub></td>

   <td width="74">010</td>

   <td width="77">753</td>

   <td width="62">332</td>

  </tr>

  <tr>

   <td width="71"><em>P</em><sub>2</sub></td>

   <td width="74">200</td>

   <td width="77">322</td>

   <td width="62"> </td>

  </tr>

  <tr>

   <td width="71"><em>P</em><sub>3</sub></td>

   <td width="74">302</td>

   <td width="77">902</td>

   <td width="62"> </td>

  </tr>

  <tr>

   <td width="71"><em>P</em><sub>4</sub></td>

   <td width="74">211</td>

   <td width="77">222</td>

   <td width="62"> </td>

  </tr>

  <tr>

   <td width="71"><em>P</em><sub>5</sub></td>

   <td width="74">002</td>

   <td width="77">433</td>

   <td width="62"> </td>

  </tr>

 </tbody>

</table>

<ol>

 <li>Determine the content of the Request matrix.</li>

 <li>Is the system in a safe state?</li>

 <li>Can all the processes be completed without the system being in an unsafe state at any stage?</li>

</ol>

<strong>Ex. 3 — </strong><em>Programming</em>

Implement the Banker’s algorithm.

<h1><strong>Ex. 4 — </strong>Minix 3</h1>

How is scheduling handled in Minix 3? Provide clear explanations on how to find the information just by exploring the source code of Minix kernel.

<h1><strong>Ex. 5 — </strong>The reader-writer problem</h1>

In the <em>reader-writer problem</em>, some data could be accessed for reading but also sometimes for writing. When processes want to read the data they get a <em>read lock </em>and a <em>write lock </em>for writing. Multiple processes could get a read lock at the same time while a write lock should prevent anybody else from reading or writing the data until the write lock is released.

To solve the problem we decide to use a global variable count together with two semaphores: count_lock for locking the count variable, and db_lock for locking the database. To get a write lock we can proceed as follows:

<ol>

 <li>Explain how to get a read lock, and write the corresponding pseudocode.</li>

 <li>Describe what is happening if many readers request a lock.</li>

</ol>

To overcome the previous problem we will block any new reader when a writer becomes available.

<ol start="3">

 <li>Explain how to implement this idea using another semaphore called read_lock.</li>

 <li>Is this solution giving any unfair priority to the writer or the reader? Can the problem be considered as solved?</li>

</ol>