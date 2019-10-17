## Scaffolding

I like to set up all my project dependencies up front with a check list and ensure the back-end and front-end are connected. I do this in the master branch and then run branches for development of features, bug fixes, etc.

### Front-end libraries
[npx create-react-app]
[npm install tachyons -S] (installs tachyons) A CSS tool-kit for rapid styling (tachy is the Greek word for rapid!) They are responsive based on mobile-first design,  with low-specificity that can be overwritten and excellent documentation [http://tachyons.io/docs/] to experiment with - ideal for quick mock-ups and M

### Back-end dependencies and libraries
[npm install node nodemon express request-promise cors dotenv -S]
1. [npm install node -S]  (adds node.js)
2. [npm install nodemon -S] (adds hot loading of backend server with nodemon)
3. [npm install express -S] (install express midware - ajax and body-parser inbuilt)
4. [npm install request-promise -S] [npm install request] (sets up back end API to get methods of request-promise from ES-6)
5. [npm install cors] enables cross-origin-resource-sharing, prevents resource blocking
6. [npm install dotenv] enables saving of passwords, files with keys for access

Connect back-end and front-end
[npm install npm-run-all]

## Set up file structure

Compartmentalize the back-end and front-end src files, in the front-end I set up common and app-pages as 2 folders. Common sets up all components that are reusable across multiple pages - nav bars, buttons, search bars, scrolly-bars, etc. The app-pages are purely for the app and all feed into App.js which then feeds into index.js.

The back-end I have server.js to set up the server files with the basic documentation from express
```
const express = require('express');
const app = express();
const port = 3000;

app.listen(port, () => console.log(`chat-app listening on ${port}`));
```

In the front-end I set up an app.js component with a hello-world tag to check it is is complining, I also add hello world to components in the common folder after that.