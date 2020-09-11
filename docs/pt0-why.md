# Why do you need redux?

Redux is used to manage application state. 

> Let's get the obvious part of the way first--Redux is complex and there are other ways to do this. Not always better, not always worse. Just different. _Use what fits._

Alright, now let's move on to application state. The application's "state" is the data that represents what is currently happening.

- The user's name `Alice`
- Their email address is `alice@email.com`
- The last query had 10 results, with 23 more available for paging
- The user has a `basic` role
- Dark mode is enabled

Or, in practice, we could imagine all of this data ("state") could be represented as a big JSON object:

```js
{
    userprofile: {
        username: 'Alice',
        role: 'basic',
        email: 'alice@email.com'
    },
    query: {
        results: [{}, {}, ...]
        page: 1,
        remaining: 23
    },
    styles: {
        darkmode: true
    }
}
```

This is only a small example. However, this is to say that any data our application is using can be considered it's "state". At first it might not seem like there's not much need for engineering here: _query something_ and then _store it_, right? This problem is deceptively complex.

## Briefly on state management

Without getting into a full history of web applications, jQuery, and why tools like Angular, React, Vue, and many others popped up...we'll just summarize to say that implementing repeatable processes for normal "CRUD" operations in the browser (and thereby, JavaScript) isn't simple. Just look at all of the design structures and ORM tools built around this problem for more structured languages like C#, Java, or Ruby!

## Explain redux "patterns"

_Okay, back to React and Redux._

- Keeps up with React's one-way data flow
- Single source of truth
- Immutability

## So, why do we need Redux in React?

I mean, React already provides an effective way to think about components, right? And those components have their own _state_! Very true, but let's look at a simple example of where this starts to break down.

## Practical ~~Core~~ Pieces

We could be limited to only discussing the "_true core pieces_" of redux, but I find they aren't entirely practical on their own when used inside of React. So, we're going to add a small bit of complexity.


- Actions
- Constants*
- Services*
- Reducers
- Store

