# Introduction

Source codes of book: Java Concurrency In Practice(2011, Brain Goetz etc. jcip for short.), rebuild from [https://jcip.net/](https://jcip.net/) with [maven](https://maven.apache.org/).

# Modules of this project:

* jcip-annotations: Source codes for annotations.
* jcip-examples: Source codes for all examples.

# Example Codes List

## Introduction

* 1.1 Non-thread-safe sequence generator: [UnsafeSequence.java](https://jcip.net/listings/UnsafeSequence.java)
* 1.2 Thread-safe sequence generator: [net.jcip.examples.Sequence.java](https://jcip.net/listings/Sequence.java)

## Thread Safety

* 2.1 A stateless servlet: [net.jcip.examples.StatelessFactorizer.java](https://jcip.net/listings/StatelessFactorizer.java)
* 2.2 Servlet that counts requests without the necessary synchronization: [net.jcip.examples.UnsafeCountingFactorizer.java](https://jcip.net/listings/UnsafeCountingFactorizer.java)
* 2.3 Race condition in lazy initialization: [net.jcip.examples.LazyInitRace.java](https://jcip.net/listings/LazyInitRace.java)
* 2.4 Servlet that counts requests using AtomicLong: [net.jcip.examples.CountingFactorizer.java](https://jcip.net/listings/CountingFactorizer.java)
* 2.5 Servlet that attempts to cache its last result without adequate atomicity: [net.jcip.examples.UnsafeCachingFactorizer.java](https://jcip.net/listings/UnsafeCachingFactorizer.java)
* 2.6 Servlet that caches last result, but with unnacceptably poor concurrency: [net.jcip.examples.SynchronizedFactorizer.java](https://jcip.net/listings/SynchronizedFactorizer.java)
* 2.7 Code that would deadlock if intrinsic locks were not reentrant: [net.jcip.examples.NonReentrantDeadlock.java](https://jcip.net/listings/NonReentrantDeadlock.java)
* 2.8 Servlet that caches its last request and result: [net.jcip.examples.CachedFactorizer.java](https://jcip.net/listings/CachedFactorizer.java)

## Sharing Objects

* 3.1 Sharing variables without synchronization: [net.jcip.examples.NoVisibility.java](https://jcip.net/listings/NoVisibility.java)
* 3.2 Non-thread-safe mutable integer holder: [net.jcip.examples.MutableInteger.java](https://jcip.net/listings/MutableInteger.java)
* 3.3 Thread-safe mutable integer holder: [net.jcip.examples.SynchronizedInteger.java](https://jcip.net/listings/SynchronizedInteger.java)
* 3.4 Counting sheep: [net.jcip.examples.CountingSheep.java](https://jcip.net/listings/CountingSheep.java)
* 3.5 Publishing an object: [net.jcip.examples.Secrets.java](https://jcip.net/listings/Secrets.java)
* 3.6 Allowing internal mutable state to escape: [net.jcip.examples.UnsafeStates.java](https://jcip.net/listings/UnsafeStates.java)
* 3.7 Implicitly allowing the this reference to escape: [net.jcip.examples.ThisEscape.java](https://jcip.net/listings/ThisEscape.java)
* 3.8 Using a factory method to prevent the this reference from escaping during construction: [net.jcip.examples.SafeListener.java](https://jcip.net/listings/SafeListener.java)
* 3.9 Thread confinement of local primitive and reference variables: [net.jcip.examples.Animals.java](https://jcip.net/listings/Animals.java)
* 3.10 Using ThreadLocal to ensure thread confinement: [net.jcip.examples.ConnectionDispenser.java](https://jcip.net/listings/ConnectionDispenser.java)
* 3.11 Immutable class built out of mutable underlying objects: [net.jcip.examples.ThreeStooges.java](https://jcip.net/listings/ThreeStooges.java)
* 3.12 Immutable holder for caching a number and its factors: [net.jcip.examples.OneValueCache.java](https://jcip.net/listings/OneValueCache.java)
* 3.13 Caching the last result using a volatile reference to an immutable holder object: [net.jcip.examples.VolatileCachedFactorizer.java](https://jcip.net/listings/VolatileCachedFactorizer.java)
* 3.14 Publishing an object without adequate synchronization: [net.jcip.examples.StuffIntoPublic.java](https://jcip.net/listings/StuffIntoPublic.java)
* 3.15 Class at risk of failure if not properly published: [net.jcip.examples.Holder.java](https://jcip.net/listings/Holder.java)

## Composing Objects

* 4.1 Simple thread-safe counter using the Java monitor pattern: [net.jcip.examples.Counter.java](https://jcip.net/listings/Counter.java)
* 4.2 Using confinement to ensure thread safety: [net.jcip.examples.PersonSet.java](https://jcip.net/listings/PersonSet.java)
* 4.3 Guarding state with a private lock: [net.jcip.examples.PrivateLock.java](https://jcip.net/listings/PrivateLock.java)
* 4.4 Monitor-based vehicle tracker implementation: [net.jcip.examples.MonitorVehicleTracker.java](https://jcip.net/listings/MonitorVehicleTracker.java)
* 4.5 Mutable point class similar to java.awt.Point: [net.jcip.examples.MutablePoint.java](https://jcip.net/listings/MutablePoint.java)
* 4.6 Immutable Point class used by DelegatingVehicleTracker: [net.jcip.examples.Point.java](https://jcip.net/listings/Point.java)
* 4.7 Delegating thread safety to a ConcurrentHashMap: [net.jcip.examples.DelegatingVehicleTracker.java](https://jcip.net/listings/DelegatingVehicleTracker.java)
* 4.8 Returning a static copy of the location set instead of a 'live' one: [net.jcip.examples.DelegatingVehicleTracker.java](https://jcip.net/listings/DelegatingVehicleTracker.java)
* 4.9 Delegating thread safety to multiple underlying state variables: [net.jcip.examples.VisualComponent.java](https://jcip.net/listings/VisualComponent.java)
* 4.10 Number range class that does not sufficiently protect its invariants: [net.jcip.examples.NumberRange.java](https://jcip.net/listings/NumberRange.java)
* 4.11 Thread-safe mutable point class: [net.jcip.examples.SafePoint.java](https://jcip.net/listings/SafePoint.java)
* 4.12 Vehicle tracker that safely publishes underlying state: [net.jcip.examples.PublishingVehicleTracker.java](https://jcip.net/listings/PublishingVehicleTracker.java)
* 4.13 Extending Vector to have a put-if-absent method: [net.jcip.examples.BetterVector.java](https://jcip.net/listings/BetterVector.java)
* 4.14 Non-thread-safe attempt to implement put-if-absent: [net.jcip.examples.ListHelpers.java](https://jcip.net/listings/ListHelpers.java)
* 4.15 Implementing put-if-absent with client-side locking: [net.jcip.examples.ListHelpers.java](https://jcip.net/listings/ListHelpers.java)
* 4.16 Implementing put-if-absent using composition: [net.jcip.examples.ImprovedList.java](https://jcip.net/listings/ImprovedList.java)

## Building Blocks

* 5.1 Compound actions on a Vector that may produce confusing results: [net.jcip.examples.UnsafeVectorHelpers.java](https://jcip.net/listings/UnsafeVectorHelpers.java)
* 5.2 Compound actions on Vector using client-side locking: [net.jcip.examples.SafeVectorHelpers.java](https://jcip.net/listings/SafeVectorHelpers.java)
* 5.3 Iteration that may throw ArrayIndexOutOfBoundsException. (fragment) 
* 5.4 Iteration with client-side locking. (fragment)
* 5.5 Iterating a List with an Iterator. (fragment)
* 5.6 Iteration hidden within string concatenation: [net.jcip.examples.HiddenIterator.java](https://jcip.net/listings/HiddenIterator.java)
* 5.7 [ConcurrentMap interface](https://jcip.net/http://java.sun.com/j2se/1.5.0/docs/api/java/util/concurrent/ConcurrentMap.html##method_summary). (external link to Javadoc)
* 5.8 Producer and consumer tasks in a desktop search application: [net.jcip.examples.ProducerConsumer.java](https://jcip.net/listings/ProducerConsumer.java)
* 5.9 Starting the desktop search: [net.jcip.examples.ProducerConsumer.java](https://jcip.net/listings/ProducerConsumer.java)
* 5.10 Restoring the interrupted status so as not to swallow the interrupt: [net.jcip.examples.TaskRunnable.java](https://jcip.net/listings/TaskRunnable.java)
* 5.11 Using CountDownLatch for starting and stopping threads in timing tests: [net.jcip.examples.TestHarness.java](https://jcip.net/listings/TestHarness.java)
* 5.12 Using FutureTask to preload data that is needed later: [net.jcip.examples.Preloader.java](https://jcip.net/listings/Preloader.java)
* 5.13 Coercing an unchecked Throwable to a RuntimeException: [net.jcip.examples.LaunderThrowable.java](https://jcip.net/listings/LaunderThrowable.java)
* 5.14 Using Semaphore to bound a collection: [net.jcip.examples.BoundedHashSet.java](https://jcip.net/listings/BoundedHashSet.java)
* 5.15 Coordinating computation in a cellular automaton with CyclicBarrier: [net.jcip.examples.CellularAutomata.java](https://jcip.net/listings/CellularAutomata.java)
* 5.16 Initial cache attempt using HashMap and synchronization: [net.jcip.examples.Memoizer1.java](https://jcip.net/listings/Memoizer1.java)
* 5.17 Replacing HashMap with ConcurrentHashMap: [net.jcip.examples.Memoizer2.java](https://jcip.net/listings/Memoizer2.java)
* 5.18 Memoizing wrapper using FutureTask: [net.jcip.examples.Memoizer2.java](https://jcip.net/listings/Memoizer2.java)
* 5.19 Final implementation of Memoizer: [net.jcip.examples.Memoizer.java](https://jcip.net/listings/Memoizer.java)
* 5.20 Factorizing servlet that caches results using Memoizer: [net.jcip.examples.Factorizer.java](https://jcip.net/listings/Factorizer.java)

## Task Execution

* 6.1 Sequential web server: [net.jcip.examples.SingleThreadWebServer.java](https://jcip.net/listings/SingleThreadWebServer.java)
* 6.2 Web server that starts a new thread for each request: [net.jcip.examples.ThreadPerTaskWebServer.java](https://jcip.net/listings/ThreadPerTaskWebServer.java)
* 6.3 [Executor interface](https://jcip.net/http://java.sun.com/j2se/1.5.0/docs/api/java/util/concurrent/Executor.html##method_summary). (external link to Javadoc)
* 6.4 Web server using a thread pool: [net.jcip.examples.TaskExecutionWebServer.java](https://jcip.net/listings/TaskExecutionWebServer.java)
* 6.5 Executor that starts a new thread for each task: [net.jcip.examples.ThreadPerTaskExecutor.java](https://jcip.net/listings/ThreadPerTaskExecutor.java)
* 6.6 Executor that executes tasks synchronously in the calling thread: [net.jcip.examples.WithinThreadExecutor.java](https://jcip.net/listings/WithinThreadExecutor.java)
* 6.7 [Lifecycle methods in ExecutorService](http://java.sun.com/j2se/1.5.0/docs/api/java/util/concurrent/ExecutorService.html##method_summary). (external link to Javadoc, shows all methods, not just lifecycle methods)
* 6.8 Web server with shutdown support: [net.jcip.examples.LifecycleWebServer.java](https://jcip.net/listings/LifecycleWebServer.java)
* 6.9 Class illustrating confusing Timer behavior: [net.jcip.examples.OutOfTime.java](https://jcip.net/listings/OutOfTime.java)
* 6.10 Rendering page elements sequentially: [net.jcip.examples.SingleThreadRenderer.java](https://jcip.net/listings/SingleThreadRenderer.java)
* 6.11 [Callable](https://jcip.net/http://java.sun.com/j2se/1.5.0/docs/api/java/util/concurrent/Callable.html##method_summary) and [Future](https://jcip.net/http://java.sun.com/j2se/1.5.0/docs/api/java/util/concurrent/Future.html##method_summary) interfaces. (external links to Javadoc)
* 6.12 Default implementation of newTaskFor in ThreadPoolExecutor. (See JDK source)
* 6.13 Waiting for image download with Future: [net.jcip.examples.FutureRenderer.java](https://jcip.net/listings/FutureRenderer.java)
* 6.14 QueueingFuture class used by ExecutorCompletionService. (See JDK source)
* 6.15 Using CompletionService to render page elements as they become available: [net.jcip.examples.Renderer.java](https://jcip.net/listings/Renderer.java)
* 6.16 Fetching an advertisement with a time budget: [net.jcip.examples.RenderWithTimeBudget.java](https://jcip.net/listings/RenderWithTimeBudget.java)
* 6.17 Requesting travel quotes under a time budget: [net.jcip.examples.TimeBudget.java](https://jcip.net/listings/TimeBudget.java)

## Cancellation and Shutdown

* 7.1 Using a volatile field to hold cancellation state: [net.jcip.examples.PrimeGenerator.java](https://jcip.net/listings/PrimeGenerator.java)
* 7.2 Generating a second's worth of prime numbers: [net.jcip.examples.PrimeGenerator.java](https://jcip.net/listings/PrimeGenerator.java)
* 7.3 Unreliable cancellation that can leave producers stuck in a blocking operation: [net.jcip.examples.BrokenPrimeProducer.java](https://jcip.net/listings/BrokenPrimeProducer.java)
* 7.4 [Interruption methods in Thread](https://jcip.net/http://java.sun.com/j2se/1.5.0/docs/api/java/lang/Thread.html##method_summary). (external link to Javadoc, shows all Thread methods, not just interruption-related)
* 7.5 Using interruption for cancellation: [net.jcip.examples.PrimeProducer.java](https://jcip.net/listings/PrimeProducer.java)
* 7.6 Propagating InterruptedException to callers. (fragment)
* 7.7 Noncancelable task that restores interruption before exit: [net.jcip.examples.NoncancelableTask.java](https://jcip.net/listings/NoncancelableTask.java)
* 7.8 Scheduling an interrupt on a borrowed thread: [net.jcip.examples.TimedRun1.java](https://jcip.net/listings/TimedRun1.java)
* 7.9 Interrupting a task in a dedicated thread: [net.jcip.examples.TimedRun2.java](https://jcip.net/listings/TimedRun2.java)
* 7.10 Cancelling a task using Future: [net.jcip.examples.TimedRun.java](https://jcip.net/listings/TimedRun.java)
* 7.11 Encapsulating nonstandard cancellation in a Thread by overriding interrupt: [net.jcip.examples.ReaderThread.java](https://jcip.net/listings/ReaderThread.java)
* 7.12 Encapsulating nonstandard cancellation in a task with newTaskFor: [net.jcip.examples.SocketUsingTask.java](https://jcip.net/listings/SocketUsingTask.java)
* 7.13 Producer-consumer logging service with no shutdown support: [net.jcip.examples.LogWriter.java](https://jcip.net/listings/LogWriter.java)
* 7.14 Unreliable way to add shutdown support to the logging service. (fragment)
* 7.15 Adding reliable cancellation to LogWriter: [net.jcip.examples.LogService.java](https://jcip.net/listings/LogService.java)
* 7.16 Logging service that uses an ExecutorService.
* 7.17 Shutdown with poison pill: [net.jcip.examples.IndexingService.java](https://jcip.net/listings/IndexingService.java)
* 7.18 Producer thread for IndexingService: [net.jcip.examples.IndexingService.java](https://jcip.net/listings/IndexingService.java)
* 7.19 Consumer thread for IndexingService: [net.jcip.examples.IndexingService.java](https://jcip.net/listings/IndexingService.java)
* 7.20 Using a private Executor whose lifetime is bounded by a method call: [net.jcip.examples.CheckForMail.java](https://jcip.net/listings/CheckForMail.java)
* 7.21 ExecutorService that keeps track of cancelled tasks after shutdown: [net.jcip.examples.TrackingExecutor.java](https://jcip.net/listings/TrackingExecutor.java)
* 7.22 Using TrackingExecutorService to save unfinished tasks for later execution: [net.jcip.examples.WebCrawler.java](https://jcip.net/listings/WebCrawler.java)
* 7.23 Typical thread-pool worker thread structure. (fragment)
* 7.24 [UncaughtExceptionHandler interface](https://jcip.net/http://java.sun.com/j2se/1.5.0/docs/api/java/lang/Thread.UncaughtExceptionHandler.html##method_summary). (external link to Javadoc)
* 7.25 UncaughtExceptionHandler that logs the exception: [net.jcip.examples.UEHLogger.java](https://jcip.net/listings/UEHLogger.java)
* 7.26 Registering a shutdown hook to stop the logging service. (fragment)

## Applying Thread Pools

* 8.1 Task that deadlocks in a single-threaded Executor: [net.jcip.examples.ThreadDeadlock.java](https://jcip.net/listings/ThreadDeadlock.java)
* 8.2 [General constructor for ThreadPoolExecutor](https://jcip.net/http://java.sun.com/j2se/1.5.0/docs/api/java/util/concurrent/ThreadPoolExecutor.html##ThreadPoolExecutor(int,%20int,%20long,%20java.util.concurrent.TimeUnit,%20java.util.concurrent.BlockingQueue,%20java.util.concurrent.ThreadFactory,%20java.util.concurrent.RejectedExecutionHandler)). (external link to Javadoc)
* 8.3 Creating a fixed-sized thread pool with a bounded queue and the caller-runs saturation policy. (fragment)
* 8.4 Using a Semaphore to throttle task submission: [net.jcip.examples.BoundedExecutor.java](https://jcip.net/listings/BoundedExecutor.java)
* 8.5 [ThreadFactory interface](https://jcip.net/http://java.sun.com/j2se/1.5.0/docs/api/java/util/concurrent/ThreadFactory.html##method_summary). (external link to Javadoc)
* 8.6 Custom thread factory: [net.jcip.examples.MyThreadFactory.java](https://jcip.net/listings/MyThreadFactory.java)
* 8.7 Custom thread base class: [net.jcip.examples.MyAppThread.java](https://jcip.net/listings/MyAppThread.java)
* 8.8 Modifying an Executor created with the standard factories. (fragment)
* 8.9 Thread pool extended with logging and timing: [net.jcip.examples.TimingThreadPool.java](https://jcip.net/listings/TimingThreadPool.java)
* 8.10 Transforming sequential execution into parallel execution: [net.jcip.examples.TransformingSequential.java](https://jcip.net/listings/TransformingSequential.java)
* 8.11 Transforming sequential tail-recursion into parallelized recursion: [net.jcip.examples.TransformingSequential.java](https://jcip.net/listings/TransformingSequential.java)
* 8.12 Waiting for results to be calculated in parallel: [net.jcip.examples.TransformingSequential.java](https://jcip.net/listings/TransformingSequential.java)
* 8.13 Abstraction for puzzles like the 'sliding blocks puzzle': [net.jcip.examples.Puzzle.java](https://jcip.net/listings/Puzzle.java)
* 8.14 Link node for the puzzle solver framework: [net.jcip.examples.PuzzleNode.java](https://jcip.net/listings/PuzzleNode.java)
* 8.15 Sequential puzzle solver: [net.jcip.examples.SequentialPuzzleSolver.java](https://jcip.net/listings/SequentialPuzzleSolver.java)
* 8.16 Concurrent version of puzzle solver: [net.jcip.examples.ConcurrentPuzzleSolver.java](https://jcip.net/listings/ConcurrentPuzzleSolver.java)
* 8.17 Result-bearing latch used by ConcurrentPuzzleSolver: [net.jcip.examples.ValueLatch.java](https://jcip.net/listings/ValueLatch.java)
* 8.18 Solver that recognizes when no solution exists: [net.jcip.examples.PuzzleSolver.java](https://jcip.net/listings/PuzzleSolver.java)

## GUI Applications

* 9.1 Implementing SwingUtilities using an Executor: [net.jcip.examples.SwingUtilities.java](https://jcip.net/listings/SwingUtilities.java)
* 9.2 Executor built atop SwingUtilities: [net.jcip.examples.GuiExecutor.java](https://jcip.net/listings/GuiExecutor.java)
* 9.3 Simple event listener. (fragment)
* 9.4 Binding a long-running task to a visual component: [net.jcip.examples.ListenerExamples.java](https://jcip.net/listings/ListenerExamples.java)
* 9.5 Long-running task with user feedback: [net.jcip.examples.ListenerExamples.java](https://jcip.net/listings/ListenerExamples.java)
* 9.6 Cancelling a long-running task: [net.jcip.examples.ListenerExamples.java](https://jcip.net/listings/ListenerExamples.java)
* 9.7 Background task class supporting cancellation, completion notification, and progress notification: [net.jcip.examples.BackgroundTask.java](https://jcip.net/listings/BackgroundTask.java)
* 9.8 Initiating a long-running, cancellable task with BackgroundTask: [net.jcip.examples.ListenerExamples.java](https://jcip.net/listings/ListenerExamples.java)

## Avoiding Liveness Hazards

* 10.1 Simple lock-ordering deadlock: [net.jcip.examples.LeftRightDeadlock.java](https://jcip.net/listings/LeftRightDeadlock.java)
* 10.2 Dynamic lock-ordering deadlock: [net.jcip.examples.DynamicOrderDeadlock.java](https://jcip.net/listings/DynamicOrderDeadlock.java)
* 10.3 Inducing a lock ordering to avoid deadlock: [net.jcip.examples.InduceLockOrder.java](https://jcip.net/listings/InduceLockOrder.java)
* 10.4 Driver loop that induces deadlock under typical conditions: [net.jcip.examples.DemonstrateDeadlock.java](https://jcip.net/listings/DemonstrateDeadlock.java)
* 10.5 Lock-ordering deadlock between cooperating objects: [net.jcip.examples.CooperatingDeadlock.java](https://jcip.net/listings/CooperatingDeadlock.java)
* 10.6 Using open calls to avoiding deadlock between cooperating objects: [net.jcip.examples.CooperatingNoDeadlock.java](https://jcip.net/listings/CooperatingNoDeadlock.java)
* 10.7 Portion of thread dump after deadlock. (not a code listing)

## Performance and Scalability

* 11.1 Serialized access to a task queue: [net.jcip.examples.WorkerThread.java](https://jcip.net/listings/WorkerThread.java)
* 11.2 Synchronization that has no effect. (fragment)
* 11.3 Candidate for lock elision: [net.jcip.examples.ThreeStooges.java](https://jcip.net/listings/ThreeStooges.java)
* 11.4 Holding a lock longer than necessary: [net.jcip.examples.AttributeStore.java](https://jcip.net/listings/AttributeStore.java)
* 11.5 Reducing lock duration: [net.jcip.examples.BetterAttributeStore.java](https://jcip.net/listings/BetterAttributeStore.java)
* 11.6 Candidate for lock splitting: [net.jcip.examples.ServerStatusBeforeSplit.java](https://jcip.net/listings/ServerStatusBeforeSplit.java)
* 11.7 ServerStatus refactored to use split locks: [net.jcip.examples.ServerStatusAfterSplit.java](https://jcip.net/listings/ServerStatusAfterSplit.java)
* 11.8 Hash-based map using lock striping: [net.jcip.examples.StripedMap.java](https://jcip.net/listings/StripedMap.java)

## Testing Concurrent Programs

* 12.1 Bounded buffer using Semaphore: [net.jcip.examples.SemaphoreBoundedBuffer.java](https://jcip.net/listings/SemaphoreBoundedBuffer.java)
* 12.2 Basic unit tests for BoundedBuffer: [net.jcip.examples.TestBoundedBuffer.java](https://jcip.net/listings/TestBoundedBuffer.java)
* 12.3 Testing blocking and responsiveness to interruption: [net.jcip.examples.TestBoundedBuffer.java](https://jcip.net/listings/TestBoundedBuffer.java)
* 12.4 Medium-quality random number generator suitable for testing: [net.jcip.examples.XorShift.java](https://jcip.net/listings/XorShift.java)
* 12.5 Producer-consumer test program for BoundedBuffer: [net.jcip.examples.PutTakeTest.java](https://jcip.net/listings/PutTakeTest.java)
* 12.6 Producer and consumer classes used in PutTakeTest: [net.jcip.examples.PutTakeTest.java](https://jcip.net/listings/PutTakeTest.java)
* 12.7 Testing for resource leaks: [net.jcip.examples.TestBoundedBuffer.java](https://jcip.net/listings/TestBoundedBuffer.java)
* 12.8 Thread factory for testing ThreadPoolExecutor: [net.jcip.examples.TestThreadPool.java](https://jcip.net/listings/TestThreadPool.java)
* 12.9 Test method to verify thread pool expansion: [net.jcip.examples.TestThreadPool.java](https://jcip.net/listings/TestThreadPool.java)
* 12.10 Using Thread.yield to generate more interleavings. (fragment)
* 12.11 Barrier-based timer: [net.jcip.examples.BarrierTimer.java](https://jcip.net/listings/BarrierTimer.java)
* 12.12 Testing with a barrier-based timer: [net.jcip.examples.TimedPutTakeTest.java](https://jcip.net/listings/TimedPutTakeTest.java)
* 12.13 Driver program for TimedPutTakeTest: [net.jcip.examples.TimedPutTakeTest.java](https://jcip.net/listings/TimedPutTakeTest.java)

## Explicit Locks

* 13.1 [Lock interface](https://jcip.net/http://java.sun.com/j2se/1.5.0/docs/api/java/util/concurrent/locks/Lock.html##method_summary). (external link to Javadoc)
* 13.2 Guarding object state using ReentrantLock. (fragment)
* 13.3 Avoiding lock-ordering deadlock using try Lock: [net.jcip.examples.DeadlockAvoidance.java](https://jcip.net/listings/DeadlockAvoidance.java)
* 13.4 Locking with a time budget: [net.jcip.examples.TimedLocking.java](https://jcip.net/listings/TimedLocking.java)
* 13.5 Interruptible lock acquisition: [net.jcip.examples.InterruptibleLocking.java](https://jcip.net/listings/InterruptibleLocking.java)
* 13.6 [ReadWriteLock interface](https://jcip.net/http://java.sun.com/j2se/1.5.0/docs/api/java/util/concurrent/locks/ReadWriteLock.html##method_summary). (external link to Javadoc)
* 13.7 Wrapping a Map with a read-write lock: [net.jcip.examples.ReadWriteMap.java](https://jcip.net/listings/ReadWriteMap.java)

## Building Custom Synchronizers

* 14.1 Structure of blocking state-dependent actions. (fragment)
* 14.2 Base class for bounded buffer implementations: [net.jcip.examples.BaseBoundedBuffer.java](https://jcip.net/listings/BaseBoundedBuffer.java)
* 14.3 Bounded buffer that balks when preconditions are not met: [net.jcip.examples.GrumpyBoundedBuffer.java](https://jcip.net/listings/GrumpyBoundedBuffer.java)
* 14.4 Client logic for calling GrumpyBoundedBuffer: [net.jcip.examples.GrumpyBoundedBuffer.java](https://jcip.net/listings/GrumpyBoundedBuffer.java)
* 14.5 Bounded buffer using crude blocking: [net.jcip.examples.SleepyBoundedBuffer.java](https://jcip.net/listings/SleepyBoundedBuffer.java)
* 14.6 Bounded buffer using condition queues: [net.jcip.examples.BoundedBuffer.java](https://jcip.net/listings/BoundedBuffer.java)
* 14.7 Canonical form for state-dependent methods. (fragment)
* 14.8 Using conditional notification in BoundedBuffer.put: [net.jcip.examples.BoundedBuffer.java](https://jcip.net/listings/BoundedBuffer.java)
* 14.9 Recloseable gate using wait and notifyAll: [net.jcip.examples.ThreadGate.java](https://jcip.net/listings/ThreadGate.java)
* 14.10 [Condition interface](https://jcip.net/http://java.sun.com/j2se/1.5.0/docs/api/java/util/concurrent/locks/Condition.html##method_summary). (external link to Javadoc)
* 14.11 Bounded buffer using explicit condition variables: [net.jcip.examples.ConditionBoundedBuffer.java](https://jcip.net/listings/ConditionBoundedBuffer.java)
* 14.12 Counting semaphore implemented using Lock: [net.jcip.examples.SemaphoreOnLock.java](https://jcip.net/listings/SemaphoreOnLock.java)
* 14.13 Canonical forms for acquisition and release in AQS. (fragment)
* 14.14 Binary latch using AbstractQueuedSynchronizer: [net.jcip.examples.OneShotLatch.java](https://jcip.net/listings/OneShotLatch.java)
* 14.15 tryAcquire implementation from nonfairReentrantLock. (See JDK source)
* 14.16 tryAcquireShared and tryReleaseShared from Semaphore. (See JDK source)

## Atomic Variables and Nonblocking Synchronization

* 15.1 Simulated CAS operation: [net.jcip.examples.SimulatedCAS.java](https://jcip.net/listings/SimulatedCAS.java)
* 15.2 Nonblocking counter using CAS: [net.jcip.examples.CasCounter.java](https://jcip.net/listings/CasCounter.java)
* 15.3 Preserving multivariable invariants using CAS: [net.jcip.examples.CasNumberRange.java](https://jcip.net/listings/CasNumberRange.java)
* 15.4 Random number generator using ReentrantLock: [net.jcip.examples.ReentrantLockPseudoRandom.java](https://jcip.net/listings/ReentrantLockPseudoRandom.java)
* 15.5 Random number generator using AtomicInteger: [net.jcip.examples.AtomicPseudoRandom.java](https://jcip.net/listings/AtomicPseudoRandom.java)
* 15.6 Nonblocking stack using Treiber's algorithm: [net.jcip.examples.ConcurrentStack.java](https://jcip.net/listings/ConcurrentStack.java)
* 15.7 Insertion in the Michael-Scott nonblocking queue algorithm: [net.jcip.examples.LinkedQueue.java](https://jcip.net/listings/LinkedQueue.java)
* 15.8 Using atomic field updaters in ConcurrentLinkedQueue. (fragment)

## The Java Memory Model

* 16.1 Insufficiently synchronized program that can have surprising results: [net.jcip.examples.PossibleReordering.java](https://jcip.net/listings/PossibleReordering.java)
* 16.2 Inner class of FutureTask illustrating synchronization piggybacking. (See JDK source)
* 16.3 Unsafe lazy initialization: [net.jcip.examples.UnsafeLazyInitialization.java](https://jcip.net/listings/UnsafeLazyInitialization.java)
* 16.4 Thread-safe lazy initialization: [net.jcip.examples.SafeLazyInitialization.java](https://jcip.net/listings/SafeLazyInitialization.java)
* 16.5 Eager initialization: [net.jcip.examples.EagerInitialization.java](https://jcip.net/listings/EagerInitialization.java)
* 16.6 Lazy initialization holder class idiom: [net.jcip.examples.ResourceFactory.java](https://jcip.net/listings/ResourceFactory.java)
* 16.7 Double-checked-locking antipattern: [net.jcip.examples.DoubleCheckedLocking.java](https://jcip.net/listings/DoubleCheckedLocking.java)
* 16.8 Initialization safety for immutable objects: [net.jcip.examples.SafeStates.java](https://jcip.net/listings/SafeStates.java)
