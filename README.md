# MERN Stack Project | Fullstack Tutorial by Dave Grey

Playlist for this MERN Stack Project Series: https://bit.ly/3Sn4EaI
All Resources for this MERN Stack Project: https://github.com/gitdagray/mern_stack_course

### 📚 MERN Stack References
- 🔗 [Official Site for MongoDB](https://mongodb.com)
- 🔗 [Official Site for Express.js](https://expressjs.com)
- 🔗 [Official Site for React.js](https://reactjs.org)
- 🔗 [Official Site for Node.js](https://nodejs.org/)

### 📚 Middleware References
- 🔗 [Express.js: Using Middleware](https://expressjs.com/en/guide/using-middleware.html)
- 🔗 [cookie-parser](https://www.npmjs.com/package/cookie-parser)
- 🔗 [cors](https://www.npmjs.com/package/cors)
- 🔗 [express-rate-limiter](https://www.npmjs.com/package/express-rate-limiter)

### 📚 React Router References
- 🔗 [Official Site for React Router](https://reactrouter.com/docs/en/v6)
- 🔗 [React Router v6 Tutorial](https://github.com/gitdagray/react_router_v6)

### 📚 Other React Dependencies
- 🔗 [Redux Toolkit](https://redux-toolkit.js.org/)
- 🔗 [FontAwesome Icons](https://fontawesome.com/docs/web/use-with/react/)
- 🔗 [React Spinners](https://www.npmjs.com/package/react-spinners)
- 🔗 [@fvilers/disable-react-devtools](https://www.npmjs.com/package/@fvilers/disable-react-devtools)

### 📚 Other Node.js REST API Dependencies
- 🔗 [date-fns](https://www.npmjs.com/package/date-fns)
- 🔗 [uuid](https://www.npmjs.com/package/uuid)
- 🔗 [dotenv](https://www.npmjs.com/package/dotenv)
- 🔗 [MongooseJS](https://mongoosejs.com/)
- 🔗 [mongoose-sequence](https://www.npmjs.com/package/mongoose-sequence)
- 🔗 [express-async-handler](https://www.npmjs.com/package/express-async-handler)
- 🔗 [bcrypt](https://www.npmjs.com/package/bcrypt)
- 🔗 [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken)
- 🔗 [express-async-errors](https://www.npmjs.com/package/express-async-errors)

--- 

## User Stories
- [UserStories.md](UserStories.md)

## To Start 
- npm run dev [starts in nodemon]
- npm run start [starts in normal mode]

### Lesson 1
- [terminal] npm i -y 
- [terminal] npm i express
- [terminal] npm i nodemon -D
- open browser to http://localhost:3500/
- add .gitignore (node_modules)
- [terminal] initiate git
- package.json scripts [
  "main": "server.js",
  "start": "node server",
  "dev": "nodemon server"
]
- server.js
- public/css/style.css
- routes/root.js
- views/index.html
- views/404.html
- set up 404 routing in server.js
---

### Lesson 2
- [server.js] add app.use(express.json());
- create logs & middleware folders
- [terminal] npm i date-fns uuid
- create middleware/logger.js
- add logs to gitignore
- [server.js] add logger
- create middleware/errorHandler.js
- [server.js] add errorHandler
- [terminal] npm i cookie-parser
- [server.js] add cookieParser
- [terminal] npm i cors
- create config folder
- create config/allowedOrigins.js
- create config/corsOptions.js
- [server.js] add cors, corsOptions, app.use(cors(corsOptions));
---

### Lesson 3
- [terminal] npm i dotenv
- create .env
- add .env on gitignore
- [server.js] add console.log(process.env.NODE_ENV);
- create MongoDB @ mongodb.com
- [terminal] npm i mongoose
- create models/User.js
- create models/Note.js
- [terminal] npm i mongoose-sequence
- create config/dbConn.js
- [server.js] add connectDB, mongoose, logEvents, mongoose.connection.once & mongoose.connection.on
---

### Lesson 4
- [server.js] add app.use('/users'
- create controllers/userController.js
- create routes/userRoutes.js
- [terminal] npm i express-async-handler bcrypt
---

### Create notesController
- [server.js] add app.use('/notes'
- create controllers/notesController.js
- create routes/noteRoutes.js
- [terminal] Change mongoose 7 to mongoose 6.12.0 - npm install mongoose@6.12.0 - mongoose-sequence doesn't work with mongoose 7+
---

### Lesson 5
- [terminal] in technotes folder, npx create-react-app frontend
- [terminal] cd frontend, npm i react-router-dom
- Update index.js with BrowserRouter, Routes, & Route to App
- Update App.js with Routes, and Route to Layout
- create src/components/Layout.js
- create src/components/Public.js
- create DashLayout.js, & DashHeader.js, import them into App.js and add Route for them
- [terminal] npm i @fortawesom/fontawesom-svg-core @fortawesome/free-solid-svg-icons @fortawesome/react-fontawesome
- create DashFooter.js
- create src/features/auth
- move Login.js to auth
- create Welcome.js & update App.js to use it
- create src/features/notes
- create NotesList.js
- src/features/users
- create UsersList.js
- update App.js to use them
---

### Lesson 6
- in frontend folder, npm i @reduxjs/toolkit react-redux
- update index.css with provided code
- create src/app/api/apiSlice.js
- create src/app/store.js
- update index.js to use them
- create src/features/users/usersApiSlice.js
- create src/features/notes/notesApiSlice.js
- fill out UsersList.js
