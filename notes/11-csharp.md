# CSharp



Data types:

int y = 10;

float z = 4.5f;

double a = 5.55;

decimal b = 6.90128m;

string h = "hello hello helllo";

char g = 'g';

bool yes = true;

bool no = false;

Arrays have a fixed length, therefore you can't take anything out or put anything in.

Array<int> = new Array[3]{1, 2, 3};

List<string> cats = new List<string>(){"Test", "Bannana", "Skits"};
cats.Add("Garfield");
cats.Add("Beans");
cats.Add("Socks");
Console.WriteLine(cats.Count);
cats.Remove("Test")
string catToRemove = cats.find(c => c == "Test")

cats.forEach(c => {
    Console.WriteLine(c)
})

A dictionary is a type that takes in a key value pair
Dictionary<TKey, TValue>

T in front of key and value is asking for its data type
Dictionary<string, ing> myCats = new Dictionary<string, int>();
myCats.Add("Mark", 0);

Dictionary<List<string>, string> marksCats = new Dictionary<List<string>, string>();
marksCats.Add(cats, "Mark");

Classes
Members are created with Capital Letters, variables and params are lowercase

class Cat{

    string Name;
    string Color;
    int Age;

    public Cat(string name, int age, string color)
    {
        Age = age
        Name = name
        Color = color
    }
}

public readonly - anyone can see it but cant change it. like a const

data decorators/attributes affect the next definition, making our class an API controller with the route ".../api/cats"
[ApiController]
[Route("api/cats")]
public class CatsController : ControllerBase{

    private readonly CatsService _catsService;

    public CatsC

    putting [HttpGet] in front of function makes it an http request

    [HttpGet]
    public string GetTest(){
        return "test"
    }

    [HttpGet]
    public List<Cat> GetCats(){

    }

}

namespace used to define existence within project

namespace projectTesting;

using works like import

using projectTesting.Models; <= thats importing every model

dollar sign at the start of string will let you use curly brackets anywhere in the string

id = Guid.NewGuid();
randomized unique id

<!-- DB VCONNECt -->

private readonly IDbConnection _db;

public WhateverRepository(IDbConnection db)
{
    _db = db;
}

internal List<Thing> GetAllThings()
{
    string sql = "SELECT * FROM things;";
    List<Things> things = _db.Query<Thing>(sql)
                                    ^^^^ <= this will map data from tables to prop. that is the data type of the row, or what it should be.
    return things;
}

use .FirstOrDefault(); when searching something by id in repository

mySQL variables can be instantiated with @

to avoid sql injection attacks pass a key value pair into the query to match and pull values

string sql = @"
INSERT INTO cars
(name, age, isStudent, hasJob)
VALUES
(@name, @age, @isStudent, @hasJob) 
SELECT * FROM friends WHERE id = LAST_INSERT_ID();
"

if(rowsAffected > 1) throw new Exception("YOU DELETED IT ALL")
if(rowsAffected < 1) throw new Exception("YOU GOOD")

no truthy falsy in C#!SECTION

ternary works a little differently

Friend original = this.getFriendById(updataData.id)
original.name = updateData.name != null ? updataData.name : original.name

So datatypes are not nullable so you can go to the model and set a ? at the end of a data type to make it nullable
or you can add two ?? to make it nullable

there is no .save() method like Mongo. Instead you need to make an update method

Friend friend = _repo.UpdateFriend(original)
{
    return friend;
}

over at repo

internal Friend UpdateFriend(Friend friendData)
{
    string sql = "@
    UPDATE friends
    SET
    name = @name,
    age = @age,
    isStudent = @isStudent
    WHERE id = @id; SELECT * FROM id WHERE id = @id
    ";
    Friend friend = _db.Query<Friend>(sql, friendData).FirstOrDefault();
    return friend;
}

@"SELECT * FROM albums alb JOIN accounts act ON act.id == alb.creatorId" <= gets albums mathching account id with creator id


                                                Actual return type
List<Album> albums = _db.Query<Album, Account, Album>(sql, (album, account)=>{
                                Aliased out =>                Aliases for what is being returned, bananna words
}).ToList();

<!-- Importing auth dependency -->

private readonly Auth0Provider _auth0; <= add as param to constructor and then _auth= = auth0

When using async in C# we must use task. Creates a new thread for the async req to run in and ends thread when we return the promise

ex: public async Task<ActionResult<Album>> Create([FromBody] DATATYPE whateverItsCalled)

[Authorize]
This decorator will guard the HTTP request below it. Adding this decorator over [ApiController] protects all of the HTTP requests in the controller.

ASYNC FUNCTIONS MUST BE WRAPPED IN A TASK SO THAT IT CAN RUN ON ITS OWN THREAD

When using Auth0 ids make sure the data type is a string because thats exactly what it is, a STRING

an interface defines a single method (contract) that can be used and made unique by multiple concrete classes in the same scope. ex: I can Console.WriteLine a unique message on every class I have without compilation errors. The method can ONLY be defined NOT implemented

an abstract reduces code redundancy. I can define and implement methods within the abstract to make them inheritable. I dont even have to define and implement the method in those concrete classes because they are already defined in that abstract. they will be automatically called if a call back BUT i can also create unique abstract methods by ONLY defining the method and the overriding it in the concrete class.

