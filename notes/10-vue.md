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

v-if will render an element on condition. v-if="something.value"