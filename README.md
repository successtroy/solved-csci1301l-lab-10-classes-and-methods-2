Download Link: https://assignmentchef.com/product/solved-csci1301l-lab-10-classes-and-methods-2
<br>
<h1>Introduction</h1>

In this lab, we will create our own class, namely <strong>Stat</strong>. The information of this class is described in the UML class diagram. Recalled what we have learned about the UML (<u>U</u>nified <u>M</u>odeling <u>L</u>anguage) and the class diagrams. A class diagram consists of a class name, attributes, and methods. For each member (an attribute or a method), there is an access modifier, such as public or private, to control which classes have access to it.




In this lab, you will work on two source codes/files. First, you will create the class that deals with statistics on data. Then, you will create a tester program (driver class) that uses the method in your first class and test the results.




<h1>—– Important! —–</h1>

Please be aware that successfully and timely completing this lab assignment is very important. You will use what you have completed in this assignment to work on the next assignment. If you fail to make the program work for this lab assignment, you are likely to fail in the next assignment.




If you have questions or unsolved issues for this assignment, we strongly suggest that you resolve all open issues and have cleared all doubts before you start working on the next lab assignment.

<strong> </strong>

<h2>Lab objectives</h2>




After completing this lab, you should be able to create classes by utilizing:

<ul>

 <li>constructors,</li>

 <li>access modifiers,</li>

 <li>instance variables,</li>

 <li>general methods with different return types,</li>

 <li>methods called another methods,</li>

 <li>specific accessor and mutator methods, and</li>

 <li>the equals() method and other user defined methods.</li>

</ul>

<strong> </strong>

<h2>Assignment</h2>

<strong> </strong>

In this lab, you will create a java program that deals with certain statistics of data. Details are described as follows:




<ol>

 <li>Use the UML diagram and method descriptions below to create your <strong>Stat </strong></li>

</ol>




<table width="487">

 <tbody>

  <tr>

   <td width="487"><strong>                         Stat </strong></td>

  </tr>

  <tr>

   <td width="487"><strong> </strong><strong>– data: double[] </strong><strong> </strong></td>

  </tr>

  <tr>

   <td width="487"><strong> </strong><strong>+ Stat() </strong><strong>+ Stat(double[] d) </strong><strong>+ getData(): double[] </strong><strong>+ setData(double[] d): void </strong><strong>+ equals(Stat s): boolean </strong><strong>+ toString(): String </strong><strong>+ min(): double </strong><strong>+ max(): double </strong><strong>+ average(): double </strong><strong>+ mode(): double </strong></td>

  </tr>

 </tbody>

</table>




The <strong>Stat</strong> class stores an array of double type values called <strong>data </strong>(private type). The <strong>data</strong> has the type double[], which is a reference type. This means that <strong>data</strong> itself will store a reference to the memory location where the array is store. However, <strong>data </strong>does not store the array.




According to this provided class diagram, you will implement public methods to compute the <strong>min</strong>, <strong>max</strong>, <strong>mode</strong>, and <strong>average</strong> of these values. Additionally, the program will also need the “get” and “set” methods. In this program, we ensure that each instance/object of the Stat class uses its own array of double type values. Therefore, you should defined <strong>getData()</strong> to create a copy of the data array and return <u>a reference to that copy</u>, rather than a reference to the original (think of why?). Similarly, the method <strong>setData(double[] d)</strong> creates a copy of the array <strong>d</strong> and assigns to <strong>data</strong> <u>a reference to the copy</u>.




<ol start="2">

 <li>After you have created the skeleton code of <strong>Stat</strong> class according the UML class diagram, implement the detail of the methods.</li>

</ol>

<h2>• Stat()</h2>

This is the default constructor for the class <strong>Stat</strong>. It should create a <strong>double</strong> array having a

single element <strong>0.0</strong>.

<h2>• Stat(double[] d)</h2>

This is another constructor for the class <strong>Stat</strong>. This constructor should create a <strong>double</strong> array of the same length as <strong>d</strong> and holding copies of the values of <strong>d</strong>. A reference to this new array should be assigned to <strong>data</strong>.

