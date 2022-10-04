# Class 08

These notes cover Role-Based Access Control and its potential uses.

## [5 steps to RBAC](https://www.csoonline.com/article/3060780/security/5-steps-to-simple-role-based-access-control.html)

### 1. What is Role Based Access Control (RBAC) and why do we care?
RBAC allows developers to protect certain resources or actions based on a role that can be assigned to each user of an application. For example, we can create an admin role that allows only certain trusted individuals to delete content from our site so that we can have non-technical people aid in moderating content without having to give them direct access to the database or code.

### 2. Describe a Role/Permission heirarchy that you might implement using RBAC.
A common heirarcy is Admin -> Moderator -> User -> Guest.

- Admin: Can view, create, edit, and delete any post. Can also delete user records, ban users, and unban users.
- Moderator: Can view, create and delete posts. Can also ban users, and maybe unban users.
- User: Can view and create posts. Maybe they can also edit and delete their own posts. Can also delete their own account/user record.
- Guest: Can only view posts.

### 3. What approach might you take to implement RBAC?
I would define some actions that the application might have built in, and then define roles around those actions. When users are created, I would assign one of those roles to the user. When an action is taken by a user, I would check to see if the necessary capability for that action exists inside of the user's role.

## [wiki - RBAC](https://en.wikipedia.org/wiki/Role-based_access_control)

### 1. If Authentication is “you are who you say you are,” what is Authorization?

Authorization is "You are allowed to do this thing." It is a check that happens after authentication, to tell us where or not the user has permission to perform a certain action or access a resource.

### 2. Name three primary rules defined for RBAC.

1. Role assignment - A user can only access something if they have a role.
2. Role authorization - A user's role must be authorized for them. Essentially, certain roles should be restricted. A user should not be able to just declare themselves an Admin.
3. Permission authorization - A user must have permission to access something or perform an action defined by their active role. Users cannot do things that their role does not give them permission to do.

## [RBAC tutorial](https://www.youtube.com/watch?v=C4NP8Eon3cA)

### 1. What are access rights associated with? The User? The role? Explain.

Access rights are associated with the role. A user is given a role, and that role contains permissions for certain actions or resource access methods. These can be broad or fine-grained, but there are trade-offs for each.

### 2. Access Rights, or authorization, is activated after a user successfully does what?
Authorization is activated after a user successfully authenticates. In other words, we can only determine whether a user has permission to do something if we first confirm that the user is who they say they are.

### 3. Explain how RBAC might benefit a business.
Well-built RBAC can help to offload content moderation to non-technical workers, or even volunteers. Take Reddit, for example. RBAC allows for the admin/moderator model that they use, where admins are typically Reddit employees with _many_ broad permissions site-wide, and moderators are typically volunteers that have permissions over a particular subreddit.  
Without RBAC implemented in this way, even the act of deleting a post that violates the rules or banning a user would require someone to access a database directly. If they wanted to expose that functionality on the front-end without RBAC, they'd have to create an entirely new dashboard that is protected from the public in some way _just_ to manage users and posts. 