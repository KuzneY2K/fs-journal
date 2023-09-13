# Vue

Uses hot module to reload.

Package JSON keeps track of dependencies.

Use run client. No more live server or bcw serve/live. 
Vite needs to run for hot module.

Vue does not use controllers. It uses single file modules.

Rule of thumb is not to exceed 150 lines of code.

Have to use ref() for reactivity. ref() turns into object that has a .value property.

In the template when something is double bound, youre telling vue to put the .value on the view automatically. Double bind is {{}}

You can ONLY make objects reactive.

Accessing instances from the AppState is the same as before.
setup is private and return is public, so make sure to return setup.

computed(() => AppState.thingToDrill) similar to ref. not intended to be modified. it is a get. 
Drill with computed to GET values and SUBSCRIBE to changes for reactivity.

v-if will render an element on condition. v-if="something.value == 1"

: binds attribute to a certain statement. :disabled="health == 0"

You can bind classes 
        :class="{text-danger": health > 75,
        text-warn": health > 30 && health < 75}"

Use curly braces when creating multiple conditions since it becomes and object.

You can conditionally bind styles. 
:style="{
    backgroundColor: health == 0 ? 'red' : 'green'
}"

v-for="item in foodItems" :key='item.id' vue will repeat component 10 times

foodItems: computed(()=> AppState.foodItems) <= will listen for changes

props work like schemas

attributes not bound with {{}} ???

lifecycle hooks:
onMounted()
onUpdated()
onUnmounted()
it will run specific functions when triggered.

Members outside of the return is acessible by the code in the set up
Members inside of the return are accessible by the template

Instead of using = in a reactive state, use : since you are inside an object at that 

The page that uses prop data is reponsible for passing the prop data
Passed down data must be bound or else an error will be thrown talm bout stringss

ex <MovieCard :move="Movie"/>

To access props inside of setup, set up needs to take in props as an arguments

Elvis operator ? keeps your code from reaching into undefined

Return code to make it accessible within template

When clearing forms the VALUE needs to be redefined to '', so something.value = ''

All of this is literally the samething weve been doing the whole time/

@submit.prevent
@click.prevent    <= both will prevent forms from refreshing page on submit

event.target.reset() <= clears form the old way

Pages vs Component, Pages are defined within the router. Other than that, theres really no big difference.

router-link :to="{name: Home}" will take a user to a link in thats in the router

Router can be accessed within set up
Router.push({name: Home}) <= Router can be used like this to navigate. 