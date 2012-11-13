# CSCI 1302 - Lists Project (cs1302-lists)

Skeleton code for the lists project assigned to the students in Michael E. 
Cotterell's Fall 2012 CSCI 1302 class at the University of Georgia. Please read 
the entirety of this file before beginning your project.

## Academic Honesty

You implicitly agree to Academic Honesty policy as outlined in the course 
syllabus and course website (available at: http://cs.uga.edu/~mec/cs1302/).

In accordance with the notice above, I must caution you to **not** fork this
repository on GitHub if you have an account. Doing so will more than likely make
your copy of the project publicly visible. Please follow the instructions 
contained in the Resources section below in order to do your development on
<code>nike</code>.

## Project Description

Your goal is to persue an adventure in the land of lists! This project is pretty
straight forward. Perform the project tasks listed below. 

## Project Tasks

Before you submit your project, you need to perform the following tasks:

 1. (10 points) Implement <code>ArrayList.java</code> from scratch according to 
    the <code>List</code> interface that is provided in <code>cs1302.lists.List</code>.
    This list implementation will be backed by a _regular Java array_. You are not
    allowed to use any of the other data structures that are included with Java when
    implementing this class.

 2. (20 points) Implement <code>LinkedList.java</code> from scratch according to 
    the <code>List</code> interface that is provided in <code>cs1302.lists.List</code>.
    This list implementation will be backed by a singly linked list. You are not
    allowed to use any of the other data structures that are included with Java when
    implementing this class.

 3. (10 points) Implement <code>DoubleLinkedList.java</code> according to the 
    <code>List</code> interface that is provided in <code>cs1302.lists.List</code>.
    This list implementation will be backed by a doubly linked list. You are not
    allowed to use any of the other data structures that are included with Java when
    implementing this class. In order to make things easier, you may extend your 
    <code>LinkedList</code> class when writing the code for <code>DoubleLinkedList</code>.

 4. (10 points) Create JUnit tests for your list classes in the 
    <code>src/test/java/cs1302/lists</code> directory. Do not cheat yourself by 
    creating poor tests and or faking your tests. They will be beneficial in 
    helping you debug your code.

 5. (10 points) Ensure that your code is properly documented using in-line comments as 
    necessary. In general, you should describe in regular terms what it is the
    code that you are writing is doing. Please note that you do not need to write JavaDoc 
    comments for the methods that implement an interface as they will inherit the 
    comments from the interface. However, if you create any new methods or classes 
    then they will need to be properly documented using JavaDoc comments and tags.

 6. (40 points) Experiment with your list implementations by creating a <code>Driver</code>
    class that compares the actual running times of each list implementation when 
    adding, removing, and searching for 10 million random elements with each. 
    Generate a report that compares your results. 
    Include in your report an asymptotic analysis of the time complexity of your 
    implementations. You should include the growth functions (i.e., t(n)) for the
    add, remove, and search methods in each of your three implementations as
    well as the worst-case time complexity of each method expressed in Big-0
    notation. When providing the growth functions and time complexities, you will
    need to justify and explain why the functions and time complexities you
    provided work based on your code. You may submit this portion of the poject
    in one of the following formats: PDF, LaTeX, or Markdown. No other formats 
    will be accepted. 
   
 6. Update the <code>README.md</code> in your project directory to contain the 
    following information at the top of the file (updating it with your own 
    information:

    ```markdown
    # Project Submission

 Author: YOUR NAME (LAST 3 DIGITS OF 810 NUMBER HERE)

    [If you did any of the extra credit then please indicate that here.]
    ```
        
## Extra Credit Project Tasks

You may earn extra credit for each of the tasks listed below:

 1. (20 points extra credit) Implement <code>SortedArrayList.java</code> from scratch according to 
    the <code>SortedList</code> interface that is provided in <code>cs1302.lists.List</code>.
    This list implementation will be backed by a _regular Java array_. You are not
    allowed to use any of the other data structures that are included with Java when
    implementing this class. In order to make things easier, you may extend your 
    <code>ArrayList</code> class when writing the code for <code>SortedArrayList</code>.
    You must also include <code>SortedArrayList</code> in your report in order
    to receive this extra credit.

 2. (20 points extra credit) Implement <code>SortedLinkedList.java</code> from scratch according to 
    the <code>SortedList</code> interface that is provided in <code>cs1302.lists.List</code>.
    This list implementation will be backed by a singly linked list. You are not
    allowed to use any of the other data structures that are included with Java when
    implementing this class. In order to make things easier, you may extend your 
    <code>LinkedList</code> class when writing the code for <code>SortedLinkedList</code>.
    You must also include <code>SortedLinkedList</code> in your report in order
    to receive this extra credit. 

 2. (10 points extra credit) Implement <code>SortedDoubleLinkedList.java</code> from scratch according to 
    the <code>SortedList</code> interface that is provided in <code>cs1302.lists.List</code>.
    This list implementation will be backed by a doubly linked list. You are not
    allowed to use any of the other data structures that are included with Java when
    implementing this class. In order to make things easier, you may extend your 
    <code>DoubleLinkedList</code> class when writing the code for <code>SortedDoubleLinkedList</code>.
    You must also include <code>SortedLinkedList</code> in your report in order
    to receive this extra credit. 

## Linked Lists

In computer science, a linked list is a data structure consisting of a group of 
objects called <code>nodes</code> which together represent a sequence. Under the 
simplest form, each <code>node</code> is composed of a <code>value</code> and a 
reference (in other words, a link) to the <code>next</code> node in the sequence. 
We call this data structure a singly linked list. In general, the last node in
the sequence should point, in its <code>next</code> reference, to the first node.

A slightly more complex variant adds some additional links. When each <code>node</code>
is composed of a <code>value</code> and a reference to both the <code>previous</code>
and <code>next</code> nodes in the sequence, we call the data structure a doubly
linked list. 

The way these data structures are usually implemented according to the following
general guidelines:

 1. Create a node class that includes a place to store the value of the element
    that is to be stored in the node as well as the appropriate number of
    reference variables to store the links (<code>next</code> for a singly linked 
    list and both <code>previous</code> and <code>next</code> for a doubly linked 
    list).
 2. In the list class, have a reference variable called <code>head</code> that
    points to the first node in the sequence. When the size of the list is 0,
    this reference is null. When the first element is added to the list, a node
    object is created, the element is stored in the node, and the <code>head</code>
    is then set to reference that node.
 3. Whenever an element is added to the list, a node object is created, the element 
    is stored in the node, and the node is added to the sequence in the appropriate
    place by adjusting the links.
 4. Whenever an element is removed from the list, the links of the nearby nodes
    are altered so that the node that contains the element is no longer in the
    sequence.
 5. Searching is performed by traversing the links.

## Resources

The files for this project are hosted Github using <code>git</code>. They can be
retrieved by cloning the repository found at <code>git@github.com:mepcotterell-cs1302/cs1302-lists.git</code>. 
For example, you can issue the following command to clone the repository:

    $ git clone git@github.com:mepcotterell-cs1302/cs1302-lists.git LastName-FirstName-p4

As always, I suggest developing directly on <code>nike.cs.uga.edu</code> because
this is where your project will be run and tested. Since <code>git</code> is 
already installed on <code>nike</code>, you can clone the project directly int your 
<code>nike</code> home directory.

If any changes are made to the project description or skeleton code, they will
be announced in class. In order to incorporate such changes into your code, you 
need only do a <code>git pull</code>.

Also, since <code>git</code> is a decentralized version control system, you will
have your own local copy of the repository. This means that you can log your 
changes using commits and even revert to a previous revision if necessary.

JavaDoc for the skeleton code should be available [here](http://cs.uga.edu/~mec/cs1302/).

## Directory Structure and Packages

All of the non-test classes for this project should be contained in the <code>src/main/java/cs1302/lists</code>
directory. These classes are in the <code>cs1302.lists</code> package.

All of the JUnit test classes for this project should be contained in the <code>src/test/java/cs1302/lists</code>
directory. These classes are also contained in the <code>cs1302.lists</code> 
package so that you do not need to do any imports to test your own code.

## Build System

For this project, we will be using the Simple Build System (sbt). If you clone 
the project from the GitHub repository then everything will be setup for you. In 
order to compile your project, you can use the following command:

    $ ./sbt compile

To run your JUnit tests, you may use the following command:

    $ ./sbt test

To run your project, use the following command:

    $ ./sbt run

In order to clean your project (remove compiled code), use the following command:

    $ ./sbt clean

## Submission Instructions

You will still be submitting your project via <code>nike</code>. Make sure your 
work is on <code>nike.cs.uga.edu</code> in a directory called 
<code>LastName-FirstName-p4</code>, and, from within the parent directory, 
execute the following command:

    $ submit LastName_FirstName-p4 cs1302a

It is also a good idea to email a copy to yourself. To do this, simply execute 
the following command, replacing the email address with your email address:

    $ tar zcvf LastName-FirstName-p4.tar.gz LastName-FirstName-p4
    $ mutt -s "[cs1302] p4" -a LastName-FirstName-p4.tar.gz -- your@email.com < /dev/null

## Questions

If you have any questions, please email them to Michael E. Cotterell at 
<code>mepcotterell+1302@gmail.com</code>

## Frequently Asked Questions

 1. What do I do if the <code>sbt</code> command does not execute?

    You probably need to make the file executable. To do this, simply make sure 
    you are in the same directory as <code>sbt</code> and issue the following
    command:

        $ chmod +x sbt

    This command updates the permissions on the file, making it executable for the
    current user.

 2. I created a <code>Driver</code> class (a class with a <code>main</code> method), 
    but <code>sbt</code> won't run it when I execute <code>sbt run</code>. How do I
    fix that?

    You should be able to fix the problem by executing the following command:

        $ sbt clean

