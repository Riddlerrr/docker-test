# Fresh Rails 6.0 app with configured Docker

Docker uses Ruby 2.6.6, PostgeSQL 12.2, Redis 5.0, NodeJS 12, yarn 1.22.4 and bundler 2.1.4
Also [dip](https://github.com/bibendi/dip) configuration was added to improve user experience.

## How to install

You must have docker installed and runned on your system. For mac is Docker Desktop app.

Install dip to your system:

```
brew tap bibendi/dip
brew install dip
```

Run `dip provision`. It will download all necessary images, build containers, install gems and npm modules and prepare a database.
That's it 🎉, you ready to run rails server: `dip rails s` to see your app runned on [http://localhost:3000](http://localhost:3000).

To run rails/rake tasks you have 2 options:

1. Run `dip sh`. It opens container terminal where you can run `rake db:migrate` or any other commands.
2. Run `dip rake db:migrate`. It executes the command and exit like if you run `rake db:migrate` without containers.



