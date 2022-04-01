# Node Backend Developer Assignment

Build a One Time Password(OTP) based signup server, where the user can signup for either Team Iron Man or Team Captain America.

### Requirements:

- The user should be able to signup using their country code and phone number
- As a first step, the user should be able to choose a team, 'ironMan' or 'captainAmerica' on the route in the post body. Return a JWT with validity for 24 hrs.
- The user should be able use the JWT and generate a OTP based on the unique combination of country code and phone number. Check for the phone number being 10 digits long in the post body. Return another JWT.
- To simulate sending of OTP, just print it on the console.
- The OTP should only be valid for 5 mins. (Suggestion: You can either use an expiring data entry in redis, or any other way you seem fit)
- Once the user has been authenticated, persist their team and their country code and phone number in the DB. Make sure to not have dublicate entries.

### Setting up your environment:

Install docker in your local environment:

You can follow the instructions as listed here:

- [Mac](https://docs.docker.com/docker-for-mac/install/)
- [Windows](https://docs.docker.com/docker-for-windows/install/)
- [Linux](https://docs.docker.com/engine/install/)

To levarage typescript based suggestions, run `npm install` inside the auth directory.

To start the server, and databases run `docker-compose up --build` in the root directory of the project.

We have included some suggestive skaffold directory structure and code in the auth directory. Feel free to build upon that or use any other structure you want.
