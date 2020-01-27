1. What problem does the context API help solve?

> Answer: The Context API solves the problem of prop drilling, where you'd have to pass props down to deeply nested components. It is especially useful for  data that is considered global and is accessed by many components such as, language & locale preferences, currently authenticated user, and themes & styles used throughout the app.

1. In your own words, describe `actions`, `reducers` and the `store` and their role in Redux. What does each piece do? Why is the store known as a 'single source of truth' in a redux application?

> Answers:
> - Actions - When and event occurs in the UI an action that describes that event is dispatched to the reducer. An action type is included in the action object to avoid hidden bugs. Invoking the action creater dispatches it to the reducer.

> - Reducers - The reducer updates the state tree in a predictable way. 

> - Store - The Store sets the state and sends it to the UI. The Redux Store cannot be mutated directly, instead the stored objects are updated with an updated clone of the original object. 

1. What is the difference between Application state and Component state? When would be a good time to use one over the other?

> Answer:  Application state should be shared thoughout out the app, and it should be considered the single source of truth. Component state is state that only the current component is concerned with. such as statefull logic to clear form fields after it has been submitted.

1. Describe `redux-thunk`, what does it allow us to do? How does it change our `action-creators`?

> Answer:  Redux-thunk intercepts and acts on returned data. If an action is returned it will forward the action to the reducer. if a function is returned (a thunk) , it will invoke the thunk and pass the dispatch function as a argument to it. Redux-thunk extends action-creators so they can consume promises.

1. What is your favorite state management system you've learned this sprint? Please explain why!

> Answer:  I prefer the explicitness of redux, but I also see many cases where context would be a great choice in a smaller application.