<h2>•getData()</h2>

This is an accessor, also known as <em>get </em>method. It is used to read/retrieve the values of <strong>data</strong>. This method should not return a reference to <strong>data</strong>. Instead, it should create a new array containing exactly the values contained in <strong>data</strong>, and then return a reference to this new array.

<h2>•setData(double[] d)</h2>

This is a mutator, also known as <em>set</em> method. It is used to set the values of the data array. The method should create a new array containing exactly the elements of <strong>d</strong> and assign to <strong>data</strong> a reference to this new array

(Hint: the method should not simply assign <strong>d</strong> to <strong>data</strong>).

<h2>•equals(Stat s)</h2>

This method returns the <strong>boolean</strong> value <strong>true</strong> if the <strong>data</strong> objects of both the calling Stat object and the passing Stat object <strong>s</strong> have all the same values in the same order, or <strong>false</strong> otherwise.

<h2>•toString()</h2>

This method returns a <strong>String</strong> of the data elements stored in the <strong>Stat</strong> object. Please look at the sample output at the end of the document for formatting. See how commas and square brackets are added. • <strong>min()</strong>

This method returns the minimum of the <strong>data </strong>array. • <strong>max()</strong>

This method returns the maximum of the <strong>data</strong> array.

<h2>•average()</h2>

This method returns the average of the <strong>data </strong>array. The average is a double type value as the mean value of a given array of numbers.

<h2>•mode()</h2>

The mode, according to this lab’s definition, is the value that occurs most frequently in a collection of all elements. In one element occurs more frequently in <strong>data</strong> than all others, then <strong>mode()</strong> should return that element. Otherwise, <strong>mode() </strong>should return <strong>Double.NaN</strong>, which means that no such an element that appears more frequently than any others.




Example 1: { 1, 1, 2, 2, 2, 3, 4, 5, 6}.  Element “2” appears 3 times, more than any other elements (“1” twice, other just once). Therefore, mode() returns 2.

Example 2: { 1, 1, 1, 2, 2, 2, 3, 4 }. Element “1” and element “2” both appear 3 times. There is no winner. Therefore, mode() returns NaN.




<ol start="3">

 <li>After you have created the Stat class, write a main method in a separate driver class to test each method of the Stat class. For each method, there should be several test cases to use. Refer to the sample program outputs for select test cases.</li>

</ol>




When you test your program, there are some considerations for the test cases (note that this is not a complete list):

<ul>

 <li>Can this program process an array full of numbers AND an empty array (i.e. no input of array)?</li>

 <li>Can this program handle values of integers and floating point numbers both?</li>

 <li>Can this program handle negative values?</li>

 <li>Can this program process mode() accurately when the most frequent value is available or unavailable?</li>

</ul>




<strong>Please note that you are NOT allowed to use any methods from java.util.Arrays or any Java Stream APIs throughout the entire program code. </strong>




<ol start="4">

 <li>Once you make the program working correctly. Understand the following statement for Academic Honesty and add it into the top of your source code to submit. The following lines should be added ABOVE the original first line of code.</li>

</ol>

/*

<ul>

 <li>[CLASS/FILE NAME].java * Author: [YOUR NAME]</li>

 <li>Statement of Academic Honesty:</li>

</ul>

*

<ul>

 <li>The following code represents my own work. I have neither</li>

 <li>received nor given inappropriate assistance. I have not copied</li>

 <li>or modified code from anywhere other than the authorized</li>

 <li>I recognize that any unauthorized sharing, assistance,</li>

 <li>or plagiarism will be handled in accordance with both the</li>

 <li>University of Georgia’s Academic Honesty Policy and the</li>

 <li>policies of this course. I recognize that my work is based on</li>

 <li>an assignment created by the Department of Computer</li>

 <li>Science at the University of Georgia. Any publishing or posting * of source code at any time for this project is prohibited.  */</li>

</ul>




