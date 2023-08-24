# MVC

have a main.js or app.js linked as a type="module"

keep getter templates in model, getter is used because its more dynamic. its used as a prop that will be changed.
cant use a const because const will be changed and cant use let because the prop may be changed several times like a template and
can cause some issues. so the getter is pretty much turned into an individual property

getter are used to change the display of a certain property without changing the original property

have a router set up that mounts controllers, look at template for reference

set everything up thats public inside of classes and export

private functions look like _privateFunction(), underscore means prive and dont mess with

models contain data blueprints, appstate holds actual true data

all data manipulation is to be handled in service since its going to directly change the appstate

pass form data through constructor from service
ex: let newCar = new Car(formData)

Also in service after changes have been made there needs to be an emit so that
the change is caught. 

                        file name       
@type {import('./models/Case.js').Case}
                                    class name
un related, but this will totally help with intellisense when working in State file
just import right before instantization


when exporting like this you are not exporting a whole class. you will only use what is needed.
ex.
        casesService.myFunction() you will take just the function from the CasesService class

                this is just banana word, keep it relevant       
export const casesService = new CasesService()

every time you are in the service file you need to emit at the end of every function.
