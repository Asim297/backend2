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

# develop models (user and video)
# npm i mongoose-aggregate-paginate-v2 for models aggregation
# import mongooseaggregationpagination in video model and use it.
# Like videoSchema.plugin(mongooseAggregatePaginate);
# install bcrypt and jsonwebtoken and import in usermodal . we can use it with middlewares like pre
# read mongoose middlewares 
# Write below code for encpyt password and compare password in usermodel
<!-- userSchema.pre("save", async function (next) {
  if (!this.isModified("password")) {
    next();
  }
  const salt = await bcrypt.genSalt(10);
  this.password = await bcrypt.hash(this.password, salt);
  next();
});

userSchema.methods.matchPassword = async function (enteredPassword) {
  return await bcrypt.compare(enteredPassword, this.password);
}; -->
# work on jwt update .env
<!-- ACCESS_TOKEN_SECRET=chaiaurcode
ACCESS_TOKEN_EXPIRY = 1d

REFRESH_TOKEN_SECRET=chaiaurcode2
REFRESH_TOKEN_EXPIRY=10d -->
# type in userschema.methed
<!-- userSchema.methods.getSignedJwtToken = function () {
  return jwt.sign(
    {
      id: this._id,
      email: this.email,
      username: this.username,
      fullname: this.fullname,
    },
    process.env.ACCESS_TOKEN_SECRET,
    {
      expiresIn: process.env.ACCESS_TOKEN_EXPIRY,
    }
  );
};
userSchema.methods.getRefreshSignedJwtToken = function () {
  return jwt.sign(
    {
      id: this._id,
    },
    process.env.REFRESH_TOKEN_SECRET,
    {
      expiresIn: process.env.REFRESH_TOKEN_EXPIRY,
    }
  );
}; -->
#
#