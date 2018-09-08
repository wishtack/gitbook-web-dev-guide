# Single-Threaded thus Asynchronous

## Multi-thread vs mono-thread

In a synchronous, multi-threaded and data-driven world, this works:

```javascript
function processRequest(request) {
​
    /*
     * Pre-processing.
     */
    var query = prepareQuery(...);
​
    var result = execQuery(query); // might take few seconds...
​
    /*
     * Post-processing.
     */
    var response = createResponse(result);
​
    return response;
​
}
```

... but in a single-threaded world, this can lead to trouble as the application would freeze until it receives a response.

**Until the function ends** _**\(and its callees\)**_**, no other function can be executed simultaneously.**

## Asynchronous processing using callbacks

```typescript
function processRequest(request, callback) {
​
    /*
     * Pre-processing.
     */
    var query = prepareQuery(...);
​
    execQuery(query, function (result) {
​
        /*
         * Post-processing.
         */
        var response = createResponse(result);
​
        callback(response);
​
    });
​
}
```

## Asynchronous processing advantages

* No threads count limitation.
* No memory overhead due to threads.
* No locks or semaphores.
* No greedy locks.
* No deadlocks.
* Data doesn't change during the execution of a function.

## Closures

A **closure** is the combination of a function definition and the lexical environment in which the latter is defined.

Closures determine the scope of the variables.

Variables can be read and modified in the closure where they are declared **but also in the functions defined inside**.

```javascript
function main() {
​
    var userName = 'Foo';
​
    function setUserName(value) {
        userName = value;
    }
​
    function getUserName() {
        return userName;
    }
​
    setUserName('John');
​
    console.log(getUserName()); // 'John';
​
}
​
main();
```



