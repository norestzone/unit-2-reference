# Unit 2 Reference


## Setting Up Node Projects
1. Create folder for project and open VS Code
   - mkdir foldername

2. Initialize Node inside project
   - npm init or npm init -y

3. Create an entry point
   - touch index.js

4. Run the program
   - node index.js

5. Add .gitignore file
   - touch .gitignore or echo "node_modules" >> .gitignore
-----
## Using Express
1. Install express
    npm i express

2. Set Up Express and Create Home Route
   - const express = require('express'); const app = express (); app.get('/', (req, res) => {
    res.send('Hello, World!'); }); app.listen(8000);

   - Run nodemon
    nodemon
----
## Using EJS
1. Install ejs
   - npm i ejs

2. Set Up EJS and Add Route
   - app.get('/', (req, res)=>{ res.render('index.ejs'); });

3. NOTES:
   - When changing to ejs you must change file extensions from .html to .ejs
   - = means to render this from ejs
   - Every ejs line MUST be wrapped in esj tags
   - ***DO NOT COMMENT IN EJS***
----
## Using Layouts
1. Install ejs layouts
   - npm i express-ejs-layouts

2. Set Up EJS in index.js
   - const express = require('express'); const app = express(); const ejsLayouts = require('express-ejs-layouts');app.set('view engine', 'ejs'); app.use(ejsLayouts); app.listen(3000)


3. NOTES:
   - When changing to ejs you must change file extensions from .html to .ejs
   - = means to render this

4. Add a layout to the views folder called layout.ejs and ensure to name it layout.ejs, as mandated by express-ejs-layouts

5. Set up you DOC in you layout.ejs file and add <%- body %> in the body

6. Add a .ejs file that corresponds to the .js file and render
   - app.get('/', (req, res) => { res.render('home'); });

----
## Using Controllers
1. Change your route urls

2. Create a controllers folder and add corresponding files for routes

3. Change app. to router. get in your controller files

4. Implement middlewear by adding app.use on your index.js to route properly

5. Update your res.render to direct properly