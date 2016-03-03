## Directions to Get A App Built with KNEX onto Heroku

* Git add, commit, and push to github so your little app is all backed up and safely tucked away in your github repo.
* Create site in heroku (`Heroku create`)
* Next, git push to heroku. (`git push heroku master`)
* Then do `heroku addons:create heroku-postgresql`
* Finally, run the migration. (`heroku run knex migrate:latest --env production`)
* And now you can open your app in heroku via `Heroku open`. BOOYAKASHA BOOOIIII!