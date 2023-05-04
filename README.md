Download Link: https://assignmentchef.com/product/solved-csc-115-assignment-4-hospital-admissions
<br>
<h1>Learning outcomes</h1>

When you have completed this assignment, you are expected to be able to:

<ul>

 <li>Use a BinarySearchTree data structure to</li>

</ul>

◦ store and manipulate comparable items,

◦ traverse the tree to produce an ordered list.

<ul>

 <li>Continue to apply good programming practice in</li>

</ul>

◦ designing programs,

◦ proper documentation, and

◦ testing and debugging problems with code.

<strong>Hospital Admission Information System Description.</strong>

The local hospital Admissions Department needs to keep a record of current patients and room numbers.  During the day, the Admission staff update, insert, delete and retrieve patient information from one of the workstations in the Admissions Department. Visitors also ask for information about the location of their loved ones.  In the evening, when the Admissions Desk staff go home, two volunteers take over the job of locating patients for the evening and night visitors.  However, the volunteers to do not have access to a workstation and therefore work from a printout of ordered patient names and room numbers.  This list is printed daily for them by one of the Admission staff just before she goes home.

<h2>Problem description</h2>

We are asked to design a system for the Admissions Department.  The hospital generally deals with thousands of admitted patient information and patient enquiries need to be handled quickly. We elect to use a BinarySearchTree data structure for relatively quick and easy access to the patient records, and because the <em>inorder</em> traversal easily processes records in their natural order, the Admissions Desk can produce an ordered printout for the volunteers at night.

<h2>Programming requirements</h2>

You will write the source code for the following single class:

<ul>

 <li>The underlying data structure will be a reference-based BinarySearchTree.</li>

</ul>

◦ Note that you are not required to create the complete BinarySearchTree

ADT.  In this assignment, the required methods are very specific to the <em>HospitalPatient </em>class, which are the elements of this data structure.

The following fully-developed Java files are provided to support the code you write:

<ul>

 <li><em>java. </em>This defines the hospitalized patient’s record. Since these are the elements of the tree structure, you need to be familiar with the content and the methods.</li>

 <li><em>java.</em> This is a basic node for any BinaryTree. However, this version is not generic,  but specific to the admitted patient records that are stored inside the AdmittedPatients tree.</li>

 <li><em>java.</em> Every admitted patient must have an admission date. This is as simple as can be for the Admissions Department’s needs.  The GregorianCalendar that is part of Java’s API is too complicated for the hospital’s needs.</li>

 <li><em>java.</em> This is provided for you so you can track the</li>

</ul>

BinarySearchTree’s structure, during the implementation and testing phase.

<h2>Implementaton details</h2>

All the specifications documentaion can be accessed via the following <a href="https://connex.csc.uvic.ca/access/content/group/590c385e-c956-4725-aa88-4b02a97059f0/Lab%20Resources_Bette_/repository/assn4/index.html">link</a><a href="https://connex.csc.uvic.ca/access/content/group/590c385e-c956-4725-aa88-4b02a97059f0/Lab%20Resources_Bette_/repository/assn4/index.html">.</a> (Make sure you are logged onto conneX when accessing the link directly.) To get you started, we recommend the following:

<ol>

 <li>Download the files associated with this assignment into a fresh working directory (csc115/assn4 for example).</li>

 <li>Read through the TreeNode, SimpleDate, and HospitalPatient source code. Keep a copy of the specifications close by when developing the code that you are writing.</li>

 <li>Create the minimal class for AdmittedPatients, copying and pasting the required specified methods.</li>

 <li>Compile each of the files.</li>

 <li>Refer to the textbook’s description of the various parts of the BinarySearchTree ADT when you start to fill in the methods.</li>

 <li>Start with the <em>admit </em></li>

 <li>Implement the <em>discharge</em> method last.</li>

</ol>

<ul>

 <li>There are 3 cases for the position of the node to delete. These are described in the specification details.  Start with the simplest case.</li>

</ul>

You are welcome to use any number of extra <em>helper</em> methods to make your code easier to understand and handle.  You may not create helper classes.

<h2>Recursion vs. non-recursion</h2>

The <em>getPatient</em> and <em>printLocations</em> methods are fairly straight-forward with implementations that use recursion.  The <em>admit </em>and <em>discharge</em> method can be implemented recursively or non-recursively.  The non-recursive management requires the maintenance of a <em>parent </em>reference for each of the <em>TreeNode </em>objects. The recursive management does not need to use this reference.

The textbook descriptions of the tree structure and method implementations use recursion.  However, some textbooks also describe non-recursive insertion and deletion methods for BinarySearchTrees.  You are welcome to use whatever makes sense.

<strong>Internal testng:</strong>

The AdmittedPatients class will require testing to make sure that each of the methods work.  Specifically the admit and discharge methods will cause changes in the tree structure that are very specific, and it is easier to see the results than to print them all out.

The following internal testing example is not complete, but is meant to get you started.  The constructor calls are spread over 2 lines to prevent word-wrapping on this document.

AdmittedPatients admitted = new AdmittedPatients();

HospitalPatient p1 = new HospitalPatient( new SimpleDate(2018,2,27),”Duck”,”Donald”,’C’,123);

HospitalPatient p2 = new HospitalPatient( new SimpleDate(2018,1,15),”Mouse”,”Minnie”,’B’,307);

HospitalPatient p3 = new HospitalPatient( new SimpleDate(2018,3,1),”Dog”,”Goofie”,’A’,422);

HospitalPatient p4 = new HospitalPatient( new SimpleDate(2017,12,25),”Newman”,”Alfred”,’X’,111);

admitted.admit(p1);       admitted.admit(p4);       admitted.admit(p3);       admitted.admit(p2);       admitted.printLocations();

// these two lines cause the tree to be viewed in a little // resizable window.

ViewableTree dbt = new ViewableTree(admitted);       dbt.showFrame();

<strong>The single file to submit:</strong>

<ol>

 <li><em> AdmittedPatients.java</em></li>

</ol>

<h1>Grading</h1>

<ul>

 <li>Submissions are expected to follow all of the requirements for the submitted files in the <a href="https://connex.csc.uvic.ca/access/content/group/590c385e-c956-4725-aa88-4b02a97059f0/Lab%20Resources_Bette_/repository/assn4/index.html">specification documents</a><a href="https://connex.csc.uvic.ca/access/content/group/590c385e-c956-4725-aa88-4b02a97059f0/Lab%20Resources_Bette_/repository/assn4/index.html">.</a></li>

 <li>Evidence of internal testing must be present: you may comment out any testing the main methods if you wish.</li>

 <li>The coding conventions, specifed in the <a href="https://connex.csc.uvic.ca/access/content/group/590c385e-c956-4725-aa88-4b02a97059f0/Lab%20Resources_Bette_/codingConventionsCSC115.pdf">pdf </a><a href="https://connex.csc.uvic.ca/access/content/group/590c385e-c956-4725-aa88-4b02a97059f0/Lab%20Resources_Bette_/codingConventionsCSC115.pdf">d</a>ocument on conneX, must be followed.</li>

 <li>Please post questions to the forum set up for this assignment; any clarifications posted there are part of the overall specifications. If there are any major changes, this will be announced and you will receive an email.</li>

</ul>