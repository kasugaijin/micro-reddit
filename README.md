# README

This Ruby on Rails application consists of the backend only for a reddit-like use case. The purpose of this project was to solidify the concept of setting up models, migrations and associations between tables.
- the User model has many Posts and Comments
- the Post model belongs to User (user_id foreign key) and has many Comments
- the Comment model belongs to User (user_id foreign key) and Post (post_id foreign key)
- Each model has a set of validations

Testing in rails console was performed to verify that validations worked and that Users, Posts and Comments could be saved to the database. Active record methods were used to test associations between tables e.g., 

    > u2 = User.find(2)
    > c1 = u2.comments.first returned that user’s comment. 
    > c1.user returned that comment’s author User (u2).
    > p1 = Post.first
    > p1.comments.first returned the comment c1.
    > c1.post returned the post p1.
    > User.find(2).destroy removed User 2, their posts and associated post comments, and comments

