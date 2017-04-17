---date:        "2017-06-21T11:27:27-04:00"title:       ""description: ""tags:        [ "" ]topics:      [ "continuous-integration" ]---
# Continuous Integration and Continuous Delivery: Walkthroughs
## Overview
From Rhonabwy.com, they list 6 rules for setting up continuous integration systems.
1. Keep all the logic for building your code in scripts in your code repositories/source control.2. Gate merging code on the results of tests, and mercilessly hunt down and resolve unstable tests.3. Speed of your gates will directly impact developer velocity and productivity, keep it lean and be consistent with mocks or dummies in your testing code.4. Make sure all the developers can reproduce what gets run in the CI system by themselves.5. Cascade your builds and tests, driving full integration tests with CI systems.6. Develop, trend, and review benchmarks about your product from your CI systems.
> 2. Gate merging code on the results of tests, and mercilessly hunt down and resolve unstable tests.
Unit tests should mock out any backing service including external APIs.Instead of actually using a backing service like a database or message queue, use mocking frameworks or code interface to keep unit tests concise and quick.Since initial testing should be happening on all code changes (commits, checkins, etc.), these tests should be concise and quick not overloading the test infrastructure -- or even time to get build status.
> 3. Speed of your gates will directly impact developer velocity and productivity, keep it lean and be consistent with mocks or dummies in your testing code.
Keep the continuous integration pipeline as smooth as possible, adding security, approvals, gates accordingly.
> As a general rule, most developers hate to document anything, but relish learning new tricks.
^ just an interesting quote
> 4. Make sure all the developers can reproduce what gets run in the CI system by themselves.
Docker solves this very easily.Having all build and test scripts part of the repo helps as well.
> 5. Cascade your builds and tests, driving full integration tests with CI systems.
## Walkthroughs
We will be looking at a simple Node.js API, https://github.com/bsedg/events-api. In this project, we generated the javascript code from a Swagger yaml file, https://github.com/bsedg/events-api/blob/master/config/swagger.yaml.
### How I created my project
Assuming Node is already installed (see here if not), here were steps after I created the swagger.yaml file.
```bash# Install dependenciesnpm install -g yonpm install -g generator-swaggerize
# Generate code, which will prompt you for a couple inputs.yo swaggerize```
See https://github.com/krakenjs/generator-swaggerize for more details.
### Continuous Integration
1. Travis-CI [travis-ci.org](https://travis-ci.org/) | [post]()2. Codeship [codeship.com](https://codeship.com/) | [post]()3. CircleCI [circleci.com](https://circleci.com/) | [post]()4. Wercker [wercker.com](https://www.wercker.com/) | [post]()5. Shippable [shippable.com](https://www.shippable.com/) | [post]()