Replace [CLASS/FILE NAME] with the required name according to the assignment instruction. Replace [YOUR NAME] with your actual name.




<h2>Submission instruction</h2>




After you have completed and thoroughly tested your program, upload and submit the file <em>Stat.java</em>.




You do not have to submit the driver class file that contains the main method. However, you may include it if you really want, but we will use different test cases to test your program.




<h2>Grading</h2>




A score between 0 and 10 will be assigned, with a minimum of 1 point increment (i.e. only integers).




<ol>

 <li>The source code is correctly provided, including the right file format/name extension. The file name is consistent with the source code’s class name. (1 point)</li>

 <li>Correct data types for variables are used, correct return types for the method are used, and correct access modifiers (public or private) are used. (1 point)</li>

 <li>Good programming practices are followed, including variable naming, coding layout, and comments. (1 point)</li>

 <li>No package declaration at the top of the program and no non-standard Java library or class is used, such as Arrays class, stream. (1 point)</li>

 <li>The program can pass the tests for each of these methods: equals, toString, min, max, average, and mode. (6 points)</li>

</ol>




Special notice regarding the submission:




<ol>

 <li>Late submission penalty. Points will be deducted from the original grade. If your submission is after the posted deadline…

  <ul>

   <li>within 24 hours: -3</li>

   <li>between 24 hours and 48 hours: -6</li>

   <li>between 48 hours and 72 hours: -9</li>

   <li>after 72 hours: assignment will not be accepted.</li>

  </ul></li>

</ol>




<ol>

 <li>If the source code file is missing, partially or completely broken, unable to open (including using a wrong file format), unable to compile, irrelevant to the assignment, purposely made to contain malicious codes, or determined to be an academic misrepresentation or a case of plagiarism, you will receive 0 grade for this assignment.</li>

</ol>







Below are sample inputs/outputs. This is not a comprehensive list of test cases.




<h3>Example 1</h3>

<em><u>Example main method:</u></em>

<strong>double</strong>[] data = {-5.3, 2.5, 88.9, 0, 0.0, 28, 16.5, 88.9, 109.5, -90, 88.9};

<strong>double</strong>[] data2 = {100.34, 50.01, 50.01, -8};

Stat stat1 = <strong>new</strong> Stat();




System.<em>out</em>.println(“stat1 data = ” + stat1.toString());

stat1 = <strong>new</strong> Stat(data);




System.<em>out</em>.println(“stat1 has been altered.”);

System.<em>out</em>.println(“stat1 data = ” + stat1.toString());




System.<em>out</em>.println(“stat1 min = ” + stat1.min());

System.<em>out</em>.println(“stat1 max = ” + stat1.max());

System.<em>out</em>.println(“stat1 average = ” + stat1.average());

System.<em>out</em>.println(“stat1 mode = ” + stat1.mode() + “
”);




Stat stat2 = <strong>new</strong> Stat(); stat2.setData(data2);

Stat stat3 = <strong>new</strong> Stat(stat1.getData());




System.<em>out</em>.println(“stat2 data = ” + stat2.toString());

System.<em>out</em>.println(“stat3 data = ” + stat3.toString());

System.<em>out</em>.println();

System.<em>out</em>.println(“stat1 is equal to stat2 using ”equals()”? ” + stat1.equals(stat2));

System.<em>out</em>.println(“stat1 is equal to stat3  using ”equals()”? ” + stat1.equals(stat3));

System.<em>out</em>.println(“stat1 is equal to stat3  using ”==”? ” + (stat1 == stat3));




<em><u>Example output:</u></em> stat1 data = [0.0] stat1 has been altered.

stat1 data = [-5.3, 2.5, 88.9, 0.0, 0.0, 28.0, 16.5, 88.9, 109.5, -90.0, 88.9] stat1 min = -90.0 stat1 max = 109.5 stat1 average = 29.80909090909091 stat1 mode = 88.9




stat2 data = [100.34, 50.01, 50.01, -8.0]

