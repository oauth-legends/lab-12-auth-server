# OAuth Comparative Analysis

## OAuth Provider: Auth0

### Research Conducted By: Jonny, Guru, and Ai

### Overall Score and Comments
#### Score (Out of 10): 9
#### General Comments
Seems like a solid app that is well built and well-connected and accepted. HAs a breadth of social ID providers to work with and thoughtfully written to play nice with other services. Type in a serach and you are almost guaranteed to find docs on how to support that integration. I haven't been stumped yet, but I am also not a level 40 coding ninja.
The site is well organized. Design and interface are user friendly, as well as the product itself.

#### Pros
* Well laid out, thorough documentation
* Very user-friendly, almost no expereience necessary. Some experoence may cause you to overthink, enough experience may give you the opportunity to manuipulate the instructions to your own designs
* Comes with its own middleware, called Passport, so you really don't need to write any.

#### Cons
* Potentially needing to dig a bit deeper into Passport
* Due to preset, in-house dependecies you may have to work a bit harder to reconfigure outside of what they have set up

### Ratings and Reviews
#### Documentation
This is a pretty cool framework, and I think it has a lot of potential and versatility. Rather than being tied to a single provider you are covering an enormous user pool because of its ties with so many large networks (facebook, twitter, google, etc). It has been thoughtfully written to play nice with many services as well. Among them are AWS, Salesforce, and Azure. 
It was very easy to use once we let go of the demo code. That was the most difficult part. We walked in with preconcieved notions of how it ought to link up. 
This app is full stack, but there is a lot that goes unseen, due to outsourcing the work to Auth0's inhouse middleware: Passport. Had we more time I think it would've served us well to dip in and get spun up on the magic behind that. That being said, we were surprised to see some of their front end having been sourced from w3schools. 

#### Systems Requirements
Above and beyond 'node' and 'linux', you'll need the following to get up and running(which you can get from our package.json, see operatiing instructions below):

`passport` - an authentication middleware for Node.js

`passport-auth0` - an Auth0 authentication strategy for Passport

`express-session` - a middleware to manage sessions

`dotenv` - a module to load environment variables 

It seems to able to play well with other services including both AWS and Heroku. There doesn't appear to be any hard fast rules on database, you are allowed to bring in your own, and as mentioned several times throughout, it seems they make a conscious effort to smoothly connect with most services.

#### Ramp-Up Projections
According to John's estimate, if it takes us 4 hours it should take them about a week. It took us the four hours, but we wasted a bit of time coming at it from the wrong framework when we left the demo. I think we could've cut our time in half, therefor a team of junior/mid level devs could probably get setup in a couple days.

#### Community Support and Adoption levels
How popular is this framework? What big companies are running on it? How is it "seen" in the general JS community?  Is there an active community of developers supporting and growing it?
This seems to be a pretty well accepted framework. They have google, facebook, twitter, and github among their available social ID providers.

### Links and Resources
* [Auth0 website](https://auth0.com/)
* [Auth0 nodejs webapp docs](https://auth0.com/docs/quickstart/webapp/nodejs)
* [Youtube tutorial (47min)](https://www.youtube.com/watch?v=SJl5THmcQik)
* [Further reading: Passport](http://www.passportjs.org/docs/)

### Code Demos
* [live/running application](https://oauthlegends-apm.herokuapp.com/)
* [Auth0 webapp sample code repository](https://github.com/auth0-samples/auth0-nodejs-webapp-sample/tree/master/01-Login)

### Operating Instructions
In order to optimally run our app, you'll want to go ahead and create an Auth0 account (which is free to do, and you get 21 days of premium services). 
* In the dashboard, navigate to Applications
* set your Allowed Callback URLs to `http://localhost:3000/oauth`

Once you have our repo cloned down:
* Set up your .env file using the Domain, ClientID and Client Secret from the Auth0 Applications tab of your dashboard.
* `nodemon`
* Endpoint: `/`
  * Returns the homepage with a message: You are not logged in! Please Log In to continue.
* Endpoint: `/user`
  * Returns the user profile, containing `req.user`, once you have succesfully logeed in.
