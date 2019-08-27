react-redux
  -react bindings are not explicitly included in redux, they must be manually  installed. this is the package that contains those bindings (for using    redux in react).

@babel/node
  -lets me run 'browser files' in node
  -dev dependency, so install with npm i -D @babel/node
  -then run file with npx babel-node ${fileName}

------------PROJECT INIT PACKAGES----------------

  alchemy-be
    package sets up JavaScript backend project with Node, Express, MongoDB/Mongoose and more
    use => npm init alchemy-be ${projectFolderName}
    create GitHub repo (no readme) after
  
  alchemy-react
    package sets up JavaScript front end project with React
    use => npm init alchemy-react ${projectFolderName}
    create GitHub repo (no readme) after