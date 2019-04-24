# Promise

A promise (or "future") is an object which represents the output of some computation which hasn't necessarily happened yet. When you try to use the value in a promise, the program waits for the computation to complete.

Promises are a pattern that helps with one particular kind of asynchronous programming: a function (or method) that returns a single result asynchronously. One popular way of receiving such a result is via a callback (“callbacks as continuations”):

```
asyncFunction(arg1, arg2,
    result => {
        console.log(result);
    });
```
In order to avoid multiple asynchronous network calls, concept of promises was introduced.

A common case where you should immediately include promises is:-

```
networkCall1(condition1, callback1(){

  netweorkCall2(condition2, callback2(){

    networkCall3(condition3, callback3(){
      //functionality

    });

  });

})
```

the above case can be considered as callback hell. Promises is the best available tool to get rid of.

Promises provide a better way of working with callbacks: Now an asynchronous function returns a Promise, an object that serves as a placeholder and container for the final result. Callbacks registered via the Promise method then() are notified of the result:

```
asyncFunction(arg1, arg2)
.then(result => {
    console.log(result);
});
```

Compared to callbacks as continuations, Promises have the following advantages:

- No inversion of control: similarly to synchronous code, Promise-based functions return results, they don’t (directly) continue – and control – execution via callbacks. That is, the caller stays in control.
- Chaining is simpler: If the callback of then() returns a Promise (e.g. the result of calling another Promise-based function) then then() returns that Promise (how this really works is more complicated and explained later). As a consequence, you can chain then() method calls:

```
  asyncFunction1(a, b)
  .then(result1 => {
      console.log(result1);
      return asyncFunction2(x, y);
  })
  .then(result2 => {
      console.log(result2);
  });
```

- Composing asynchronous calls (loops, mapping, etc.): is a little easier, because you have data (Promise objects) you can work with.
- Error handling: As we shall see later, error handling is simpler with Promises, because, once again, there isn’t an inversion of control. Furthermore, both exceptions and asynchronous errors are managed the same way.
- Cleaner signatures: With callbacks, the parameters of a function are mixed; some are input for the function, others are responsible for delivering its output. With Promises, function signatures become cleaner; all parameters are input.
