# shinyloadtest examples

This is a repo showing examples of doing performance testing on a shiny applications deployed on Connect. 

You might also be interested in: <https://github.com/leesahanders/demo_app_perf/tree/main> 

It has slides: <https://questionable.quarto.pub/improving-app-performance-with-profvis/#/title-slide>

## Process

1. Deploy application to Connect
2. Install shinyloadtest (Node.js 20+, `npx shinyloadtest@next`)
3. Add environment variable
4. Create "Recording" of a typical user's interaction
5. Run load tests 
6. Analyze the results 

## Additional resources 

There are links to various additional and recommended resources sprinkled throughout, however here a few overview level recommendations: 

Benchmarking / profiling tools
-   Profiling your shiny app with [profvis](https://shiny.rstudio.com/articles/profiling.html), [shinyloadtest](https://github.com/rstudio/shinyloadtest), [shinytest2](https://rstudio.github.io/shinytest2/articles/use-application-audit.html#load-testing-with-shinytest2)
-   Plumber: [profvis](https://rstudio.github.io/profvis/)
-   More granular profiling with [microbenchmark](https://cran.r-project.org/web/packages/microbenchmark/index.html)
-   Dash: [Dash Dev Tools](https://dash.plotly.com/devtools) / [pyinstrument](https://pyinstrument.readthedocs.io/en/latest/guide.html#profile-a-specific-chunk-of-code)
-   Streamlit / Bokeh / Flask / FastAPI: [pyinstrument](https://pyinstrument.readthedocs.io/en/latest/guide.html#profile-a-specific-chunk-of-code)

[Mastering Shiny](https://mastering-shiny.org/performance.html)
[Shiny in production: Principles, practices, and tools](https://www.rstudio.com/resources/rstudioconf-2019/shiny-in-production-principles-practices-and-tools/)
[Scaling and Performance Tuning in RStudio Connect](https://support.rstudio.com/hc/en-us/articles/231874748-Scaling-and-Performance-Tuning-in-RStudio-Connect)
Simulate runtime settings and events: [Shimmer Shiny Sizing](https://colorado.rstudio.com/rsc/shimmer_and_shiny/)

### shinyloadtest

 - shinyloadtest (Node.js CLI) repo: <https://github.com/posit-dev/shinyloadtest>
 - shinyloadtest npm package: <https://www.npmjs.com/package/shinyloadtest>
 - shinyloadtest R package documentation (custom analysis of results): <https://rstudio.github.io/shinyloadtest/>
 - shinyloadtest R package repo: <https://github.com/rstudio/shinyloadtest/> 
 - Connect specific article: <https://rstudio.github.io/shinyloadtest/articles/load-testing-authenticated-apps.html>
 - Analyzing the results: <https://rstudio.github.io/shinyloadtest/articles/analyzing-load-test-logs.html> 

### shinytest2 

- shinytest2 main documentation: <https://rstudio.github.io/shinytest2/articles/use-application-audit.html#load-testing-with-shinytest2> 
- shinytest2 load testing: <https://rstudio.github.io/shinytest2/articles/use-application-audit.html?q=load%20test#load-testing-with-shinytest2> 
- <https://www.youtube.com/watch?v=Gucwz865aqQ>
- <https://www.youtube.com/watch?v=7KLv6HdIxvU>
- <https://github.com/schloerke/presentation-2022-07-28-rstudioconf22-shinytest2>
- <https://github.com/schloerke/presentation-2022-04-27-appsilon-shinytest2>
- <https://www.jumpingrivers.com/blog/end-to-end-testing-shinytest2-part-1/>

### CRAN whales case study 

- Cran whales: <https://rstudio.github.io/promises/articles/casestudy.html>
- Cran whales <talk: https://www.youtube.com/watch?v=Wy3TY0gOmJw>
- Cran whales article: <https://cran.r-project.org/web/packages/promises/vignettes/casestudy.html>
- Output: [https://rpubs.com/jcheng/cranwhales-etl](https://rpubs.com/jcheng/cranwhales-etl)
- Cranwhales app: <https://gallery.shinyapps.io/087-crandash/>
- Install it yourself: <https://github.com/rstudio/cranwhales>

### Related packages

 - Novartis developed shinyValidator: <https://github.com/Novartis/shinyValidator> 
 - shinyValidator slide deck: <https://appsilonconf2022.rinterface.com/?panelset3=package-your-app2&panelset4=what2&panelset5=purpose2#1> 
   - (Note that shinyValidator is not to be confused with shinyValidate which is used for input validation: <https://rstudio.github.io/shinyvalidate/> )
 - reactlog: <https://rstudio.github.io/reactlog/> 
 - shinytest2: <https://rstudio.github.io/shinytest2/articles/use-application-audit.html> 
 - Python load testing: <https://locust.io/> 


