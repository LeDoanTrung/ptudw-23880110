# Installation and Application Setup Guide

## Student Information
- **Full Name**: Lê Doãn Trung  
- **Student ID**: 23880110  

## Installation Steps

### Step 1: Install Node.js and npm
```bash
sudo apt-get install nodejs npm
```

### Step 2: Install pnpm
```bash
sudo npm install -g pnpm
```

### Step 3: Install required libraries
```bash
pnpm -s install express
pnpm i -s express-handlebars
pnpm i -s express-handlebars-paginate
pnpm i -s express-session
pnpm i -s express-validator
pnpm i -s jsonwebtoken node-mailjet
pnpm i -s passport passport-local bcrypt connect-flash
pnpm i -s pg pg-hstore sequelize
pnpm i -s dotenv
```

### Step 4: Install Sequelize CLI
```bash
sudo npm i -g sequelize-cli
```

### Step 5: Initialize the project
```bash
npm init -y
sequelize init
```

### Step 6: Run migrations and seed data
```bash
npx sequelize-cli db:migrate
sequelize db:seed:all
```

### Note: Handling bcrypt-related errors
If you encounter a bcrypt model error, run the following commands:
```bash
sudo npm install -g node-pre-gyp
cd node_modules/bcrypt
node-pre-gyp install --fallback-to-build
```

### Step 7: Run the application
```bash
npx nodemon
