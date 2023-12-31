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

### Lesson 1 - MERN Stack Project - Backend
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

### Lesson 2 - Middleware in a MERN Stack Project 
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

### Lesson 3 - MongoDB MERN Stack Tutorial
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

### Lesson 4 - MERN API Controllers & Routers 
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

### Lesson 5 - React.js App Project
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

### Lesson 6 - MERN Stack Project with React Redux and RTK Query
- in frontend folder, npm i @reduxjs/toolkit react-redux
- update index.css with provided code
- create src/app/api/apiSlice.js
- create src/app/store.js
- update index.js to use them
- create src/features/users/usersApiSlice.js
- create src/features/notes/notesApiSlice.js
- fill out UsersList.js
- create User.js
- fill out Notes.js
- create Notes.js
---

### Lesson 7 - React Forms with Redux & RTK Query 
- update usersApiSlice.js with addNewUser, updateUser, deleteUser
- update notesApiSlice.js with addNewNote, updateNote, deleteNote
- create NewUserForm.js & EditUser.js as placeholders
- create NewNote.js & EditNote.js as placeholders
- add Routes to App.js
- create src/config/roles.js
- create Prefetch.js
- in App.js, wrap path dash in Prefetch
- in UsersList.js, add refresh to useGetUsersQuery
- in NotesList.js, add refresh to useGetNotesQuery
- in store.js, add setupListeners
- in Welcome.js, add links to add new user & note
- create NewNotesForm.js
- filled in NewNote.js
- create EditNoteForm.js
- filled in EditNote.js
---

### Lesson 8 - MERN Stack Authentication with JWT Access, Refresh Tokens, Cookies
- add app.use('/auth' to server.js
- create backend/routes/authRoutes.js
- [terminal] in backend 'npm i express-rate-limit'
- create backend/middleware/loginLimiter.js
- update authRoutes to have router.route('/').post(loginLimiter)
- create controller/authController.js
- [terminal] in backend 'npm i jsonwebtoken'
- update authRoutes to have router.route('/').post(loginLimiter, authController.login); & router.route('/refresh').get(authController.refresh); & router.route('/logout').post(authController.logout);
*
- add ACCESS_TOKEN_SECRET= & REFRESH_TOKEN_SECRET= to .env
- [terminal] node
- [terminal] require('crypto').randomBytes(64).toString('hex') gets you a random code. You need one for each TOKEN_SECRET
- create backend/controllers/authController.js
- create backend/middleware/verifyJWT.js
- noteRoutes.js & userRoutes.js - const verifyJWT & router.use(verifyJWT);
- 