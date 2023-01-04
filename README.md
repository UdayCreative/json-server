# json-server

# Live Link : https://json-server-ob37.onrender.com/

# How to Create a json-server and how to deploy:

# json-server: 

1. Create the new repository on GitHub
2. Clone the repository in your system
3. npm i json-server
4. npm init -y
5. Create the db.json file or type this command in your terminal json-server --watch db.json
6. Create the index.js or server.js file whatever your want
7. package.json = write into depedencies "start":"node index.js"
8. following data add into index.js: 
    - const jsonServer = require('json-server');
    - const server = jsonServer.create();
    - const router = jsonServer.router('db.json');
    - const middlewares = jsonServer.defaults();
    - const port = process.env.PORT || 8000; 
    - server.use(middlewares);
    - server.use(router);
    - server.listen(port);
9. Added node_modules in .gitignore file
10. git add . 
11. git commit -m 'commit the message'
12. git push origin 'branch-name'

# Deployment:

1. Open the render.com website and signup/signin and open dashboard.render.com
2. Click on new+ tab
3. Click on web service
4. Connect your repo with render
5. After that give the name your project 
6. Add node index.js
7. Click on Create a web server
8. It will redirects to dashboard and deployment starting
9. It will takes some time and then Deploy succeeded message shown on render dashboard
