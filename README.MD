# JSO3 API
This class will assume the following: **proficiency with git**, **mastery over javascript variables**, and a *comfortable* **ES6 syntax**
## Resources
- [JQuery Documentation](https://api.jquery.com/)
- [PokeApi](https://pokeapi.co/)
- [Postman](https://www.getpostman.com/) **Recommended**
- [Ecmascript 6](https://github.com/airbnb/javascript) **Suggested**
- More will be added in the future

What this class will review is javascript APIs!

To make a simple JQuery Ajax call:
```javacript
callOptions = {
    url: 'https://pokeapi.co/api/v2/',
    type: 'GET',
    datatype: 'json',
    success: (data) => {
        console.log(data);
    },
    error: (data, error) => {
        console.log(data);
        console.log(error);
    }
}
$.ajax(callOptions);
```

`callOptions` is a javascript **object** that we use to define the link, type of request, and datatype of `data`. `success` and `error` are both object keys that define a **callback function**. This means that the ajax call will pass the data from the api calls to those functions.
*Hint: you need to know what the bold words mean.*

# Week Reviews
1. [Week 1](Week1.md)


# Homework
1. [Week 1 Homework](Week1Hw.md)
