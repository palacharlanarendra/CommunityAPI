
## Testing Community API with SUPERTEST and JEST

Navigate to the below-shown folder, to test the API.  

```
CommunityAPI/Community_API_TESTS_WITH_JESTS/
```

### Install Required NPM packages

All the packages required for the testing will installed with below command
```
npm install 
```
or else

```
npm install -g nodemon (install nodemon globally)

npm install jest

npm install supertest --save-dev
```
we are testing the API endpoints with supertest in the jest environment.

### Config the JSON file
```JSON
{
  "name": "communityforumapi",
  "version": "0.0.0",
  "private": true,
  "scripts": {
    "start": "nodemon ./bin/www",
    "test": "jest"
  },
  "dependencies": {
    "bcryptjs": "^2.4.3",
    "cookie-parser": "~1.4.4",
    "debug": "~2.6.9",
    "express": "~4.16.1",
    "http-errors": "~1.6.3",
    "jade": "~1.11.0",
    "jsonwebtoken": "^8.5.1",
    "lodash": "^4.17.21",
    "mongoose": "^5.13.0",
    "morgan": "~1.9.1",
    "slugger": "^1.0.1"
  },
  "devDependencies": {
    "jest": "^27.2.0",
    "supertest": "^6.1.6"
  }
}

```
### Run the tests file.

Drop the mongo database every time, before you run tests using jest.
```
use communityForum 

dropDatabase();
```


Hurray! you are almost there, use this command to see the magic.
```JSON
npm run test
```
You can see total 23 Endpoints can be passed successfully.
```JSON
 PASS  ./user.test.js
  ✓ user register (400 ms)
  ✓ user login (9 ms)
  ✓ Get Current User Detail (8 ms)
  ✓ Get Current User Detail (95 ms)
  ✓ Update profile (16 ms)
  ✓ Follow user (29 ms)
  ✓ Unfollow user (16 ms)
  ✓ Create  a new Question (21 ms)
  ✓ Get Current User Detail (9 ms)
  ✓ Update Question using Id (21 ms)
  ✓ Create New Answer (20 ms)
  ✓ Get All the List of Answers (13 ms)
  ✓ Upvote the Question (15 ms)
  ✓ Delete the Upvote of the question (14 ms)
  ✓ Create a Comment on your question (17 ms)
  ✓ Update Answer using Id (14 ms)
  ✓ Upvote the Answer (12 ms)
  ✓ Create New Answer (22 ms)
  ✓ Delete the Answer (14 ms)
  ✓ Create an new Comment (23 ms)
  ✓ Get all the list of avaialable Tags (10 ms)
  ✓ Delete question using the slug (10 ms)
  ✓ Delete Answer using answerId (17 ms)

Test Suites: 1 passed, 1 total
Tests:       23 passed, 23 total
Snapshots:   0 total
Time:        1.595 s, estimated 2 s
Ran all test suites.
```
### Video of executing tests successfully

https://github.com/palacharlanarendra/CommunityAPI/blob/main/Community_API_TESTS_WITH_JESTS/executing%20tests%20demo%20successfully.mp4
