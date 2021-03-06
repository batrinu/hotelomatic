# Hotelomatic

This a basic crud react-redux-featherjs application for managing guest check-ins. It currently uses NeDB for the database and FeathersJS for the REST API server. 

##  How to install

```bash
git clone git@github.com:batrinu/Hotelomatic.git
cd hotelomatic

# Install client dependencies
cd client
npm install
# or
yarn

# Install server dependencies
cd server
npm install
# or
yarn
```


## How to run
Ensure you have node installed on your system
```bash
node -v
npm -v
# or
yarn -v
```

### Start the backend server
Start the backend server first:

```bash
cd hotelomatic/server
npm start
# or
yarn start
```
This will run the backend server at localhost:3030. If all is working well, you should be able to access the url http://localhost:3030 from your Browser or Postman

### Start the client
Open a separate terminal to start the client:

```bash
cd hotelomatic/client
npm start
# or
yarn start
```

Your default web browser will be launched automatically with the url http://localhost:3000

### Create a staff member account

Open a terminal and run:

```bash
curl 'http://localhost:3030/users/' -H 'Content-Type: application/json' --data-binary '{ "email": "staff@hotelomatic.com", "password": "admin1234", "userType": "staff" }'
```
Open a browser and go to http://localhost:3000/signin




## Future todos

- [ ] Add backend form validation hook
- [ ] Choose a DB (something other than NeDB)
- [ ] Wrap '/checkins' service in Auth layer
- [ ] Decide redux-form VS formik
- [ ] Create action and reducer files for each component
- [x] Fix LF ... CRLF errors
- [x] Fix client eslint errors