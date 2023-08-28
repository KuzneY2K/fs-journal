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

