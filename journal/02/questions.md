# Intro to JavaScript
01. Which keywords are used to declare a variable in JavaScript?

    > let, var, const

02. What is the definition of a function?

    > It is a subprogram designed to perform a specific task,

03. What are the `SOLID` principles?

    > | Single responsibility principle, open/closed principle, liskov substitution principle, interface segregation principle, dependency inversion principle

04. Given this array: How could you remove the `pineapple`?

    ```js
    let fruit = ['apple', 'banana', 'pineapple', 'orange', 'strawberry']
    ```

    > | delete fruit[2]

05. Given these two objects: How could you add each to the others friends arrays?

    ```js
    let you = {
        name: "You",
        hair: true,
        friends: []
    }
    let them = {
        name: "Them",
        hair: false,
        friends: []
    }
    ```

    > | ANSWER HERE |

06. Give an example of a JavaScript `Conditional`:

    let example = 'example'
    > an if statement. if(example === 'example'){
        alert('example')
    } else {
        alert('example is not an example')
    }

07. What is the main difference between `parameters` and `arguments`?

    > parameters are listed in the function and arguements are passed down as parameters into a function

08. Instead of writing everything to the console, what is a better way to debug your code?

    > A better way to debug would be using "debugger" in a line of code

09. What is the difference between a `primitive` value and a `reference` value?

    > primitive values are strings and numbers such as "let x = 6" and "let y = 'test'"
    a reference value is a value that is stored in memory and can be accessed as a reference, for example
    "let z = x"

10. Demonstrate a loop that prints the numbers between -100 and 100?

    > for let(i = -101; i <= 101; i++){
        console.log('i')
    }
