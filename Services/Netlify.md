Netlify is mostly straight forward to used BUT if using with React apps make sure to adjust the following settings for your app in the Netlify app settings section:

Go into your app's "Build & Deploy" section of settings.
Look at the sub-section called "Build Settings"

There are 2 feilds that are important:
1. Build Command
2. Publish Directory

IF using Ryans Metah's package:
set them as follows (but omit the quotation marks):
Build Command: "npm run build"
Publish Directory: "dist"

IF using create-reat-app package:
  *might need to run yarn build and remove build folder from gitignore
Build Command: "npm build"
Publish Directory: "build"


the npm run build part is pretty self explanitory.
the "dist" part is still a mystery to me, just do it.

