# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
# Database Structure

1. User

* email
* password

has_many :forum_threads
has_many :forum_post

2. ForumThread

* user_id:integer
* subject:string

belongs_to :user 
has_many :forum_posts

3. ForumPost

* forum_thread_id:integer
* user_id:integer
* body:text

belongs_to :forum_thread
belongs_to :user

