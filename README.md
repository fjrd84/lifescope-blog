# lifescope-blog

This is the blog of the [lifescope project](https://www.lifescope-project.com).

## Dependencies installation

If you're running Mac OSX 10.11.06 El Capitan or higher, these are the commands
you'll need to get the blog up and running.

If you are using Linux or Windows, the commands will be pretty similar (just ignore the part with `-n /usr/local/bin`).

First of all, [install Ruby on your system](https://www.ruby-lang.org/en/documentation/installation/).

Then, run the following commands on the console.

```bash
 sudo gem update --system
 bundle install # Install the required gems
 bundle exec jekyll serve
```

If everything went fine, you'll see something like this on the console:

```bash
> lifescope-blog bundle exec jekyll serve
Configuration file: /Users/jdonado/Git/lifescope-blog/_config.yml
            Source: /Users/jdonado/Git/lifescope-blog
       Destination: /Users/jdonado/Git/lifescope-blog/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
                    done in 0.373 seconds.
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```

Just open the server address to preview the contents.

## Build a new version

Just compile the blog to `/docs`:

`bundle exec jekyll build --destination docs`
