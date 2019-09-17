**ART/Dalvik**

ART as the runtime executes the Dalvik Executable format and Dex bytecode specification. ART and Dalvik are compatible runtimes running Dex bytecode, so apps developed for Dalvik should work when running with ART.

Interesting:

JIT vs AOT: [https://softwareengineering.stackexchange.com/questions/274640/why-is-android-runtimes-aot-compilation-more-performant-than-dalviks-jit](https://softwareengineering.stackexchange.com/questions/274640/why-is-android-runtimes-aot-compilation-more-performant-than-dalviks-jit)

At install time, ART compiles apps using the on-device **dex2oat** tool. This utility accepts [DEX](https://source.android.com/devices/tech/dalvik/dex-format.html) files as input and generates a compiled app executable for the target device

You can reference a very large number of methods in a DEX file, but you can only invoke the first 65536, because that's all the room you have in the method invocation instruction.

Dalvik bytecode has a fundamental limitation which allows to invoke a maximum of 2^16 (65536) methods (per dex file).

[https://blog.osom.info/2014/10/multi-dex-to-rescue-from-infamous-65536.html](https://blog.osom.info/2014/10/multi-dex-to-rescue-from-infamous-65536.html)

[https://android-developers.googleblog.com/2011/07/custom-class-loading-in-dalvik.html](https://android-developers.googleblog.com/2011/07/custom-class-loading-in-dalvik.html)

[http://www.marioalmeida.eu/2015/01/27/how-to-easy-way-load-apk-classes-using-dexclassloader/](http://www.marioalmeida.eu/2015/01/27/how-to-easy-way-load-apk-classes-using-dexclassloader/)

How notification are shown in other process:

[https://stackoverflow.com/questions/15530293/can-noticationmanager-notify-be-called-from-a-worker-thread](https://stackoverflow.com/questions/15530293/can-noticationmanager-notify-be-called-from-a-worker-thread)

Multiple threads, concurrency:

Executor

* An object that executes submitted Runnable  tasks. This interface provides a way of decoupling task submission from the mechanics of how each task will be run, including details of thread use, scheduling, etc

Group your ThreadPools (for network, disk I/O, and computation). These types of work are generally independent and shouldn’t block each other.

webview#evaluateJavascript :

*This method must be called on the UI thread and the callback will be made on the UI thread.*

#addJavascriptInterface

JavaScript interacts with Java object on a private, background thread of this WebView. Care is therefore required to maintain thread safety

The Java object's fields are not accessible

We can make a generic Room DAO which:

* Takes database name, table name and sql query as input

* Returns datasource

Extend: **LimitOffsetDataSource** and implement the convertRows method.

Localization:

[https://developer.android.com/guide/topics/resources/multilingual-support](https://developer.android.com/guide/topics/resources/multilingual-support)

This example also shows why you should store French strings in fr rather than fr_FR for Android 7.0 or higher. Here the course of action is to match the closest parent dialect, making resolution faster and more predictable.

Supporting different screen densities:

[https://stackoverflow.com/questions/5518852/android-what-is-the-difference-between-resolution-and-density](https://stackoverflow.com/questions/5518852/android-what-is-the-difference-between-resolution-and-density)

[https://www.captechconsulting.com/blogs/understanding-density-independence-in-android](https://www.captechconsulting.com/blogs/understanding-density-independence-in-android)

**Image Loading:**

**In notes.**

**Memory:**

**Dominator tree, shallow vs retained memory:**

**[https://help.eclipse.org/oxygen/index.jsp?topic=%2Forg.eclipse.mat.ui.help%2Fconcepts%2Fdominatortree.htm**l](https://help.eclipse.org/oxygen/index.jsp?topic=%2Forg.eclipse.mat.ui.help%2Fconcepts%2Fdominatortree.html)

**OKhttp caching:**

[https://medium.com/@I_Love_Coding/how-does-okhttp-cache-works-851d37dd29cd](https://medium.com/@I_Love_Coding/how-does-okhttp-cache-works-851d37dd29cd)

[https://android.jlelse.eu/reducing-your-networking-footprint-with-okhttp-etags-and-if-modified-since-b598b8dd81a1](https://android.jlelse.eu/reducing-your-networking-footprint-with-okhttp-etags-and-if-modified-since-b598b8dd81a1) : This is much better.

Two methods : 

Etag header.

Last-Modified.

Constraint Layout:

[https://android-developers.googleblog.com/2017/08/understanding-performance-benefits-of.html#bookmark=kix.qjly41rrtsa9](https://android-developers.googleblog.com/2017/08/understanding-performance-benefits-of.html#bookmark=kix.qjly41rrtsa9)

[https://medium.com/androiddevelopers/building-interfaces-with-constraintlayout-3958fa38a9f7](https://medium.com/androiddevelopers/building-interfaces-with-constraintlayout-3958fa38a9f7)

Multithreading in SQLite:

[http://touchlabblog.tumblr.com/post/24474398246/android-sqlite-locking](http://touchlabblog.tumblr.com/post/24474398246/android-sqlite-locking)

[http://touchlabblog.tumblr.com/post/32793099735/training-sqlite](http://touchlabblog.tumblr.com/post/32793099735/training-sqlite)

RecyclerView:

[https://proandroiddev.com/recyclerview-pro-tips-part-1-8a291594bafc](https://proandroiddev.com/recyclerview-pro-tips-part-1-8a291594bafc)

[https://academy.realm.io/posts/360andev-yigit-boyar-pro-recyclerview-android-ui-java/](https://academy.realm.io/posts/360andev-yigit-boyar-pro-recyclerview-android-ui-java/)

[https://android.jlelse.eu/anatomy-of-recyclerview-part-1-a-search-for-a-viewholder-404ba3453714](https://android.jlelse.eu/anatomy-of-recyclerview-part-1-a-search-for-a-viewholder-404ba3453714) : very good article on viewholder cache and pool works.

Clean architecture:

[https://proandroiddev.com/a-guided-tour-inside-a-clean-architecture-code-base-48bb5cc9fc97](https://proandroiddev.com/a-guided-tour-inside-a-clean-architecture-code-base-48bb5cc9fc97) 

Very good article

How android boots up (deep dive) :

[https://proandroiddev.com/how-android-boot-up-9864376d911c](https://proandroiddev.com/how-android-boot-up-9864376d911c)

Lifecycle:

In the [onStop()](https://developer.android.com/reference/android/app/Activity.html#onStop()) method, the app should release or adjust resources that are not needed while the app is not visible to the user. For example, your app might pause animations or switch from fine-grained to coarse-grained location updates. Using [onStop()](https://developer.android.com/reference/android/app/Activity.html#onStop()) instead of [onPause()](https://developer.android.com/reference/android/app/Activity.html#onPause()) ensures that UI-related work continues, even when the user is viewing your activity in multi-window mode.

When your activity enters the Stopped state, the [Activity](https://developer.android.com/reference/android/app/Activity.html) object is kept resident in memory: It maintains all state and member information, but is not attached to the window manager.

Discussion around why android destroys the activity on rotation.

[https://www.reddit.com/r/androiddev/comments/2xgu06/is_there_a_good_reason_why_configuration_changes/](https://www.reddit.com/r/androiddev/comments/2xgu06/is_there_a_good_reason_why_configuration_changes/)

Android has a system to destroy and recreate your Activities in order to manage limited device resources. You *must* handle this correctly in your app. Instead of creating a whole new mechanism for configuration changes, they opted instead to reuse the one they already had. Since you already must assume your Activity can be destroyed and recreated at any time, there *should* be no extra implementation cost because of this decision.

[https://developer.android.com/topic/libraries/architecture/saving-states.html](https://developer.android.com/topic/libraries/architecture/saving-states.html): V Imp

Using a combination of local storage, instance state bundle and viewmodel.

Song example.

**Fragments:**

When you add a fragment as a part of your activity layout, it lives in a [ViewGroup](https://developer.android.com/reference/android/view/ViewGroup.html) inside the activity's view hierarchy and the fragment defines its own view layout.

You should design each fragment as a modular and reusable activity component.

If you don't call [addToBackStack()](https://developer.android.com/reference/androidx/fragment/app/FragmentTransaction.html#addToBackStack(java.lang.String)) when you perform a transaction that removes a fragment, then that fragment is destroyed when the transaction is committed and the user cannot navigate back to it. Whereas, if you do call [addToBackStack()](https://developer.android.com/reference/androidx/fragment/app/FragmentTransaction.html#addToBackStack(java.lang.String)) when removing a fragment, then the fragment is *stopped* and is later resumed if the user navigates back.

Calling [commit()](https://developer.android.com/reference/androidx/fragment/app/FragmentTransaction.html#commit()) doesn't perform the transaction immediately. Rather, it schedules it to run on the activity's UI thread (the "main" thread) as soon as the thread is able to do so. If necessary, however, you may call [executePendingTransactions()](https://developer.android.com/reference/androidx/fragment/app/FragmentManager.html#executePendingTransactions()) from your UI thread to immediately execute transactions submitted by [commit()](https://developer.android.com/reference/androidx/fragment/app/FragmentTransaction.html#commit())

 To share data, create a shared ViewModel, as outlined in the Share data between fragments section in the [ViewModel guide](https://developer.android.com/topic/libraries/architecture/viewmodel.html). If you need to propagate events that cannot be handled with a ViewModel, you can instead define a callback interface inside the fragment and require that the host activity implement it

**Design Pattern:**

[https://www.raywenderlich.com/470-common-design-patterns-for-android-with-kotlin](https://www.raywenderlich.com/470-common-design-patterns-for-android-with-kotlin)

* Creational

    * Builder

        * Alert Dialog

    * DI

    * Singleton

* Structural

    * Adapter

        * RecyclerView adapter (b/w business classes and viewholders)

    * Facade

        * Retrofit

* Behavioral

    * Observer

    * Pubsub

        * Might compromises readability though

    * MVC

        * Controller

            * glue between M and V

            * Processes user input, modifies models and updates views

        * Benefits:

            * Re-using same models across multiple screens

            * Shifting a view widget between screens

    * MVVM

        * ViewModel

            * Glue between M and V

            * Binds the V with M, so V automatically updates when M is updated. Similarly, M is updated when user interacts with V

Comparing MVC, MVP and MVVM:

[https://academy.realm.io/posts/eric-maxwell-mvc-mvp-and-mvvm-on-android/](https://academy.realm.io/posts/eric-maxwell-mvc-mvp-and-mvvm-on-android/) : very good post.

MVC is definitely bad. 

MVVM is more declarative and has less boilerplate code (specially if I go with data binding). 

Good intro to RX:

[https://jasonroell.com/2016/10/21/rxjava-a-paradigm-shift/](https://jasonroell.com/2016/10/21/rxjava-a-paradigm-shift/)

[http://reactivex.io/intro.html](http://reactivex.io/intro.html) : very imp.

[https://ejf.io/dev_blog/async_java_compare/](https://ejf.io/dev_blog/async_java_compare/)

[https://developer.android.com/guide/components/broadcasts#restrict-broadcasts-permissions](https://developer.android.com/guide/components/broadcasts#restrict-broadcasts-permissions)

Interesting  ^. 

Image loading libraries:

* Glide automatically loads the correct size in the memory, instead of loading full size image. Picasso doesn’t do it, it loads the complete size in memory

* Glide caches that size only, picasso caches the complete size.

* Glide supports animations, picasso doesn’t

* Glide adapts with activity/fragment lifecycle. Pauses and resume downloads accordingly.

[https://medium.com/@anitaa_1990/how-to-update-an-activity-from-background-service-or-a-broadcastreceiver-6dabdb5cef74](https://medium.com/@anitaa_1990/how-to-update-an-activity-from-background-service-or-a-broadcastreceiver-6dabdb5cef74)

interesting.
