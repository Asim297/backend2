# chai aur backend serires

This is a video serieson backend with javascript
# setup
# create src directry
# create app.js , index.js and constants.js files
# create folders... controllers,db,middleware,models,routes,utils.
# create public folder with temp folder and .gitkeep to upload in github
# create .env and .gitignore files out side of the src dirctory



# 1-connectdb
# 2- install cookie-parser and cors and import in app.js
  # conifigure middlewares:
   <!-- app.use( -->
  <!-- cors({
    origin: process.env.CORS_ORIGIN,
    credentials: true,
  })
);

app.use(express.json({ limit: "16kb" }));
app.use(express.urlencoded({ extended: true }));
app.use(express.static("public")); -->
<!-- app.use(cookieParser()); -->

# setup utils folder for ApiErrors, ApiResponse,asynHandler..need deepstudy