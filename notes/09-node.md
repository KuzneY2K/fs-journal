# Node

Node server is stateless. No AppState.

Schema keyword for Mongo. Creates structure for the data to be saved to the DB.

schema ex...
{
    title: {type: String, required: true}
}

Comment out Auth0Provider.configure

Inheritance is one class taking from another class. extends takes data from parent/base controller.
Must add a super call to child class.
Super calls the constructor of the parent/base controller.
this.router
.get('', ()=> console.log "yoooo")
is someone hits api get req it will console log "yooo" because there were no extends.
.get('/:catName', this.getCatByName) this is an extend
you can define route with a :, so now name became a variable
the : creates a property on the request params
const cat = catsService.getCatByName(request.params.catName)
response.send(Cat)

Request is an obj representing incoming request from user
Response is an obj for you to manipulate and use to sent responses to user
Next kicks people back into hall

response.send(can only send one thing)

next moves on to the next thing and eventually sends user back to starting point

DBConnection.connect()

Params take out what is in the URL 


ObjectId will always reference from "ref" and always pull data from that.

type: schema.types.objectid, ref: 'parent collection'

request.query can be passed into .find() method

api/examples?key=value &name=test+query or &key=value <= will turn obj into array

{ toJSON: {vituals: true} }

AnimalSchema.virtual('exhibit', 
{
    THIS schema
localfield: 'exhibitid' 
REFERENCING other schema
ref: 'Exhibit', 
from OTHER schema we take _id for THIS schema
foreignField: "_id", 
justOne: 'true'
})

.populate('exhibit') after mongoose method
syntax for multiple args loogs like this 'biome emoji'

get animals from specific exhibit for example

/:exhibitId/animals

ternary works better with BOOL

<!-- AUTH0 -->

Go to applications => Applications and create and application

Copy domain and client id under settings.

scroll to allowed urls

Need to modify Allowed Callback URL, Allowed Logout URL, Allowed Web Origins
Notifies where the user is making a login/logout request

Create and API and give it a name and an identifier, dont touch signing algo

go to actions and go to flows, then go to log in

next to add action, the build custom

extend_user_info_with_mongo_id, for name

on login users will be generated an object id from mongo db

domain, client id and audience <= important need

set up .env in server, then head to client and set up env.js with auth0


In postman, you can paste bearer token in the Auth tab <= network, preview, token
You can also paste the bearer token for the whole collection

const body = request.body

You can get a list of stuff or have stuff render in before having to log in
.get()
.use(Auth0Provider.AuthorizeUserInfo)
^^^^
This middle ware will only let people post put and delete when logged in

This will attach an Auth id onto a customer
body.customerId = request.userInfo.id
.populate('customer')

dont need to make another axios instance since the server already holds the api.
I can just create http requests pointing at "api/whatever"

make sure .populate is awaited since the method is a promise.

only on .find methods should .populate be tacked onto the end.

.sort('-createdAt') will have mongoose sort by created at, or you can even use updated at.
tacked on after find method, on db context

user.isAuthenticated better than using account.id 