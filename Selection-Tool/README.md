# bbm479

# Important
To set env change env file to env
here is content of .env


"SKIP_PREFLIGHT_CHECK=true
CI=false yarn build
REACT_APP_SUPABASE_URL="URL"
REACT_APP_SUPABASE_ANON_KEY="SECRET"
REACT_APP_GOOGLE_SHEET_URL="sheet best"
REACT_APP_TOOL_URL="AHP-Tool Link""

# Adding &  Deleting 
You can add or delete via this [Add](https://bbm479.vercel.app/admin/add) & [Delete](https://bbm479.vercel.app/admin/delete) These are deployment's links the password is different than usual one if you want to access local you can check out these routese /admin/add and admin/delete

Important Note" The submit pages only for gathering request from users not for adding or deleting please be might while using the application.

Note 2: Default password is "pass"

## First App
Notes if db is not working:
ALTER SEQUENCE dataset_id_seq RESTART WITH 9;

Or some id. You should run this command in db.
## Submit Page
You can see incoming requests via "Submit" at here 
[Here is Google Sheet Link](https://docs.google.com/spreadsheets/d/1vM2VbZycjqfGiDUFEYNqw0wh-ndTA0aeCd4kamAhd3E/edit?usp=sharing)
## Admin Panel
- /admin/delete
- /admin/add
- /admin/login (it is temp page) and routes to delete
The application store basic seassion so you don't have to enter password again and again

------------
#### Steps to  build project 
Requirements:
Node and nvm should be installed
- Node version should be 16.10.0
---------------------------------
- `nvm install 16.10.0`
- `clone the project`
- `nvm use 16.10.0`
- `yarn install` it will take a little bit time
- `yarn start` you can start the project

### Note SQL Definition

create table
  public.dataset (
    id bigint generated by default as identity not null,
    title text null,
    CommentAbout text null,
    LinkToMD text null,
    category text null,
    type array null,
    rating bigint null,
    price double precision null,
    coverSrc text null,
    score array null,
    customType array null,
    constraint dataset_pkey primary key (id),
    constraint dataset_id_key unique (id),
    constraint dataset_title_key unique (title)
  ) tablespace pg_default;

### Note Admin Password 
Default password is: "pass"
You can change it in "AdminLogin.js"


