# Async

Reject is an error

Async code should be in try and catch

try catch runs code, if errors occur, it will stop where the error happened and jump to the catch and stop running bad code

promise creates function to pause sync running of code

awaiting a promise pauses the code on the line until the promise resolves or rejects

await will wait for a resolution or rejection and the run the code once there it happens

await only wait for one event vs an event listener that listens for multiple events. await is very specific

await will throw async before function

click button
await console log <= wont run until button clicked
console.log(await pop.confirm)
console.log(4) <= wont run until pop is confirmed

try {
    
    console.log(sdfsdaf)

     catch (error)}{
        console.log('error')
}

api is middleman from me to the database
application program interface

fetch('url') grabs url and returns a response with a promise

await fetch('.com'), will wait till comes back with successful reponse

const data = await reponse.json(), will convert to data

grabbing api stuff

const reponse = await fetch('api url') <= reponse will wait until there was a successful response so it wont return a null
const data = await reponse.json <= will wait until there was a successful reponse and then will convert json to data.

map from api

                                this    =>          passed to this
newMontsters = data.data.map(monster => new Monster(monster))
model constructor data needs to match the json keys

export class Monster{
    constructor(id, name, image, description, drops){
        this.id = id
        this.name = name
        this.image = image
        this.description = description
        this.description = drops
    }
}

@type {Monster[]}

get MonsterCard(){
    return
    you already know what to do here dude
}

Appstate.monsters = newMonsters

async getMonsters(){
    await monsterService.getMonsters()
    _drawMonsters()
}

(private functions are the ones that run automatically, public are functions that are invoked by the user)

or

AppState.on('monsters', _drawMonsterCards)

another way to get data

const response = await axios.get('url')


will draw all monsters in a certain location

let filtered = newMonsters.filter(monster => monster.locations.includes(location))

AppState.monsters = filtered


const api = axios.create({
    baseURL: "test.com 😨"
    timeout: 8000 <= if it takes longer than 8s then throw an error
})

async getData(){ <= service getData
    const response = await _sandboxApi.get('api/data')
    console.log(response.data or whatever it is)
}

newStuff = response.data.map(dataObj => new Stuff(dataObj))
model constructor data needs to match the json keys

Appstate.on('Stuffs', _drawStuff()) will draw on any changes made to appstate stuffs

async getData()
try {
    await stateService.getData()
} catch (error) {
    alert(error)
    }
}

    async createStuff()
try
const form = window.event.target // targets the form that was submitted with the fuction attached to it
const formData = getFormData(form) // Creates object from form
await stuffService.createStuff(formData)
catch (error)
pop.error(error.message)

DO ALL FORMS IN TRY CATCH

create and post go hand in hand
anytime we do a post request we will be supplying some kind of body
the body is what we are trying to insert into the API


                                    target         what Im trying to send up
const res = await _sandboxApi.post('api/cars', formData)

const newStuff = new Styff(res.data) // takes new stuff that was posted from API and put it on local state

headers tab in network shows where requests go

post sandbox api link into env js file

async getAccount(){
    try {
        const res = await api.get('/account')
        AppState.account = new Account(res.data)
    }
}

statics exist as members of the class

getters exist on instances of the class

Car.createCarForm() - statics will work on this because its a member of the car class

new Car().createCarForm() - static will not work on this because its a NEW INSTANCE of a class

<!-- dynamic rendering -->

if appstate.account == null then return ''

if appstate.account.id == this.creator.id is true then return out a button or whatever

put the compute method into another method that renders elements

on any changes to the account re draw the page to show hidden elements


const updatedStuff = new Car(res.data)

let originalIndex = Appstate.stuff.findIndex(stu => stuff.id == activeStuffId)

Appstate.stuff.splice(originalIndex, 1, updated stuff)

splice will remove any # of index from an array based on the starting index, the last arg is what we want to replace the removed indexes with
grab the index of the old car
remove the one index
replace that index with updated index

after editing appstate make sure to emit('stuffs') or whatever you edited so that the on('stuff') fires what you need
