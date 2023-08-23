# MVC

have a main.js or app.js linked as a type="module"

have a router set up that mounts controllers, look at template for reference

set everything up thats public inside of classes and export

private functions look like _privateFunction(), underscore means prive and dont mess with

models contain data blueprints, appstate holds actual true data

all data manipulation is to be handled in service since its going to directly change the appstate

pass form data through constructor from service
ex: let newCar = new Car(formData)

Also in service after changes have been made there needs to be an emit so that
the change is caught. 