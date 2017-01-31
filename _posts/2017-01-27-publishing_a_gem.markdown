---
layout: post
title:  "Publishing a Gem"
date:   2017-01-27 21:04:00 +0000
---


Congratulations on the creation of your brand new ruby gem. It deserves a pat on the back, don’t be bashful. However, before we kick our feet up and crack open an adult beverage, there’s still *one* more item on the good o'l to-do-list. Now that you’ve created this incredible gift to developers, how do we share it with the world? [RubyGems.org](https://rubygems.org/) of course!

## Getting Started
I'm going to make the assumption your gem's already been created at this point. *If* the the answer is "not yet", [Smashing Magazine](https://www.smashingmagazine.com/2014/04/how-to-build-a-ruby-gem-with-bundler-test-driven-development-travis-ci-and-coveralls-oh-my/) has an informative article which will take you through the process.
* Note: We'll name our project `foobar` for demonstration purposes. Needless to say, you'll want to instead name it after your own project because the `foobar gem` may already be in use (confirmed it has indeed been taken).

### Step 1: Create an account
Visit (https://rubygems.org/sign_up) and enter an email address to be associated with your new account, a "Handle" (aka username), and a password. After a quick email confirmation, your new account will be good to go!

### Step 2: Setup an API key
Once your RubyGems.org account has been activated, you'll need to connect it to your local machine (computer) by downloading & storing a personal API key. Add the line below followed by your password.

* Note: Remember to replace `john_doe` with your own username.

`$ curl -u john_doe https://rubygems.org/api/v1/api_key.yaml > ~/.gem/credentials`

`Enter host password for user ‘john_doe’:`

### Step 3 (may not apply): Remove restrictions
If your gem was originally created via Bundler, open up the `foobar.gemspec` file which should be located at the root level of your project. Look for the following lines:

```ruby
# Prevent pushing this gem to RubyGems.org. To allow pushes either set the 'allowed_push_host'
# to allow pushing to a single host or delete this section to allow pushing to any host.
if spec.respond_to?(:metadata)
  spec.metadata['allowed_push_host'] = "TODO: Set to 'http://mygemserver.com'"
else
  raise "RubyGems 2.0 or newer is required to protect against public gem pushes."
end
```

Either remove or comment out the lines above (if they exist) to prevent the [following error](http://codespeakeasy.com/2016/06/28/bad_uri_is_not_uri_todo_set_to_http_mygemserver_com/) while pushing onto RubyGems.org:

```bash
$ gem push foobar-0.1.0.gem
Pushing gem to https://rubygems.org...
ERROR:  While executing gem ... (URI::InvalidURIError)
    bad URI(is not URI?): TODO: Set to 'http://mygemserver.com'
```

Once these lines have been removed from the `gemspec` file , don't forget to commit your changes via `git`.

`$ git commit -am 'Remove default from gemspec file to allow pushing to rubygems.org'`


### Step 4: Package
Use your gemspec file to package the gem for production:

```bash
$ gem build foobar.gemspec
  Successfully built RubyGem
  Name: foobar
  Version: 0.1.0
  File: foobar-0.1.0.gem
```

### Step 5: Publish
Publish your gem by pushing it to RubyGems.org:
```bash
$ gem push foobar-0.1.0.gem
Pushing gem to https://rubygems.org...
Successfully registered gem: foobar (0.1.0)
```

### Step 6: Enjoy
Visit your shiny new gem at `https://rubygems.org/gems/foobar` and enjoy :)

## Helpful Resources
http://guides.rubygems.org/make-your-own-gem/
http://guides.rubygems.org/publishing/
http://www.alexedwards.net/blog/how-to-make-a-rubygem-part-three
https://www.digitalocean.com/community/tutorials/how-to-package-and-distribute-ruby-applications-as-a-gem-using-rubygems

