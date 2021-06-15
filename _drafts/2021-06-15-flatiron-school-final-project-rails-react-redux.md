---
published: false
---
# Rails, React, Redux oh my!

With my final project for FlatIron School finally completed I'm so excited to continue moving forward, learning, and building. This is a major milestone for me as I have put off completing this final project for far too long. Taking breaks of months at a time due to life getting in the way, work that doesn't really require the skills I've learned from the bootcamp I started back in September of 2018, and any other excuse I have used for not pushing myself. The final straw was a change in the Learn.co program which placed a deadline on completion in order to graduate and I couldn't possibly let myself down and not complete this program. For me it is a life accomplishment as it is for many other. Unlike many others, my current position doesn't allow me to really apply the skills learned, so it was for personal gain only at this point. Regardless of the reasons it's important to finish what you start and for that I am very happy.

So this application builds on 3 other projects I've sompleted for the program and I've progressivily improved them with each new project requirement. I started with a Sinatra application, next up was a Rails app, then Rails with Javascript, and now Rails with React and Redux. 

I am a firearms enthusiast and I wanted to create a tool that allows others to track how many rounds they have shot through a particular firearm barrel. The reason this is important specifically for those that shoot competitively is that barrels are a consumable and require replacement after having shot a number of rounds. Keeping track of shots is commonplace and there really wasn't a tool out there that is easy to use for tracking. Most just use a notebook or spreadsheet for keeping track and I wanted a better tool, one that I could continually improve and add additional functionality.

This was by far the most difficult project mainly due to the time I took to complete, constantly updated code from community contributed packages, and version changes that I continually had to deal with updating. This is inherent in the developer space as improvements are made and security vulnerabilities are dealt with.

With all of that out of the way let's talk about the app.

### Rails breakdown:
Using Rails 5.x I implemented a custom User authentication process with help from Jordan Hudgens using a cookie based approach that allows React to utilize the Rails API for authentication and authorization.

After setting up the User management piece I created migrations that allowed for the creation of the API that is accessible from the React app using JSON as an output via `fetch` requests made directly to the Rails API. When using Rails as a backend and React as a front end it requires running each app on a separate port so I utilized Foreman which allows a `rake` task to start both applications on separate port easily.

As previously mentioned I repurposed my previous Rails project so it saved some time on scaffolding the firearms, barrels, and outings data model and allowed me to focus more on the React portion of the app.

### React breakdown:
For the React application I again leaned on Jordan Hudgens to build out the User Registration and Login for authorization and authentication. With his tutorial I managed to piece together the User management and it works great for this small aplication using session cookies.

I used a mix of both Axios and Fetch for interacting with the Rails API to get a good mix of experience with multiple approaches to API interaction. Learning multiple paths help with real life situations where some projects you may encounter have different methods for everything.

The redux portion was the hardest part to wrap my head around and I'm still not 100% in my understanding but it is definintely an awesome tool for building more complex applications the require state to be managed in multiple components. 


I'm looking forward to continued learning of the latest and greatest that React has to offer but I'm really interested getting to know VueJs and other backend options like Firebase, and NodeJS.

Here's to continually learning and growing with code. Cheers!
