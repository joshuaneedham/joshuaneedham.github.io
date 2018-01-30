---
published: false
---
## DownTheTu.be Sinatra App

Right after I finished my CLI gem project I began thinking about a project idea that I could build on moving forward through the Learn.co Full Stack Developer Program. There are several projects required to complete the curriculum and I really want to end up with something that could be turned loose into the wild for the public to use.

With that being said I am setting out to build an app that will allow any firearms owner to track the number of rounds shot from each of their firearms. For competitive shooters, it is very important to know how many rounds have been shot through each barrel used. For others, it's just a nice piece of information that can be utilized for proper firearm maintenance and what not.

Enter ## DownTheTu.be
![down-the-barrel.jpg]({{site.baseurl}}/_posts/down-the-barrel.jpg)


The basics of the application include:

User - Fields to include Username, Email, Password
  * Create
  * Login
  * Logout

Firearm - Fields to include Name, Round Count(number of rounds fired)
  * Create
  * Show
  * Edit
  * Delete

A user `has_many` firearms and firearms `belong_to` users. Users only have access to their own firearms which can be updated or deleted and there is no limit to the number of firearms a user can add.

In the future I plan to add many more features to the app as I progress through Flatiron's program. It will eventually be a full fledged application that will include things like barrels for firearms, load data, ability to upload pictures of firearms, etc....

You can `git` the app [here](https://joshuaneedham.github.io/down-the-tube)



