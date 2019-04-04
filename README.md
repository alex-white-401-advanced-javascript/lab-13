#### Requirements
* Install the core bearer authorization system
  [x] middleware.js - Handle the Bearer Header to pull and verify with the token
  [x] users-model.js - Add a bearer authorization method that verifies the token
* Improve the core bearer authorization system…
  [x] Alter the JWT to be time sensitive (valid for 15 minutes)
  [x] Alter the JWT to be single-use
    [] With every authenticated access, re-send a new JWT token as a cookie or header
    [] Disable those that you’ve already authenticated
* Create a Auth Key system
  [] Create a new route: router.post('/key' ... ) that will generate a JWT without an expiration date, and noted to be an auth key (so that it won’t be deleted like a single use token)
  [] Allow users to authenticate using the Auth Key as they would a normal token
  [] Auth Keys should never expire
  [] Auth Keys should be re-usable