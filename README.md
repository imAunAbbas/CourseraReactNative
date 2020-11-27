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

### To set a local server i.e. `json-server`

1. To implement the server locally, you need to install `json-server` in your PC globally. Simply run `sudo npm install json-server -g`.
2. Place the given `json-server` folder into your Documents folder and run `json-server --watch db.json -p 3001 -d 2000` in that folder directory.
3. Once your server is started, you can access data in your browser like this: e.g. `localhost:3001/dishes`.

`Note:`
If you are unable to access the server by using your IP address, then run this intead: `json-server --host <Your_IP> --watch db.json -p 3001 -d 2000`
