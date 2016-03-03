## Directions to Get An App Built with KNEX onto Heroku

* Git add, commit, and push to github so your little app is all backed up and safely tucked away in your github repo.
* Create site in heroku (`Heroku create`)
* Next, git push to heroku. (`git push heroku master`)
* Then do `heroku addons:create heroku-postgresql`
* Finally, run the migration. (`heroku run knex migrate:latest --env production`)
* And now you can open your app in heroku via `Heroku open`. BOOYAKASHA BOOOIIII!!!!!

## Things to double check if you are getting errors with Heroku

* Check your logs. Check your logs. Check your logs. Do this in terminal via `heroku logs`.
* If your app is working, but your page is not rendering anything from your database, make sure that you have seeded your database in heroku. You can do this in the terminal via `heroku run knex seed:run`.
* In your package.json do you have a line that says `"scripts": {"start": "NODE_ENV=development node ./bin/www"}`? If so, replace 'development' with 'production'. Or, remove the entire `NODE_ENV=development` part.