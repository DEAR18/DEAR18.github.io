# GitHub Page site

https://dear18.github.io/

# Testing GitHub Pages site locally

Use Docker to get test environment.
This repository uses Jekyll to generate static website.

## Environment
```
docker pull jekyll/jekyll
docker container run -p 4000:4000 -v host-path:path-inside-container -it your-docker-image-for-test bash
```
**Note:** Map the container's port (default is 4000 for Jekyll) to the port on your host machine

## Generate web page
In the container:
```
cd github-page-repository-path
bundle install
bundle exec jekyll serve --host 0.0.0.0
```
Now the server should be running, open http://localhost:4000 in your web browser.
