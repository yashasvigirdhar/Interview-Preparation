<!----- Conversion time: 1.924 seconds.


Using this Markdown file:

1. Cut and paste this output into your source file.
2. See the notes and action items below regarding this conversion run.
3. Check the rendered output (headings, lists, code blocks, tables) for proper
   formatting and use a linkchecker before you publish this page.

Conversion notes:

* Docs to Markdown version 1.0β17
* Tue Sep 17 2019 09:11:35 GMT-0700 (PDT)
* Source doc: https://docs.google.com/open?id=1vVcFc9Id4ZWj-D1pyJlRkf_kciUnv88ZuEPUmkbUs9E
----->


Basics:

[http://www.cs.cmu.edu/~jcarroll/15-100-s05/supps/basics/history.html](http://www.cs.cmu.edu/~jcarroll/15-100-s05/supps/basics/history.html)

Consequently, you can write a Java program (on any platform) and use the JVM compiler (called `javac`) to generate a bytecode file (bytecode files use the extension `.class`). This bytecode file can be used on any platform (that has installed Java). However, bytecode is not an executable file.  To execute a bytecode file, you actually need to invoke a Java interpreter (called `java`). Every platform has its own Java interpreter which will automatically address the  platform-specific issues that can no longer be put off. When platform-specific operations are required by the bytecode, the Java interpreter links in appropriate code specific to the platform.

To summarize how Java works (to achieve platform independence), think about the compile-link-execute cycle. In earlier programming languages, the cycle is more closely defined as "compile-link then execute". In Java, the cycle is closer to "_compile then link-execute_".

[https://stackoverflow.com/a/13422467/1594776](https://stackoverflow.com/a/13422467/1594776)

How exactly are negative numbers stored in binary. 

2’s complement of x -> ~x +1. Invert x and add 1.

So, 10 is stored as 000.....1010.

-10 is stored after applying the above formula.

Weight of MSB is negative in a signed integer. In unsigned, it’s positive.

OOPS:

**Polymorphism:**

Polymorphism is the ability of an object to take on many forms. Any Java object that can pass more than one IS-A test is considered to be polymorphic.

An overridden method is invoked at run time, no matter what data type the reference is that was used in the source code at compile time.

This behavior is referred to as virtual method invocation, and these methods are referred to as virtual methods

In **Java**, all non-static methods are by default "**virtual functions.**" Only methods marked with the **keyword final**, which cannot be overridden, along with **private methods**, which are not inherited, are **non-virtual**.

[https://www.geeksforgeeks.org/static-vs-dynamic-binding-in-java/](https://www.geeksforgeeks.org/static-vs-dynamic-binding-in-java/)



*   private, final and static members (methods and variables) use static binding while for virtual methods (In Java methods are virtual by default) binding is done during run time based upon run time object.
*   Static binding uses Type information for binding while Dynamic binding uses Objects to resolve binding.

Daemon threads:

[https://stackoverflow.com/questions/2213340/what-is-a-daemon-thread-in-java](https://stackoverflow.com/questions/2213340/what-is-a-daemon-thread-in-java)

When a Java Virtual Machine starts up, there is usually a single non-daemon thread (which typically calls the method named main of some designated class). The Java Virtual Machine continues to execute threads until either of the following occurs:



*   The exit method of class Runtime has been called and the security manager has permitted the exit operation to take place.
*   All threads that are not daemon threads have died, either by returning from the call to the run method or by throwing an exception that propagates beyond the run method.

Ways to create new thread:



*   Subclassing Thread class and overriding the run method.
*   Creating an instance of Thread class and passing a Runnable instance to it.

[https://www.javamadesoeasy.com/2015/03/reason-why-suspend-and-resume-methods.html](https://www.javamadesoeasy.com/2015/03/reason-why-suspend-and-resume-methods.html)

Blocking Queue:

[http://tutorials.jenkov.com/java-util-concurrent/blockingqueue.html](http://tutorials.jenkov.com/java-util-concurrent/blockingqueue.html)

Implementing a thread pool:

[http://tutorials.jenkov.com/java-concurrency/thread-pools.html](http://tutorials.jenkov.com/java-concurrency/thread-pools.html)

Interrupting a thread:

Interrupting a thread means stopping what it is doing before it has completed its task, effectively aborting its current operation. Whether the thread dies, waits for new tasks, or goes on to the next step depends on the application

Very good article on interrupting a thread:

[https://web.archive.org/web/20080510173455/http://articles.techrepublic.com.com/5100-10878_11-5144546.html#](https://web.archive.org/web/20080510173455/http://articles.techrepublic.com.com/5100-10878_11-5144546.html#)

Summary:

Thread.interrupt works in blocking cases (More precisely, if the thread is blocked at one of the methods _Object.wait_, _Thread.join_, or _Thread.sleep_). But if the thread is not blocked and normally executing, to stop it, you need to use a shared volatile variable which it checks periodically while executing.

If it’s blocked on I/O, in newer versions, interrupt works. In older versions, we need to manually close the socket.

Another interesting article on designing a custom executor where you can cancel tasks:

[https://dzone.com/articles/interrupting-executor-tasks](https://dzone.com/articles/interrupting-executor-tasks)

To-read: [https://docs.oracle.com/javase/6/docs/technotes/guides/concurrency/threadPrimitiveDeprecation.html](https://docs.oracle.com/javase/6/docs/technotes/guides/concurrency/threadPrimitiveDeprecation.html)

Abstract class vs Interface:

Put things in abstract classes that are essential to concrete class. Without which, it won’t be able to work.

It’s kind of soul of the concrete class. It’s not related to whether I want to implement a method or not.

Interface is a behavioral contract between two systems. It’s a behavioral addition to a class. Class can exist without it also i.e. this shouldn’t be mandatory. Whenever a concrete class implements an interface, ask this question that will it require all the methods of that interface? If no, keep dividing that interface unless the answer is yes.

**2. Can you name few design patterns used in standard JDK library?**

[Decorator design pattern](http://javarevisited.blogspot.com/2011/11/decorator-design-pattern-java-example.html) which is used in various Java IO classes, Singleton pattern which is used in `Runtime` , `Calendar` and various other classes, Factory pattern which is used along with various Immutable classes likes Boolean e.g. `Boolean.valueOf` and Observer pattern which is used in Swing and many event listener frameworks.

[https://www.journaldev.com/4098/java-heap-space-vs-stack-memory](https://www.journaldev.com/4098/java-heap-space-vs-stack-memory)

Heap memory vs stack memory.

String pool:

[https://www.journaldev.com/797/what-is-java-string-pool](https://www.journaldev.com/797/what-is-java-string-pool)

Why string is immutable:

One reason is : so that a thing such as string pool can exist. Same strings can be shared between threads as they are immutable.

Safe for multithreading

Can cache it’s hashcode. One of the most commonly used keys in hashmaps. So caching hashcode increases performance. 

Security reasons (I don’t understand this):



*   Classloader uses strings to load classes. So making them immutable makes sure some malicious class is not being loaded by intercepting the string.
*   Same for db connection etc.

Other reasons : [https://www.journaldev.com/802/string-immutable-final-java](https://www.journaldev.com/802/string-immutable-final-java)

Why primitives are not allowed in java collections.

[https://stackoverflow.com/questions/2504959/why-can-java-collections-not-directly-store-primitives-types](https://stackoverflow.com/questions/2504959/why-can-java-collections-not-directly-store-primitives-types)

Making Arraylist unmodifiable:

[http://www.javacreed.com/modifying-an-unmodifiable-list/](http://www.javacreed.com/modifying-an-unmodifiable-list/) : good enough

What unmodifiable does is just throws on the apis which try to change the list structure. 

Objects can still be modified if they are not immutable.

Also, if producer changes the list, it’ll reflect in the list given to consumer.

If we want to prevent this, create a new arraylist with all the elements, wrap it in a unmodifiable list and return.

**ConccurrentModificationException:**

Fail-fast iterators throw this if it detects that a collection has been modified during the iteration. Modified by other means, such as directly using the collection’s remove method.

We can use iterator’s remove method so that it’s aware of the removal.

Other way is using classical for loop to remove so that we are not dealing with iterators all together.

Arraylist, LinkedList etc return fail-fast iterators.

[https://javaconceptoftheday.com/fail-fast-and-fail-safe-iterators-in-java-with-examples/](https://javaconceptoftheday.com/fail-fast-and-fail-safe-iterators-in-java-with-examples/)

**Volatile:**

Solves the **Visibility problem. guarantees visibility of changes to variables across threads**



*   Don’t cache anything in thread-local cache. Directly read/write from the main memory
*   Access to this variable acts as if it’s enclosed in a synchronized block.

[http://tutorials.jenkov.com/java-concurrency/volatile.html](http://tutorials.jenkov.com/java-concurrency/volatile.html) : very good.

All variables present in cache before writing a volatile variable are written to main memory at that time.

All variables read after reading the volatile variable are read from main memory.

Also, java guarantees that instruction reordering won’t affect this.

Still, volatile doesn’t solve all the problems. See the above mentioned article

**Difference between synchronized and concurrent collections:**

[https://javarevisited.blogspot.com/2016/05/what-is-difference-between-synchronized.html](https://javarevisited.blogspot.com/2016/05/what-is-difference-between-synchronized.html)

Synchronized collections apply collection level lock, while concurrent collections such as concurrent hashmap divides the collection into certain segments and applies segment level locks. So that other threads can explore the other segments.

Preventing singleton class from reflection, serialization and cloning

[https://www.geeksforgeeks.org/prevent-singleton-pattern-reflection-serialization-cloning/](https://www.geeksforgeeks.org/prevent-singleton-pattern-reflection-serialization-cloning/)

[https://www.geeksforgeeks.org/jvm-works-jvm-architecture/](https://www.geeksforgeeks.org/jvm-works-jvm-architecture/)

[https://dzone.com/articles/jvm-architecture-explained](https://dzone.com/articles/jvm-architecture-explained)

[https://www.geeksforgeeks.org/object-class-in-java/](https://www.geeksforgeeks.org/object-class-in-java/)

Object class: root of inheritance hierarchy

Hashcode doesn’t directly returns the address. It converts the address into a unique integer.

[https://www.programiz.com/java-programming/nested-inner-class](https://www.programiz.com/java-programming/nested-inner-class)



*   Java treats inner class as a regular member of a class. They are just like methods and variables declared inside a class.
*   Since, inner class are members of outer class, you can apply any access modifiers like private, protected to your inner class which is not possible in normal classes.
*   Since Nested class is a member of its enclosing class Outer, you can use `. (dot)`notation to access Nested class and its members.
*   Using nested class will make your code more readable and provide better encapsulation.
*   Non-static nested classes (inner classes) have access to other members of the outer/enclosing class, even if they are declared private.

**Concurrency:**

Benefits of multithreading:



*   Better resource utilization
*   More responsive programs
*   Simpler program design, in case we have to do the same job with each thread

Costs:



*   Shared data, complex to handle
*   Context switching
*   More resource consumption.

Concurrency models:



*   Parallel workers
    *   Shared state
    *   Forced to have stateless workers
    *   Each worker thread: end to end job
*   Assembly line
    *   Each thread performs one specific part of the job.
    *   No shared state, there each thread can cache it’s data in-memory too, therefore, stateful workers
    *   Has better hardware conformity as cpu cache also comes into play in this.
    *   Disadvantages: code is not that readable as it’s spread across classes.
    *   Similar to microservices model

Unfortunately linked lists don't perform very well on modern hardware. Each element in the list is a separate object, and these objects can be spread out all over the computer's memory. Modern CPUs are much faster at accessing data sequentially, so on modern hardware you will get a lot higher performance out of a list implemented on top of an array. An array stores data sequentially. The CPU caches can load bigger chunks of the array into the cache at a time, and have the CPU access the data directly in the CPU cache once loaded. This is not really possible with a linked list where elements are scattered all over the RAM

Concurrency vs parallelism :

[http://tutorials.jenkov.com/java-concurrency/concurrency-vs-parallelism.html](http://tutorials.jenkov.com/java-concurrency/concurrency-vs-parallelism.html)

Very imp.

[https://stackoverflow.com/questions/1050222/what-is-the-difference-between-concurrency-and-parallelism](https://stackoverflow.com/questions/1050222/what-is-the-difference-between-concurrency-and-parallelism)

Very good article on thread interruption : 

[https://web.archive.org/web/20080510173455/http://articles.techrepublic.com.com/5100-10878_11-5144546.html#](https://web.archive.org/web/20080510173455/http://articles.techrepublic.com.com/5100-10878_11-5144546.html#)

Thread safe code:

If a resource are created, used and disposed within the same thread

AND

Never escapes the control of this thread.

Then usage of that control is thread safe.

It is important to distinguish whether the object controlled by the thread IS the resource OR is a mere reference to the resource.

[http://tutorials.jenkov.com/java-concurrency/java-memory-model.html](http://tutorials.jenkov.com/java-concurrency/java-memory-model.html) : Wow !



*   A synchronized block guarantees that only one thread can enter a given critical section of the code at any given time. Synchronized blocks also guarantee that all variables accessed inside the synchronized block will be read in from main memory, and when the thread exits the synchronized block, all updated variables will be flushed back to main memory again, regardless of whether the variable is declared volatile or not
*   The volatile keyword can make sure that a given variable is read directly from main memory, and always written back to main memory when updated.

Volatile is enough only if multiple threads are not writing to the shared variable.

If one if writing and all others are reading, it’s fine.

In fact, multiple threads could even be writing to a shared volatile variable, and still have the correct value stored in main memory, if the new value written to the variable does not depend on its previous value. In other words, if a thread writing a value to the shared volatile variable does not first need to read its value to figure out its next value.

**Thread signalling:**



*   Shared object: But each thread needs access to the shared object
*   Busy waiting : threads keeps running a loop till a shared signal is set. This is cpu intensive
*   Wait(), notify() signals 
    *   the calling thread must call wait() or notify() from inside a synchronized block. Once a thread calls wait() it releases the lock it holds on the monitor object. This allows other threads to call wait() or notify() too, since these methods must be called from inside a synchronized block.
    *   **Don't call wait() on constant String's or global objects**

        the JVM/Compiler internally translates constant strings into the same object


**Deadlock prevention:**



*   Lock ordering
*   Lock timeout
*   Deadlock detection, using managing the lock allocation ourself

Thread.join:

[https://www.geeksforgeeks.org/joining-threads-in-java/](https://www.geeksforgeeks.org/joining-threads-in-java/)

Enums:

[https://howtodoinjava.com/java/enum/guide-for-understanding-enum-in-java/](https://howtodoinjava.com/java/enum/guide-for-understanding-enum-in-java/)

[https://codepumpkin.com/breaking-singleton-using-reflection-and-enum-singleton/](https://codepumpkin.com/breaking-singleton-using-reflection-and-enum-singleton/)

Preventing singleton from reflection and where does enums come into picture.

We can check the field nullability in constructor but the attacker can set the field to null after changing it from private to public.

For this, we can make the field final. But then, this only works with eager initialization.


<!-- Docs to Markdown version 1.0β17 -->

