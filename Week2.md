# Week 2 - Review
#### Explanation between synchronous and asynchronous
A synchronous operation **blocks a process till the operation completes**. An asynchronous operation is non-blocking and **only initiates the operation**. The caller could discover completion by some other mechanism discussed later. [Source](http://www.cs.unc.edu/~dewan/242/s07/notes/ipc/node9.html)
For example:
```javascript
do1(); //this is async
do2(); // this is not async, it is sync
```
In the above code, `do1()` will start first, and it will immediately go to the next line `do2()`, without finishing. AJAX calls in Javascript are `async` because retrieving data from the Internet is slow (it's faster to do make a calculation of `1+1` in the computer rather than calling on an api to do so, as it has to receieve the requests, calculate, then send back the request).

### String Interpolation
Note: backticks (**`**) **are required**.
```javascript
const h = "iajfoa;iwejfawf";
console.log(`This is my variable h ${h}`); //"This is my variable h iajfoa;iwejfawf"
```
This is very useful for configuration messages, and code readability.
### ES6 Syntax (Functions)
```javascript
const nameOfFunct = (param1, param2) => {
    //your code here
    console.log(`${param1} ${param2}`);
}
```
Please follow form!
### Making POST requests, the fun part
```javascript
$.ajax({
            url: `LINK`, // Api Endpoint
            type: 'POST', // Type of request
            data: {
                "text": "Giordan was here",
                "aaaa": "was he though?" //this is how to add another row of data
            },
            success: (data) => console.log(data),
            error: (data, err) => {
                console.log(data);
                console.log(err);
            }
        });
```
Try it! Some apis require extra headers (remember giving a *blue box* to gift shops that only want gifts in blue boxes!). Add them like so:
```javascript
$.ajax({
            url: `LINK`, // Api Endpoint
            headers: { //HERE
                "header1": "pass",
                "API_KEY": MY_API_KEY
            }, //ENDHERE
            type: 'POST', // Type of request
            data: {
                "text": "aaaaaaaaaaaa",
            },
            success: (data) => console.log(data),
            error: (data, err) => {
                console.log(data);
                console.log(err);
            }
        });
```
