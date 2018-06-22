# A Simple Chat Server
A simple chat server build entirely with node.js a test server is available at
chat.techcentroid.com/ room id
It can be anything you want
eg: chat.techcentroid.com/123
Then share that URL with your friend so that they can join your room.

**Environment Requirements**
1. Node (version 0.9.5 because this repo old af)
2. npm (version >2, caveats below)

**Running a development environment**
1. `npm install`
2. `npm start`

**Deployment**
1. Ensure you have access to `spartannomadlist-chat` on heroku
2. Login to `heroku-cli`
4. Add `spartannomadlist-chat` as a git remote
3. Run `git push heroku master`

**API**
- `/` - shows a landing page for the chat
- `/:slug` - any arbitrary slug will create a new chatroom that people can join

**Caveats**
This was a fork of a 6+ year old repo so some things are Bad.
For example, you'll get Path errors if you try to run this on any newer versions of node. To bypass this you can either:
- Use node 0.9.5 and npm 1.x, but set the npm registry to use the nonsecure http://registry.npmjs.org/ version (what we're doing in prod)
- Use a modern version of node/npm to install deps, and use something like [nvm](https://github.com/creationix/nvm) to install the old version of node and run the app with `<path>/<to>/.nvm/v0.9.5/bin/node app.js`
