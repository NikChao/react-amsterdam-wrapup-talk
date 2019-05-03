# Micro-frontends
### with Max Gallo

1. Why we need
- scaling a backend across teams -> microservices
- Monolith frontend
  - Same codebase for all teams
  - Communication overhead for code & impl
  - Infrastructure requires meetings/lots of communication


- Microfrontends
  - broken down frontends, teams can own one microfrontend. One business domain
  - each FE is self contained
  - teams get more autonomy
  - teams get more responsobility/freedom
  - innovation - less friction making upgrades



2. What are they
- Learn from others
  - OpenTable: open components (component lib tied to BE login session)
  - zalando: interface framework
  - spotify: iframes and event bus

- DAZN micro-fe maanifesto
  - indepeendent implementation, avoiding sharing logic
  - modelled around business domain
  - own by a single team




3. How they work under the hood
- Bootstrap
  - bring the user to the right micro-fe
  - user goes on www.dazn.com they get bootstrap.js/index.html (just a spinning logo)
  - bootstrap loads the microfrontend and handles lifecycle


Sharing components
- they have no shaerd code
- this makes me very sad
- big yikes

Deployment:
- built deployed separately