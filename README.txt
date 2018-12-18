CampusNet Project reference material details and links.


For the development of this project, I have used some javascript libraries and frameworks along with my knowledge of vanilla javascript coupled with HTML5 and CSS. Throughout the development process I have learned with practical hands-on and the official documentation for the libraries. One particular resource called Udemy has been of great help as I had enrolled into its Web developer bootcamp and complete node developer course. 

Udemy is an online learning platform with video lectures, challenge quizz and hands on mini project.
 
Following is the detailed report of all the resources and the materials used and modifications done.

Reference mataterial and courses for Database using Node js

The step by step video lecture from udemy was where i learned to build the database along with Express js for communicating with front end.


https://www.udemy.com/the-complete-nodejs-developer-course-2/learn/v4/t/lecture/5525250?start=0


Udemy web developer course reference for front end with Angular and Bootstrap

For the front end I used the Boilerplate code template from Bootstrap documentation and example. 

Modifications:- I made changes to the Navbar code and added the container class for wraping the Navbar in the frame. I also added the fade option in the css for the navbar. I added signup and login options in the original navbar to give the required look and options. I added glyphicons component to customize the look.
http://getbootstrap.com/docs/3.3/components/#navbar

With the above modifiation, I folowed the video instruction in webdeveloper bootcamp for modifying the template bootstrap code for my specific needs.
https://www.udemy.com/the-web-developer-bootcamp/learn/v4/t/lecture/3861400?start=45

For the authentication I implemented JWT and OAuth protocol with the help form following.

https://www.toptal.com/web/cookie-free-authentication-with-json-web-tokens-an-example-in-laravel-and-angularjs

Modifications:- The boilerplate was in python for JWT authentication. I configured the similar auth class for Angular Js routing and extended the controller script file which handles the token parsing at the server. The above mentioned resource made it possible to configure jwt for AngularJs.
I implemented the JSON.stringify method to get the user token.
Also I added a controller for error handling in HTML for JWT.

Error handling code snipet.
success(message: string, keepAfterNavigationChange = false) {
       this.keepAfterNavigationChange = keepAfterNavigationChange;
       // this.subject.next({ type: 'success', text: message });
       this.popToastsuccess(message);
   }

   error(message: string, keepAfterNavigationChange = false) {
       /// this.keepAfterNavigationChange = keepAfterNavigationChange;
       this.popToasterror(message);
       //this.subject.next({ type: 'error', text: message });


Angular Js Resources

The routing fro the components was done with the help of following.

https://angular-templates.io/tutorials/about/learn-how-to-build-a-mean-stack-application

Modifications:- Extended the JWT authentication class for login routing. routing for authentication with username and password stored in DB. Added courseId view for routing from login to course.
Added components of the project.
Code snippet for authentication class extedted from JWT auth.
// Authenticate
router.post('/authenticate', (req, res, next) => {
    const username = req.body.username;
    const password = req.body.password;

    User.getUserByUsername(username, (err, user) => {
        if (err) throw err;
        if (!user) {
            return res.json({ success: false, msg: 'User not found' });
        }


Visualisation Using D3.js library.

D3 Js is an open source library for visualisation of data. I imported the core library in my project as dependency in the app.js file for angular cli and created a services folder for it.
Source Code
https://github.com/d3/d3
Implementation demos with source code
https://beta.observablehq.com/@mbostock/d3-sortable-bar-chart
https://plot.ly/javascript/pie-charts/

Modifications: The source code at the D3.js docs had an example of 2D pie chart and bar graph. I changed the SVG tag element and configured it to be three dimensional. This library can be viewed as a service in src folder for the project file.
Instead of scraping the data or manually providing the exxternal source i used POSTMAN service and POST method to insert data into the MongoDB database which gets stored in JSON file format by default.


Other reference resources for learning and debuging code.

https://docs.mlab.com/connecting/
https://stackoverflow.com/questions/53659511/error-in-error-metadata-version-mismatch-at-node-modules-ng2-smart-table-in?noredirect=1#comment94272278_53659511
https://github.com/feathersjs/authentication/issues/411
https://github.com/themikenicholson/passport-jwt/issues/117
https://codeburst.io/jwt-to-authenticate-servers-apis-c6e179aa8c4e

