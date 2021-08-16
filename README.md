## `heroku-buildpack-storybook`

This buildpack builds storybook using `npm` and is meant to be used before `https://github.com/heroku/heroku-buildpack-static.git`.

If you are using an `app.json`, it might look something like this:

```JSON
{
  "name": "your-app-name",
  "description": "",
  "scripts": {},
  "env": {},
  "formation": {
    "web": {
      "quantity": 1,
      "size": "free"
    }
  },
  "addons": [],
  "buildpacks": [
    {
      "url": "heroku/nodejs"
    },
    {
      "url": "https://github.com/Root-App/heroku-buildpack-storybook.git"
    },
    {
      "url": "https://github.com/heroku/heroku-buildpack-static.git"
    }
  ]
}

```
