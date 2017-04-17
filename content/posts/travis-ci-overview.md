---date:        "2013-04-13T11:27:27-04:00"title:       ""tags:        [ "" ]topics:      [ "" ]---
# Travis CI
## Overview
Travis CI is a hosted build platform that allows for quick, simple build pipelines setup for a github project. With a public open source project, using this service is free. If you have private repositories, there are paid plans.
In order to get started, you create an account at https://travis-ci.org. Once you create your account, you can setup your first project using Travis CI. Follow along with their up to date getting started page, https://travis-ci.org/getting_started.
1. Go to your travis-ci profile page, https://travis-ci.org/profile/<username>.2. Add a `.travis.yml` file to the root of your repository. For the purposes of the example, we can use the Node.js build documentation at https://docs.travis-ci.com/user/languages/javascript-with-nodejs/.3. Push some code to your repository to test out your build.
## Example Walkthrough
## Do It Yourself
First, setup your git repository.
1. Create repository in github - Check the option for `Initialize this repository with a README` - Add `.gitignore` for Node2. Follow the instructions to clone your project locally.
Then, setup your local development and initialize the project.
1. Go to http://editor.swagger.io and create your own API spec or use one of their's predefined for you (File -> Open Example...). Download the yaml file via File -> Download YAML.2. In your project folder you created for the git repository, move the `swagger.yaml` file you downloaded to that folder.3. Run `yo swaggerize` and answer the prompted inputs. - I used Express for the web framework4. Build and run your code to test to make sure it works...
```bash# will install dependencies to the ./node_modules foldernpm install
# will start the server locally to listen on a port 8000?npm start
# send request to an endpoint you defined# if you have a version, be sure to add that to the path:#  i.e. /v1/<endpoint>curl -i http://127.0.0.1:8000/<endpoint>```
## Conclusion
Travis CI is just one of many continuous integration platforms to use, but is trusted by many great organizations.
## Other links
https://github.com/dwyl/learn-travis
