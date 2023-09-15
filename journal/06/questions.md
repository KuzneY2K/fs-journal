# Single Page Applications with Vue
01. What is the entrypoint of an application?

  > The entrypoint is the window or frame

02. What is the difference between a vue `component` and `page`?

  > Pages handle getting the data, handling it and getting that data out to the page. Components are the data and the things that make up the page in a smaller form.

03. What is ***Component-Based Architecture***?

  > Method of encapsulating individual pieces of a larger user interface into self sustaining, independent micro-systems.

04. What are the three tags that make up a Vue component?

  > Template, Script, Tag

05. What are ***lifecycle hooks***? What are lifecycle hooks used for?

  > They are a window into how the library youre using works behind the scenes. Lifecycle hooks allow you to know when component is created, added to the dom, updated or destroyed.

06. Which component in Vue does the vue-router use to mount pages onto?

  > routes

07. What is the difference between the `AppState` and the state object within a component?

  > State is exclusive to the component. Its internal. The AppState is app wide and shares data with the rest of the app.

08. What is the responsibility of `Services` in our Vue projects?

  > The same as our MVC projects. Handle business and communicate with the appstate.

09. What are ***props*** and how are they used? Provide an example

  > Props are how we pass variables and other information between components. An example is passing down a computed prop to a component so that it can use that data. <PostCard :post="post" /> then in the component props: {post: {type: Post, required: true}} and now the PostCard component can use Post data.

10. What is the Vue method used to create watchable objects such as `state` or `AppState`?

  > watchers. they watch for changes and fire callbacks if anything is diffrent
