# NoAPI

```typescript
// calling backend function should be this easy
try {
  const myUser: User = await NoAPI.getUserById(123);
} catch(e: NoAPIError) {
  console.log(e.status)
  console.log(e.message)
}
```

The idea is to build function definitions in TypeScript that are shared by both backend and front-end with the popular socket.io library.

Instead of REST APIs, GraphQL, would pass all data through one websocket layer, but have strongly typed functions to.

This would be like microsofts long time "web services" which bridged C# accross client / server.

Defining your API should be this easy

```typescript
// need to define methods in one file
interface NoAPIMethods = {
  getUserById: (userId: number) => Promise<User> 
}
```

## Roadmap

- [ ] Get started, try deno with socket.io
- [ ] Setup simple client / server demo with regular socket.io events.
- [ ] Figure out how to make function calls simple from the client
- [ ] Throw consitent http exception object containing messages, status codes.
- [ ] Need to figure out best way to shared definitions with client if they are not from same code repo.
- [ ] Figure out nice way for subscribing to events also

