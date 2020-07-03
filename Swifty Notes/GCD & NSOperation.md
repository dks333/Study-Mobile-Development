# GCD & NSOperation

## GCD

- Serial anc concurrent
- Synchronous method returns control to the caller only after the task is completed
- Asychronous method returns control to the caller immediately
- Three main types of queues
  - Main queue (only Async)
    - Mainly used to rendering User Interface without any interferences
  - Global queues (4 types of Quality of Service from User-interactive to Background)
  - Custom queues(Default: serial queues)
- Deadlock 
  - Solutions: Make queues concurrent, avoid using locks
  - Dispatch Barries: all works prior to the barrier are guarateed to complete in the same queue
- No need to retain or release any of the global dispatch queues, including the concurrent dispatch queues or the main dispatch queue. Any attempts to retain or release the queues are ignored
- On iphones, discretionary and background operations including networking are paused when Low Power Mode is enabled



## NSOperation

- Operations are executed on a separate thread from GCD
- Using dependencies to execute an operation after another one is done
- Support KVO and KVC
  - Ready, cancelled, executed 
- Cacellation is enabled at any time duirng execution
- NSBlockOperation
  - ```let blockOperation = BlockOperation{ () -> Void }```
- NSInvocationOperation (Not in Swift)
- Operations with high priority will be executed first (5 levels)