stat3 data = [-5.3, 2.5, 88.9, 0.0, 0.0, 28.0, 16.5, 88.9, 109.5, -90.0, 88.9]




stat1 is equal to stat2 using “equals()”? false stat1 is equal to stat3  using “equals()”? true

stat1 is equal to stat3  using “==”? false




<h3>Example 2</h3>

<em><u>Example main method:</u></em>

<strong>double</strong>[] data = {10.0, 20.0, 30.0};

Stat stat1 = <strong>new</strong> Stat(data);

data[0] = 100.0; data[1] = 200.0; data[2] = 300.0;




Stat stat2 = <strong>new</strong> Stat(data);




System.<em>out</em>.println(“stat1 data = ” + stat1.toString());

System.<em>out</em>.println(“stat2 data = ” + stat2.toString());

System.<em>out</em>.println(“The two arrays should be different”);




<em><u>Example output:</u></em>

stat1 data = [10.0, 20.0, 30.0] stat2 data = [100.0, 200.0, 300.0] The two arrays should be different

<strong> </strong>

<h3>Example 3</h3>

<em><u>Example main method:</u></em>

<strong>double</strong>[] data1 = {10.0, 20.0, 30.0};

Stat stat1 = <strong>new</strong> Stat(data1);

<strong> </strong>

<strong>double</strong>[] data2 = stat1.getData();




System.<em>out</em>.println(“The arrays are identical: ” + (data1 == data2));




<em><u>Example output:</u></em>

The arrays are identical: false




<h3>Example 4</h3>

<em><u>Example main method:</u></em>




<strong>double</strong>[] data1 = {10.0, 20.0, 30.0}; Stat stat1 = <strong>new</strong> Stat(); stat1.setData(data1); Stat stat2 = <strong>new</strong> Stat(data1); <strong>double</strong>[] data2 = stat1.getData();




System.<em>out</em>.println(“The arrays are identical: ” + (data1 == data2));

System.<em>out</em>.println(“stat2 equals stat1: ” + stat2.equals(stat1));

System.<em>out</em>.println(“stat1 equals stat2: ” + stat2.equals(stat1));




<em><u>Example output:</u></em>

The arrays are identical: false stat2 equals stat1: true stat1 equals stat2: true

<strong> </strong>

<h3>Example 5</h3>

<em><u>Example main method:</u></em>

Stat stat1 = <strong>new</strong> Stat();

System.<em>out</em>.println(“stat1 data = ” + stat1.toString());

System.<em>out</em>.println(“stat1 min = ” + stat1.min());

System.<em>out</em>.println(“stat1 max = ” + stat1.max());

System.<em>out</em>.println(“stat1 average = ” + stat1.average());

System.<em>out</em>.println(“stat1 mode = ” + stat1.mode());

System.<em>out</em>.println(“stat1 data = ” + stat1.toString());




<em><u>Example output:</u></em>

stat1 data = [0.0] stat1 min = 0.0 stat1 max = 0.0 stat1 average = 0.0 stat1 mode = 0.0

stat1 data = [0.0]




<h3>Example 6</h3>

<em><u>Example main method:</u></em>

<strong>double</strong>[] data = {1,2,2,3,3,4};

Stat stat1 = <strong>new</strong> Stat(data);




System.<em>out</em>.println(“stat1 data = ” + stat1.toString());

System.<em>out</em>.println(“stat1 min = ” + stat1.min());

System.<em>out</em>.println(“stat1 max = ” + stat1.max());

System.<em>out</em>.println(“stat1 average = ” + stat1.average());

System.<em>out</em>.println(“stat1 mode = ” + stat1.mode());

System.<em>out</em>.println(“stat1 data = ” + stat1.toString());




<em><u>Example output:</u></em>

stat1 data = [1.0, 2.0, 2.0, 3.0, 3.0, 4.0]

stat1 min = 1.0 stat1 max = 4.0 stat1 average = 2.5 stat1 mode = NaN

stat1 data = [1.0, 2.0, 2.0, 3.0, 3.0, 4.0]