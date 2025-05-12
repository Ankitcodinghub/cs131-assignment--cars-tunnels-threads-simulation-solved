# cs131-assignment--cars-tunnels-threads-simulation-solved
**TO GET THIS SOLUTION VISIT:** [CS131 Assignment -Cars-Tunnels Threads Simulation Solved](https://www.ankitcodinghub.com/product/cs131-assignment-cars-tunnels-threads-simulation-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;91017&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS131 Assignment -Cars-Tunnels Threads Simulation Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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
Overview

Your task is to implement a simulation of tunnels and vehicles using Java Threads. There will be few tunnels, but many vehicles. There will be several constraints on how many vehicles of each type a tunnel can contain at any given time. After you implement this primary system, you will implement a higher-level tunnel controller that will schedule access to the tunnels based on a priority system.

The project is split into 2 required tasks and 1 extra-credit task. Task 1 requires you to use Java default synchronized methods and busy waiting to prevent race conditions. Task 2 requires you to build on your synchronized code and add Java condition variables to avoid busy-waiting and add a scheduler. The extra credit task asks you to use the Java condition variables to make the scheduler preemptive.

Task 1 has an earlier due date than Task 2 and the extra-credit assignment. See LATTE for due dates.

Tunnel Description

Any implementation of the Tunnel interface must satisfy the following properties:

<ul>
<li>● &nbsp;Each tunnel has only one lane, so at any given time all vehicles must be traveling in the
same direction.
</li>
<li>● &nbsp;Only three cars may be inside a tunnel at any given time.

● Only one sled may be inside a tunnel at any given time. ● Cars and sleds cannot share a tunnel.

As you know from learning about concurrency, without proper synchronization, these constraints could be violated since a thread may secure permission to enter a tunnel, then be interrupted before it can actually enter, at which point another thread may also secure permission to enter the tunnel and do so. When the first thread to get permission to enter the tunnel does so, one of the invariants may be violated (e.g., maybe a sled and car will be in the tunnel at the same time). Part of your job in this assignment is to use synchronization to prevent such race conditions from occurring regardless of scheduling.

To implement your solutions you will need to use the code base provided by us, described below. This code base includes a test harness that allows us (and you) to test the correctness of your solutions. You will be therefore instructed to follow certain conventions in your code and will be not allowed to modify certain classes. For example, your code will not be starting or joining client threads. Instead, the threads will be started by the test harness. Please follow the instructions carefully. You will need to understand how the entire provided code works to complete your assignment.

Provided Code

The code for this assignment is divided into the following packages
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
cs131.pa2.Abstract

The Abstract package contains the abstract classes and interfaces that your program must implement. You are not allowed to modify any of the files within this package

cs131.pa2.Abstract.Log

The Abstract.Log package contains classes used to record the actions of the car. These classes are used by the test packages to evaluate that constraints have not been violated. The log is not a means for passing messages. The only reference to Log classes in your code should be in the ConcreteFactory.createNewPriorityScheduler method. You are not allowed to modify any of the files within this package.

cs131.pa2.Test

You may not edit any of the test classes, but we highly encourage you to study them for your understanding and to aid in discovering why a test is failing.

cs131.pa2.CarsTunnels

The CarsTunnels package contains a few mostly empty classes that implement the classes found in the Abstract package. All of the code pertaining to your solution of this assignment must go in this package. You are free to add, edit, rename, and delete files in this package in the course of implementing your solutions.

API Documentations

You will want to inspect the java files yourself, but to get you started we include the API docs generated with javadoc from the files we provide.

Task 1: The Basic Tunnel Implementation

You must create a class called BasicTunnel (in a file called BasicTunnel.java) that implements the interface Tunnel, and then within that class carry out the following tasks:

● Enforce the Tunnel Restrictions described above.

● Use the Java synchronized keyword to prevent race conditions (without introducing

deadlock).

When this task is complete your code should pass all tests included in BehaviorTest, and SimulationTest.Basic_Tunnel_Test.

Task 2: The Priority Scheduler

You have now successfully programmed BasicTunnel which enforces entry criteria and prevents race conditions. However, there are two problems with the design of BasicTunnel:

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
<ul>
<li>● &nbsp;While no tunnel is available to a Vehicle, that Vehicle busy-waits (loops over all tunnels repeatedly inside of its run() method).</li>
<li>● &nbsp;There is no way of prioritizing important vehicles (say, an ambulance) over less-important vehicles (say, an ice cream truck).
Priority Defined

● Priority is a number between 0 and 4 ( inclusive).
</li>
</ul>
● A higher number means higher priority.

Implementation

You must create a class called PriorityScheduler (in PriorityScheduler.java) that implements Tunnel and controls access to a collection of Tunnels in order to implement the priority scheduling policy described above. The Tunnels “behind” the PriorityScheduler will be BasicTunnels. BasicTunnel should be the same class you implemented for the first part of this project. PriorityScheduler will carry out the following tasks:

<ul>
<li>● &nbsp;Keep references to BasicTunnels as private member variables inside PriorityScheduler.</li>
<li>● &nbsp;When a Vehicle calls tryToEnter(vehicle) on a PriorityScheduler instance, the following general steps should be executed:
○ If vehicle.getPriority() is less than the highest priority from among all the other vehicles waiting to enter a tunnel (i.e., there is another vehicle with higher priority) ○ Or there are no other vehicles with higher priority but there are no tunnels into which

the vehicle can currently enter,
</li>
</ul>
○ Then the vehicle thread must wait;

○ Otherwise the vehicle successfully enters one of the tunnels.

<ul>
<li>● &nbsp;When a Vehicle v exits the scheduler by calling exitTunnel on a PriorityScheduler instance, the scheduler must call exitTunnel(v) on the appropriate tunnel from the collection of tunnels managed by the scheduler (remember, you may not modify Vehicle or any of the other classes provided to you, or BasicTunnel, so you must solve this problem within PriorityScheduler). After a vehicle has successfully exited a tunnel, the waiting vehicles should be signaled to retry to enter a tunnel. Note that the vehicles with highest priority should be allowed to enter.</li>
<li>● &nbsp;Use condition variables to avoid busy waiting when the car cannot find a tunnel to enter. Make sure the use of the condition variables is safe.
When this task is complete your code should pass all tests included with this assignment, except the SimulationTest.Preemptive_Priority_Scheduler_Test which refers to the extra credit.

No “main” method

Note that your only point of entry in the code we provide is through the JUnit tests, which will set up the environment in which your client threads will run. Your tasks for this assignment do
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
not include writing a main method. Rather, you must rely on your understanding of busy waiting/condition variables, and the JUnit tests to know if you have completed the assignment.

Important Note about Disallowed Java Tools

In PA1, you were instructed to consider using a synchronized class provided by Java for inter- thread communication (LinkedBlockingQueue) to solve the problem. For this project, that is not allowed; you may not use any synchronized data structure included in the Java API. You must write your own (using the “synchronized” keyword). Of course, you can and should use non- synchronized data structures in the Java standard library. You can consult the API docs to see if a data structure is synchronized.

You also may not use the thread priority methods provided by Java (e.g., you may not use Thread.setPriority).

Extra Credit: Preemptive Scheduler

This task is not required. If you choose to do it, it will be worth 15% extra credit. Please do not

attempt it until you are confident that tasks 1 and 2 are implemented correctly. Please run your design idea by the TA before you start coding the extra credit portion.

Your extra credit task is to modify your scheduler to be preemptive. In order to do this, you are allowed to modify the doWhileInTunnel method and the constructors of the Vehicle class. The new scheduler class must be called PreemptivePriorityScheduler.

Preemption Rules

<ul>
<li>● &nbsp;The highest priority value (4) will be reserved for ambulances</li>
<li>● &nbsp;An ambulance may share a tunnel with any other vehicles (including a sled) except another ambulance (i.e., the only time an ambulance must wait is if there is already an ambulance in all tunnels).</li>
<li>● &nbsp;Any time an ambulance wants to enter a tunnel, any vehicles in that tunnel must immediately pull over and wait for the ambulance to completely pass through the tunnel. That is, the vehicle cannot make progress toward the end of the tunnel while the Ambulance is in the tunnel.</li>
<li>● &nbsp;Once an ambulance leaves the tunnel, vehicles in the tunnel start making progress again.
Implementation
</li>
</ul>
● Add new vehicle type Ambulance with the fastest possible speed. ● Modify Vehicle.doWhileInTunnel as follows:

○ Use Java condition variables to avoid busy-waiting while an ambulance is in a tunnel.

</div>
</div>
<div class="layoutArea">
<div class="column">
○

</div>
<div class="column">
Use await(timeout) where the timeout is the same as the parameter to

</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
Thread.sleep in the implementation provided to you.

○ Think carefully about what object to lock (remember, a synchronized method locks

“this”). You may modify the Vehicle constructor (or add a new field and setter/getter) if you wish for the purpose of referencing another object to synchronize on.

● Here is an example of how Vehicles wait on an ambulance:

○ Say a vehicle waits in a tunnel for 100 ms, and has currently been waiting for 50 ms

○ When it is notified that an ambulance is entering its tunnel, it waits indefinitely for the ambulance to leave the tunnel

○ When the ambulance notifies it that it has left the tunnel, the vehicle begins its timeout wait again, using whatever time was remaining on the clock from when it was woken up the first time by the ambulance. In other words, the vehicle calls await(50).

Tests

You will have to pass all tests and your code must satisfy the described conditions to get full credits.

Hints

instanceof operator

You might find the instanceof operator helpful. instanceof can tell you if an object can be downcast from a parent type into a child type. Typically, we don’t use it because there are better techniques (polymorphism leverages the type system to do the work for you), but for this problem it will probably help you out.

Here is an example:

<pre>public class TestInstanceof {
    public static class Parent {}
    public static class Child1 extends Parent {}
    public static class Child2 extends Parent {}
</pre>
<pre>    public static void main(String[] args) {
        Parent p1 = new Child1();
        Parent p2 = new Child2();
</pre>
if(p1 instanceof Child1) {

System.out.println(“p1 is instance of Child1”);

<pre>        }
        if(p1 instanceof Child2) {
</pre>
</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
<pre>            System.out.println("p1
</pre>
<pre>        }
        if(p2 instanceof Child1) {
</pre>
<pre>            System.out.println("p2
</pre>
<pre>        }
        if(p2 instanceof Child2) {
</pre>
<pre>            System.out.println("p2
</pre>
<pre>p1 is instance of Child1 p2
is instance of Child2
</pre>
</div>
<div class="column">
<pre>is instance of Child2");
</pre>
<pre>is instance of Child1");
</pre>
<pre>is instance of Child2");
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
}

This outputs:

</div>
</div>
<div class="layoutArea">
<div class="column">
} }

</div>
</div>
</div>
