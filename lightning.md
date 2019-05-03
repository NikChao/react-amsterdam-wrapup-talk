# Next for Next

- Optimizes for prod
- For the mobile web

MDX 1.0
- Reliable PArsing
Smaller MDX output docs
prettier support
mdxjs.com

# Lighning fast SSR React app with no client side JS

- even after SSR, waiting for react - Time to interactive
- Uncanny valley from paint to TTI
- Looks interactive eh? aka LIE
- Can be decent with fiber/3g gets sloooowww
- Removing all clientside react got netflix +50% perceived perf (halved TTI)
- Cristalize 3g test
  - SSR w/ client side js -> 6.6s LIE
  - withouth clientside JS -> 2.5s LIE
- Always test for Uncanny Valley

# Faster SSR

- github.com/esxjs (faster algo than NextJS's caches)
- node bench (autocannon)
- lower latency, more req/s, higher throughput

- SSR can be slow, because even though you hit the same path many times, you end up blocking the main thread loop
- key trick to esxjs is that it tagged templated literals
  - instead of creating a tree, then rendering, you keep it flat, similar to older tempalting engines

  ```jsx
    render () {
      return esx`
        <Box>
          {/** content */}
        </Box>
      `;
    }
  ```

  - `node -r esx/optimize app.js*`
  - babel plugin rather than preloader
    - babel-plugi-esxjs

# Demystifying SSRendered react apps

- SEO factors into SSR
- Perf win -> UX win
