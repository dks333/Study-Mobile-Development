# RxSwift

## Why using RxSwift

Making serialization of data/event streams and asynchronous tasks more convenient

- Asynchrony is simplified with declarative programming: no more nested callbacks, delegates, notifications, KVOs
- Safe multi-threading with .observerOn(scheduler)
- Clean code and release pressures in controller layers

## Subjects

### PublishSubject

- Only accepts events that occur after subscribing to him

### ReplySubject

- Accepts event after subscribing to him, as well as receive the event that was send before him(buffersize: the number of previous events)

### BehaviorSubject (the most common usage)

- Accepts event after subscribing to him, as well as the last event

## Variable

- Wrapped BehaviorSubject
  - Use ```.asObservable``` to unbox
- Modify the value of the object when issuing an event

## Transformation 

1. Map
2. FlatMap
   - FlatMapLatest: only care about changes in the value of the lastest subsription

## Resouces Release

1. Dispose (MRC)
   - Dispose Bags (ARC)

## Example: Tableview with RxSwift

![RxSwift Example](/Users/apple/Desktop/📖/Study-Notes/Swifty Notes/RxSwift Example.png)





## Related Articles or Resources

Credits from: <a href="https://programmersought.com/article/6406641733/;jsessionid=7E73989D719589F93895DBAA84200AA1">This article</a>

<a href = "https://medium.com/flawless-app-stories/practical-mvvm-rxswift-a330db6aa693">MVVM & RxSwift</a>

