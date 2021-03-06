## Compiled notes

### Design systems

- Reducing choice in building blocks (typography, color, spacing)
- https://airbnb.design/building-a-visual-language/
- https://component-driven.github.io/component-driven-development/styleguide

- https://medium.com/seek-blog/sketching-in-the-browser-33a7b7aa0526
- https://airbnb.design/painting-with-code/

- https://github.com/seek-oss/braid-design-system
- https://github.com/seek-oss/playroom


### SSR
- Seems to be becoming more popular
- Perf talk about netflix getting +50% perceived perf (halved TTI) by removing all client side react
- Uncanny valley, aka, LIE, looks interactive eh?
- Max stoiber talked up Next.js, regrets not using it as their SSR solution at spectrum
- esxjs which is an optimisation over Next js


### Micro frontends
- DAZN talked about how they break FE work across many teams
- Spotify way: Many iframes rendered on the page which communicate with an in-house event bus (although, spotify is moving to a react/redux solution so idk if they still considewr this a good idea)
- DAZN way
  - 1 micro frontend loaded at a time, don't want to share dependencies between micro frontends
  - 1 micro frontend per business domain (DDD)
  - Bootstraper loads first, retrieves some config from the API, based on request/url/whatever selects the correct micro frontend
  - https://medium.com/dazn-tech/adopting-a-micro-frontends-architecture-e283e6a3c4f3


### GraphQL
1. Workshop
    - serving graph-ql is actually a piece of cake with the right tools (yoga, graphpack)
    - react-apollo-hooks is very good, but not official, therefore requires a different context provider to react-apollo(-boost)

2. Conf talk
    - 2019 will be about DX for apollo
    - better TS support (apollo-cli can already auto-gen TS based on GQL schema)
    - better suggestions (i.e. for query perf)


### Fundamentals/React/Misc
- babel repl is good for figuring out `exactly` what's going on

- components should take props which handle behaviour not interaction
- components should do as little as possible and do it well, delegate up if you can
- if some logic isn't core to a feature, put it in a HOC or hook

- When designing an app which is mobile first/web for support, max stoiber says use react-native-web


### Open source libraries
- https://github.com/wilk/microjob
- https://github.com/hshoff/vx
- https://github.com/diegohaz/constate