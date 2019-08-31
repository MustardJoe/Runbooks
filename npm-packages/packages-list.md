react-redux
  -react bindings are not explicitly included in redux, they must be manually  installed. this is the package that contains those bindings (for using    redux in react).

@babel/node
  -VERRY COOL _ ITS LIKE A REPL KINDA BUT CAN DO IN TERMINAL!!!!!!!!!
  -lets me run 'browser files' in node
  -dev dependency, so install with npm i -D @babel/node
  -then run file with npx babel-node ${fileName}

react-router-dom
  -for making SPAs
  -cool package for 'routing' in react
  -there are downsides to client side rendring(it,s slow, not mobile friendly), so don't forget this
  -but overall it's pretty cool

------------PROJECT INIT PACKAGES----------------

  alchemy-be
    package sets up JavaScript backend project with Node, Express, MongoDB/Mongoose and more
    use => npm init alchemy-be ${projectFolderName}
    create GitHub repo (no readme) after
  
  alchemy-react
    package sets up JavaScript front end project with React
    use => npm init alchemy-react ${projectFolderName}
    create GitHub repo (no readme) after