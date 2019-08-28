# Source maps

# Comment 1

in production build, we should prioritize performance over information (if any error is happening on prod).
By using devtool: source-map on production, there are pro and cons:

pro:
  - we will get the information if user face an error on production
cons:
  - user need to download extra file (.map) which is reduce the web load performance
  - our code will be visible for every user (risky if the user is a deveoper)

but actually there is some way to do source-map on production without allowing user to download the extra file (.map), but this needs to do more research

So the conclusion, it would be best to use devtool: none in production
devtool: eval or cheap-eval-source-map in development. 

Resources:
- https://webpack.js.org/configuration/devtool/