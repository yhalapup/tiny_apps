# Blog
Rails 4.2, Sqlite3

## Installation

```ruby
gem install rails -v 4.2.10
```

This will create a Rails application called Blog in a blog directory and .
```ruby
rails new blog
```
install the gem dependencies that are already mentioned in Gemfile using
```ruby
bundle install
```
```ruby
rails new -h
```
will show you all command line options that Rails application builder accepts

```bash
cd blog
```

start a web server on your development machine
```ruby
bin/rails server
```

```ruby
bin/rails generate controller welcome index
```

```ruby
bin/rails generate controller articles
```
```ruby
bin/rails generate model Article title:string text:text
```
```ruby
bin/rake db:migrate
```
(for production environment you must explicitly pass the environment
```
bin/rake db:migrate RAILS_ENV=production
```
A frequent practice is to place the standard CRUD actions in each
controller in the following order: index, show, new, edit, create, update
and destroy. You may use any order you choose, but keep in mind that these
are public methods; as mentioned earlier in this guide, they must be placed
before any private or protected method in the controller in order to work.

```ruby
bin/rails generate model Comment commenter:string body:text article:references
```
```ruby
bin/rake db:migrate
```
```ruby
bin/rails generate controller Comments
```
