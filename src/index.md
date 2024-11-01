---
sql:
   nations: ./data/nations.json
---

```sql id=idpop display
SELECT population FROM nations WHERE name='Netherlands'
```

```js
const p = JSON.parse(idpop);
const r = p[0].population;
// const g = Plot.line(r).plot();

const g = Plot.plot({
    x: {grid: true, label: "year", transform: (d) => d, tickFormat: d3.format('.0f')},
    y: {grid: true, label:"population (x1.000.000)", transform: (d) => d / 1e6, tickFormat: d3.format('.0f')},
    marks:[
        Plot.line(r)
    ]
});

display(g);
```



[//]: # ()
[//]: # (<div class="hero">)

[//]: # (  <h1>.\funfunfunction</h1>)

[//]: # (  <h2>Welcome to your new app! Edit&nbsp;<code style="font-size: 90%;">src/index.md</code> to change this page.</h2>)

[//]: # (  <a href="https://observablehq.com/framework/getting-started">Get started<span style="display: inline-block; margin-left: 0.25rem;">↗︎</span></a>)

[//]: # (</div>)

[//]: # ()
[//]: # (<div class="grid grid-cols-2" style="grid-auto-rows: 504px;">)

[//]: # (  <div class="card">${)

[//]: # (    resize&#40;&#40;width&#41; => Plot.plot&#40;{)

[//]: # (      title: "Your awesomeness over time 🚀",)

[//]: # (      subtitle: "Up and to the right!",)

[//]: # (      width,)

[//]: # (      y: {grid: true, label: "Awesomeness"},)

[//]: # (      marks: [)

[//]: # (        Plot.ruleY&#40;[0]&#41;,)

[//]: # (        Plot.lineY&#40;aapl, {x: "Date", y: "Close", tip: true}&#41;)

[//]: # (      ])

[//]: # (    }&#41;&#41;)

[//]: # (  }</div>)

[//]: # (  <div class="card">${)

[//]: # (    resize&#40;&#40;width&#41; => Plot.plot&#40;{)

[//]: # (      title: "How big are penguins, anyway? 🐧",)

[//]: # (      width,)

[//]: # (      grid: true,)

[//]: # (      x: {label: "Body mass &#40;g&#41;"},)

[//]: # (      y: {label: "Flipper length &#40;mm&#41;"},)

[//]: # (      color: {legend: true},)

[//]: # (      marks: [)

[//]: # (        Plot.linearRegressionY&#40;penguins, {x: "body_mass_g", y: "flipper_length_mm", stroke: "species"}&#41;,)

[//]: # (        Plot.dot&#40;penguins, {x: "body_mass_g", y: "flipper_length_mm", stroke: "species", tip: true}&#41;)

[//]: # (      ])

[//]: # (    }&#41;&#41;)

[//]: # (  }</div>)

[//]: # (</div>)

[//]: # ()
[//]: # (---)

[//]: # ()
[//]: # (## Next steps)

[//]: # ()
[//]: # (Here are some ideas of things you could try…)

[//]: # ()
[//]: # (<div class="grid grid-cols-4">)

[//]: # (  <div class="card">)

[//]: # (    Chart your own data using <a href="https://observablehq.com/framework/lib/plot"><code>Plot</code></a> and <a href="https://observablehq.com/framework/files"><code>FileAttachment</code></a>. Make it responsive using <a href="https://observablehq.com/framework/javascript#resize&#40;render&#41;"><code>resize</code></a>.)

[//]: # (  </div>)

[//]: # (  <div class="card">)

[//]: # (    Create a <a href="https://observablehq.com/framework/project-structure">new page</a> by adding a Markdown file &#40;<code>whatever.md</code>&#41; to the <code>src</code> folder.)

[//]: # (  </div>)

[//]: # (  <div class="card">)

[//]: # (    Add a drop-down menu using <a href="https://observablehq.com/framework/inputs/select"><code>Inputs.select</code></a> and use it to filter the data shown in a chart.)

[//]: # (  </div>)

[//]: # (  <div class="card">)

[//]: # (    Write a <a href="https://observablehq.com/framework/loaders">data loader</a> that queries a local database or API, generating a data snapshot on build.)

[//]: # (  </div>)

[//]: # (  <div class="card">)

[//]: # (    Import a <a href="https://observablehq.com/framework/imports">recommended library</a> from npm, such as <a href="https://observablehq.com/framework/lib/leaflet">Leaflet</a>, <a href="https://observablehq.com/framework/lib/dot">GraphViz</a>, <a href="https://observablehq.com/framework/lib/tex">TeX</a>, or <a href="https://observablehq.com/framework/lib/duckdb">DuckDB</a>.)

[//]: # (  </div>)

[//]: # (  <div class="card">)

[//]: # (    Ask for help, or share your work or ideas, on our <a href="https://github.com/observablehq/framework/discussions">GitHub discussions</a>.)

[//]: # (  </div>)

[//]: # (  <div class="card">)

[//]: # (    Visit <a href="https://github.com/observablehq/framework">Framework on GitHub</a> and give us a star. Or file an issue if you’ve found a bug!)

[//]: # (  </div>)

[//]: # (</div>)

[//]: # ()
[//]: # (<style>)

[//]: # ()
[//]: # (.hero {)

[//]: # (  display: flex;)

[//]: # (  flex-direction: column;)

[//]: # (  align-items: center;)

[//]: # (  font-family: var&#40;--sans-serif&#41;;)

[//]: # (  margin: 4rem 0 8rem;)

[//]: # (  text-wrap: balance;)

[//]: # (  text-align: center;)

[//]: # (})

[//]: # ()
[//]: # (.hero h1 {)

[//]: # (  margin: 1rem 0;)

[//]: # (  padding: 1rem 0;)

[//]: # (  max-width: none;)

[//]: # (  font-size: 14vw;)

[//]: # (  font-weight: 900;)

[//]: # (  line-height: 1;)

[//]: # (  background: linear-gradient&#40;30deg, var&#40;--theme-foreground-focus&#41;, currentColor&#41;;)

[//]: # (  -webkit-background-clip: text;)

[//]: # (  -webkit-text-fill-color: transparent;)

[//]: # (  background-clip: text;)

[//]: # (})

[//]: # ()
[//]: # (.hero h2 {)

[//]: # (  margin: 0;)

[//]: # (  max-width: 34em;)

[//]: # (  font-size: 20px;)

[//]: # (  font-style: initial;)

[//]: # (  font-weight: 500;)

[//]: # (  line-height: 1.5;)

[//]: # (  color: var&#40;--theme-foreground-muted&#41;;)

[//]: # (})

[//]: # ()
[//]: # (@media &#40;min-width: 640px&#41; {)

[//]: # (  .hero h1 {)

[//]: # (    font-size: 90px;)

[//]: # (  })

[//]: # (})

[//]: # ()
[//]: # (</style>)
