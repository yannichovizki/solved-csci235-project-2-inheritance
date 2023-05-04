Download Link: https://assignmentchef.com/product/solved-csci235-project-2-inheritance
<br>
Project2 will build on Project1 to work with <strong>inheritance</strong> and <strong>separate compilation:</strong> after completion of this project you should be comfortable compiling multiple classes into one program with g++, understand #includes and work with basic inheritance. <u>If</u> <u>you are not absolutely comfortable with all of this, please seek help immediately</u> (contact me or visit the labs to work with our UTAs).

You will write 3 very simple classes that <u>derive from </u><u>Animal</u> but <strong>also have other attributes specific to their type</strong>.

<strong>You will write the following</strong> <strong>3 classes</strong>:

-Mammal

-Bird

-Fish

<strong> </strong>

<strong>Implementation: </strong>

You must write the 3 classes (both .hpp and .cpp files <strong>for each class</strong>) based on the following specification (FUNCTION PROTOTYPES AND MEMBER VARIABLE NAMES MUST MATCH EXACTLY). As you implement these classes <u>think about what is</u> <u>inherited and what is not</u> (e.g. constructors are not inherited!!!). Also think about the order in which constructors are called, and how/where must you explicitly call the base class constructor. <u>Constructors must initialize data members to 0 or false unless</u> <u>an argument is passed for that data member</u>. You must also modify Animal to support inheritance and provide direct access from the derived classes to its private members.

Remember, <strong>you must thoroughly document your code!!!</strong>

<strong> </strong>

<strong>class Mammal </strong><strong>public</strong><strong> members:</strong>

Mammal();

Mammal(std::string name, <strong>bool</strong> domestic = <strong>false</strong>, <strong>bool</strong> predator = <strong>false</strong>);      <strong>bool</strong> hasHair() <strong>const</strong>;      <strong>bool</strong> isAirborne() <strong>const</strong>;      <strong>bool</strong> isAquatic() <strong>const</strong>;      <strong>bool</strong> isToothed() <strong>const</strong>;      <strong>bool</strong> hasFins() <strong>const</strong>;      <strong>bool</strong> hasTail() <strong>const</strong>;      <strong>int</strong> legs() <strong>const</strong>;      <strong>void</strong> setHair();      <strong>void</strong> setAirborne();      <strong>void</strong> setAquatic();      <strong>void</strong> setToothed();     <strong>void</strong> setFins();      <strong>void</strong> setTail();      <strong>void</strong> setLegs(<strong>int</strong> legs);

<strong>class Mammal </strong><strong>private</strong><strong> members:</strong>

<strong>bool</strong> hair_;

<strong>bool</strong> airborne_;      <strong>bool</strong> aquatic_;      <strong>bool</strong> toothed_;      <strong>bool</strong> fins_;      <strong>bool</strong> tail_;      <strong>int</strong> legs_;

<strong>class Bird </strong><strong>public</strong><strong> members:</strong>

Bird();

Bird(std::string name, <strong>bool</strong> domestic = <strong>false</strong>, <strong>bool</strong> predator = <strong>false</strong>);      <strong>bool</strong> isAirborne() <strong>const</strong>;      <strong>bool</strong> isAquatic() <strong>const</strong>;      <strong>void</strong> setAirborne();      <strong>void</strong> setAquatic();

<strong>class Bird </strong><strong>private</strong><strong> members:</strong>

<strong>bool</strong> airborne_;      <strong>bool</strong> aquatic_;

_____________________________________________________________________________

<strong>class Fish </strong><strong>public</strong><strong> members:</strong>

Fish();

Fish(std::string name, <strong>bool</strong> domestic = <strong>false</strong>, <strong>bool</strong> predator = <strong>false</strong>);

<strong>bool</strong> isVenomous() <strong>const;</strong>     <strong>void</strong> setVenomous();

<strong>class Fish </strong><strong>private</strong><strong> members: </strong> <strong>bool</strong> venomous_; <strong>Testing: </strong>

You must always test your implementation <strong>INCREMENTALLY</strong>!!!

<strong><em>What does this mean? </em></strong>

<ul>

 <li>Implement and test one class at a time!!!</li>

 <li>For each class:</li>

 <li>Implement one function/method and test it thoroughly (multiple test cases + edge cases if applicable)</li>

 <li>Implement the next function/method and test it …</li>

 <li>…</li>

</ul>

<strong><em>How do you do this?</em></strong><em>  </em>

Write your own <strong>main()</strong> function to test your classes. In this course you will never submit your test program but you must always write one to test your classes. First implement and test the Mammal class. Start from the constructor(s), then move on to the other functions.  Instantiate an object of type Mammal and as you implement each method, call it in main and test that it is working correctly. Choose the order in which you implement your methods so that you can test incrementally (i.e. implement mutator functions before accessor functions). Sometimes functions depend on one another. If you need to use a function you have not yet implemented, you can use <strong>stubs: </strong>a dummy implementation that always returns a single value for testing (don’t forget to go back and implement the stub!!! If you put the word STUB in a comment, some editors will make it more visible so you will remember to implement it later) For example:

<em>//******** STUB ************//</em> <strong>bool</strong> Animal::isPredator() <strong>const</strong>

{

<strong>return</strong> false; }

<u>Note:</u> this will make much more sense as your programs become more complex, but it is very important to understand the fundamental concepts and develop good implement/test/debug habits from the very beginning.

Once you are done with the Mammal class, you can move on to implementing Bird, then Fish.







In your main function you also want to test for inheritance. Think about:

<ul>

 <li><strong>Can you access members of the base class from the derived class? Test it!!! </strong></li>

 <li><strong>Test calling a member function of the base class via an object to type derived. Make sure it works! </strong></li>

</ul>