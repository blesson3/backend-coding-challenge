<img src="http://i.giphy.com/kCVIL0CLNWv2E.gif" height="100"/>

### Philosophy

The goal of this challenge is to get insight on how you approach an everyday task, not a hypothetical algorithm unicorn puzzle of doom. Complete the challenge by writing code that you would write again any day and pick up with ease 5 years from now. Basically, write code you're proud of.

### Values

- We highly value code cleanliness, reusability, structure and hierarchy.
- We make extensive use of code formatting, code reviews and tests.
- We are huge fans of popular 3rd party libraries, so use them when it makes sense to not re-invent the wheel but make sure you show us what you can do on your own.
- We are big fans of small, incremental commits, not 5,000 LoC `Initial Commit.` and `Added stuff.` monsters.
- We know StackOverflow et al. exist; getting inspiration from other sources is totally fine as long as you attribute them in your code.
- We delight our users with a familiar but fresh UX.

### Time Limit

The task is doable in a half day over the weekend. It is OK to leave reasonable TODOs in the code when you run out of time or took a shortcut, just explain yourself.

Overall, please complete this challenge within ≈2 weeks of receiving it, unless you've been given a different time limit.

### The Challenge

1. Implement the following endpoints using the Node JS framework.
2. Provide SQL for how the MySQL database should be setup.
3. Provide tests for the `/users` endpoints only. You may use any testing framework you're familiar with.

#### Endpoints

    GET /users                          -- returns all users in the database
    GET /users/:id                      -- gets the info about a specific user
    POST /users                         -- creates a new user
    DELETE /users/:id                   -- deletes a user gracefully

    GET /groups                         -- returns all groups with its members in the database
    GET /groups/:id                     -- gets the info about a specific group
    POST /groups                        -- creates a new group (specifying userIds for members, or something similar)
    POST /groups/:id/user/:userId       -- adds a user to a group
    DELETE /groups/:id                  -- deletes a group
    DELETE /groups/:id/user/:userId     -- removes a user from a group
    
#### Notes

Models:

    User -- id, name, address (ex. 283 RaspberryPi Ln, Cherry Town, CO)
    Group -- id, name, associated users (many to many relationship)

Other Notes:
- The term gracefully when deleting refers to the association between the users and groups being adjusted accordingly.
    - E.g. Erin, Bob, and Joe are in a group. If I remove Erin from the database and the group still exists, but now just Bob and Joe are in the group.
- MySQL database is the preferred database technology, but you may use what you're confortable with.
- You do not have to provide hosting, the zipped up project should have a README that contains comprehensive setup on a local machine.

**Note**: You should build this as if it were a real project that you had to maintain for the foreseeable future. You should ensure the user experience is balanced with the robustness and cleanliness of your code. We left this open ended, but it doesn't mean you should rush through it and just send something functional without any polish. This should be a direct representation of who you are.

When you're all done: 
- Commit it to a repo in your personal Github account that we can access (or zip the project and host it somewhere for us to download, _including_ the git history)
- Shoot us a quick email or message us in Angel.co letting us know you're done and we'll clone it and run it from our machines

### Review

When reviewing your submission, we'll be looking at the following (not necessarily in this order):

- Code Quality
  - Is the code reasonably easy to understand and well-organized (i.e. broken down into models, networking, views, controllers)? Could we plug our app into your code reasonably fast?
  - Is your code reasonably robust (i.e. what happens when the server returns errors or there is no internet connection and how do you display those to the user)?

- Functionality
  - Core functionality of searching and showing results
  - Accuracy of the returned results (easy to find something locally or far away)

- Experience
  - How does the user experience feel?