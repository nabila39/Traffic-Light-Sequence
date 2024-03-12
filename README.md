# Project Name
Traffic Light Sequence

# What is a callback function in JavaScript?
A Callback Function In Javascript Is A Function Passed To Another Function As A Parameter And Invoked Within The Outer Function. It Is Used To Perform A Task After A Certain Asynchronous Operation Has Completed, Ensuring That Javascript Is Non-Blocking And Efficient.
# Why are callbacks important in asynchronous programming?
Callbacks are crucial in asynchronous programming because they provide a mechanism for defining what should happen after a task completes without blocking the execution of other code. By passing functions as arguments to asynchronous functions, callbacks allow for non-blocking operations, enabling JavaScript to handle tasks like fetching data from servers or reading files while continuing to execute other code. This promotes efficient resource utilization and responsiveness in applications. Additionally, callbacks facilitate error handling and modular code design, enhancing the maintainability and flexibility of asynchronous programs.
# How do you define and pass a callback function to another function?
1. Define the Callback Function:
```
const callMe =()=> {
    console.log('I am callback function');
}
```
2. Define the Higher Order Function:
```
const greet =(name, callback)=> {
    console.log('Hi' + ' ' + name);
    callback();
}
```
3. Passing function as an argument:
```
greet('Peter', callMe);
```

# Difference between synchronous and asynchronous callbacks.
Synchronous callbacks in Javascript run immediately and block subsequent code from executing until they complete. Asynchronous callbacks, on the other hand, are non-blocking and allow subsequent code to run before they finish. They're generally used for time-consuming operations such as network requests and file I/O.
# What is the "callback hell" problem, and how can it be mitigated?
Callback hell is a phenomenon where a Callback is called inside another Callback. It is the nesting of multiple Callbacks inside a function. If you look at the design of the code, it seems just like a pyramid. Thus the Callback hell is also referred to as the ‘Pyramid of Doom’.
Callback hell structurally is just a nesting of function calls inside a function. But, it becomes difficult to understand and keep track of the nesting once the size of the nesting is increased.
### Here's an example of what callback hell might look like:
```
asyncFunction1(function(result1) {
  asyncFunction2(result1, function(result2) {
    asyncFunction3(result2, function(result3) {
      // More nested callbacks...
    });
  });
});
```
### There are several techniques to mitigate callback hell:
- Use named functions
- Use Promises
- Use async/await
# Live Demo
You can vist the web page from [Traffic Light Sequence]()
