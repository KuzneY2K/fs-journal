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

mongodb+srv://mkuzfl:markMarkmark@cluster0.tdofteo.mongodb.net/?retryWrites=true&w=majority
goes to .env in vscode

DBConnection.connect()

Params take out what is in the URL 