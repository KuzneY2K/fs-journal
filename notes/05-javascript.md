# JavaScript

<!-- Primitive Data types -->

<!-- strings -->

let stringData = `Yo this is a string` 'Yo this is a string' "Yo this is a string\'s string."

<!-- floats -->

let numberData = 3

let decimalData = 32.33333333333333

let negData = -6

<!-- truthy / falsy -->

let falseNumber = 0 - is always false

let trueNumber = 1 - any other number is true including negative numbers

let falseString = '' - nothing = false

let trueString = 'fasdf' - anything including space

let moreFalse = undefined

let evenMoreFalse = null

let moreTrue = [] - if array or object is empty they are seen as true

let anotherTrue = {}

<!-- No Value types -->

let undefinedNumber - I dont know there is nothing

let knowTheresNothing = null - I know there is nothing

<!-- Reference Data Types -->

let array = ['one', 'two', 'three']
let numArr = ['1', '2', '3']
let mixed Arr = ['1', 'true', 'two']

obj = {
    dog: 'fat mutt',
    cat: 'chungus',
    mouse: 'jerry'
}

Objects can be accessed with square brackets [] and dot notation object.value

<!-- NOTE information can get passed down like this, be mindful of that. -->

let otherArr = arr

otherArr[3] = 'Sword'

arr
['jack sparrow', 'black beard', 'luffy', sword]

<!-- Function -->
<!-- are blocks of code to store and run later -->

function sayHello(){
    console.log(`hello`)
}

<!-- Parameters -->
<!-- temporary variables only exist when func is executed -->
<!-- anytime you use numbers in a function it will pull variables from the closest scope -->

function addNumbers(x, y){
    console.log(x + y)
}

<!-- on separate part of the doc -->
<!-- will replace x and y with values pulled from doc -->


                                x                       y
function addNumber(numberOutputOne.innerHTML, numberOutputTwo.innerHTML){
    console.log(x + y)
    return x + y - you can give back numbers with a return and store them
}

<!-- array with object -->

let userData = [
    {
        name: 'test'
        othername: 'test'
        address: {street: 'test', state: 'test', zipCode: 'test'}
    },
    {
        name:
        othername:
        favoriteFood: ['food', 'food', 'food', 'food']
    }

]

for (let i = 0; i <= userData.length; i++){
    let user = userData[i]
    runInfo(user)
}

function runInfo(user){
    console.log(userData.name, userData.favoriteFood)
}

userData.forEach(runInfo)

for each user run their info

anonymous function
no name function, good for buttons


                    this variable is targeting to userData, creating temp variable
userData.forEach((user, i) => {
    console.log(i)  writes index(position) number
    console.log(user.name)
})

runs and destroys it self 

userData.forEach((user) => {
    console.log('area')
   let inArea = userData.filter((user) => user.currentArea == area)
   let userEmoji = inArea.map((user) => user.emoji + user.name)
    document.getElementById(area).innerText = userEmojis.join(",")
})

    searches the array for the user that is in the area and logs them if their
    current area is the area that was originally console logged

userData.map((user)=> user.name)

.join turns array into a string

find filter map



----- make own event emitter ---

const myEvent = new Event('my-event')

elem.dispatchEvent('my-event')

elem.addEventListener('my-event', () => {
    drawSomething();
})

local storage

localStorage.setItem(key, value)
localStorage.getItem(key)
localStorage.removeItem(key)
localStorage.clear()

ex...

localStorage.setItem('username', 'markMark55')

if (localStorage.username === 'markMark55'){
    return 'Its mark'
}

localStorage.setItem('myCat', 'kitty')

const cat = localStorage.getItem('myCat')

constructors are used for creating and initializing instances of their class.

get date

let date = new Date() <= gives timestamp
                    ^
                    you can put a date in the args and change time stamp, ex. 3-12-2017


.onsubmit="myFunction()" works for submit buttons for forms

ternary
this.reportedData = data.reportedData ? new Data(data.reportedData) : new Date()
                            new date?      do this if true            else do this


.slice() sting method can take in the index of a string and take another index and slice everything else out


get reportBody
return this.reportBody.slice(0, 15) + "..."

will return characters 0 - 15 and will add a ... at the end
the getter will change the display of the string without changing the orignial

drawing to dom will look like: foreach content += template
content is empty ''

using null allows us to use true/false / bool
can set an object default by just putting it on the file as null ex. activeCases = null <= will set to false by default

AppState.on('activeCase') listens for an changes in the activeCase object <= arg MUST be exact.

.split(' ') on every space it will split the string up and toss the word or whatever into the array
.join(' ') will insert a space between each index when combining into a string


Fisher Yates Shuffle Algo

for (let i = array.length - 1; i > 0; i--){
    const j = Math.floor(Math.random() * (i + 1))
    [array[i], array[j]] = [array[j], array[i]]
}

Another Similar Algorithm


  shuffleArray(array) {
    // Loop Through Array
    for (let i = 0; i < array.length; i++) {
      // Create Random Number 0 - Array Length
      const swapIndex = Math.floor(Math.random() * array.length)
      // Current Index
      const currentIndex = array[i]
      // Finds Random Index
      const indexToSwap = array[swapIndex]
      // Swaps Current Index With Random Index
      array[i] = indexToSwap
      // Swaps The Random Index With the Old Index
      array[swapIndex] = currentIndex
      // Randomized
    }
    return array
  }