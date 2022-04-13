The Dominion Shirt

## Todo

flip button below shirt, can hover to zoom in
store icon

## Deploy

### Heroku

Create a new project:

Create a new App
`heroku create`

Log in to container registry
`heroku container:login`

Build and upload the image
`docker build -t registry.heroku.com/<app_id>/web -f ./deploy/docker/Dockerfile.prod .`

Push the image
`docker push registry.heroku.com/<app_id>/web`

Release the image
`heroku container:release --app <app_id> web`

fast-sands-60878
`docker build -t registry.heroku.com/fast-sands-60878/web -f ./deploy/docker/Dockerfile.prod .`
`docker push registry.heroku.com/fast-sands-60878/web`
`heroku container:release --app fast-sands-60878 web`

### Github

Bundle project
`cd ui && npm run build`

Copy the contents of /ui/dist to the root of the project

Push changes to github

Configure github pages in the repository's settings page

## Troubleshooting

### Favicon not updating

The favicon is automatically set as the default VUE favicon, and needs to be replaced manually everytime you run `npm run build`. After compiling, edit index.html with the link to your PNG file (or similar).

https://stackoverflow.com/questions/53216047/change-favicon-vuejs
