# Coursera: Full-Stack Web Development with React

### The Hong Kong University of Science and Technology

## Course 3: Multiplatform Mobile App Development with React Native

At this point, avoided error by using:
This happened because the react-navigation use older version of SafeView.

You have 2 ways:

1. Long way: need to migrate to v5 react-navigation v4 to v5 migration.

2. Very fast and ugly solution:

Go to the dir `YOUR_PROJECT_PATH/node_modules/react-native-safe-area-view/index.js` and update:

from:

`this.view._component.measureInWindow((winX, winY, winWidth, winHeight) => {`

to:

`this.view.getNode().measureInWindow((winX, winY, winWidth, winHeight) => {`
