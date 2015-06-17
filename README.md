# in-sane-ember-mobile-chrome-apps

# in_sane_ember-mobile-chrome-apps

###### Disclaimer #####
## This REPO was started as a copy of the very fine SANE project ( See => SANE STACK below )
#######################

I decided to copy (vs fork) the repo because I wanted an opportunity to express my own opinions on several fronts at once. Doing this from the context of a fork can be painful for all involved.

What 'opinions' do I have?

1) Rails is a mature environment that will RULE for many years if for no other reason than MANY full stack developers know it
2) Unless a web app implemented using client-side MVC LOOKS BETTER than one using Server-Side rendering, why bother?
3) Unless I get native apps by using client-side MVC, why bother?
4) The SAME forces that drove developers away from JAVA (faster response to user needs+++) drawing projects away from JAVA web development will drive them back to recover speed and scaling 'lost in translation' to newer platforms.

So... What comes of these RANTS?

I scanned the the marketplace (with the help of some friends) and came up with a DREAM STACK. The one compromise in this based on a measure of MINIMUM COST TO REALIZE.

Companies to the rescue:

DOCKER: https://www.docker.com/
    Uses VirtualBox and Linux kernal containers to 'Build, Ship and Run Any App, Anywhere'. Even better with:

DOCKER_COMPOSE: https://docs.docker.com/compose/
    Multi-container orchestration for docker.

VERT.X - http://vert-x3.github.io/
    A tool-kit for building reactive applications on the JVM.

SANE STACK: - http://sanestack.com/
    A Javascript Fullstack and CLI that lets you rapidly create production-ready web apps using Sails and Ember. The server component is based on Node.

FAMO.US: - http://famous.org/
    High-performance javascript library for animations & interfaces

The community to the rescue:

NODEYN: https://github.com/nodyn/nodyn
    Executes Node on VERT.X

JUBILEE: https://github.com/isaiah/jubilee
    Vert.x runs Rack Apps (like Rails (http://rubyonrails.org/) and Sinatra (http://www.sinatrarb.com/) )
Stretch DREAMS: Given a bigger budget and/or a partner:

PISTON: http://pistoncloud.com
  Piston's IAAS software allows the cows to be treated as COWS vs PUPPIES... (http://pistoncloud.com/2013/04/announcing-enterprise-openstack-version-2/)

BroadCloud: http://www.broadcloud.com
  Would be my first choice.

Almost on the list:

CloudFoundry: http://cloudfoundry.org/index.html
    Definitely cool... but pretty costly in terms BOTH of complexity and hardware the last time I dug into it....
    ( see http://thenewstack.io/docker-on-diego-cloud-foundrys-new-elastic-runtime/ for more )

####################################################
VVV Originally Copied From SANE STACK README.md VVV
####################################################

<p align="center">
  <img src="https://camo.githubusercontent.com/b8ecf54b15f51c7c992d6fce003b661c96d8acec/68747470733a2f2f63646e2e7261776769742e636f6d2f6172746966696369616c696f2f73616e652f67682d70616765732f5f696e636c756465732f73616e652d6c6f676f2e737667" width="400"/>
</p>
## SANE Stack [![Bountysource][bounty-badge]][bounty-badge-url] [![Gitter][gitter-badge]][gitter-badge-url]

[![Build Status][travis-badge]][travis-badge-url] [![Build status][appveyor-badge]][appveyor-badge-url]  [![Dependency Status][david-badge]][david-badge-url] [![npm][npm-badge]][npm-badge-url]

**NOTE: This project, while exciting, is still an early prototype. While being mostly stable it is still being iterated with feature changes and improvements fairly regularly.**

Sane - A Javascript fullstack and cli that uses two of the best frameworks, [Sails](http://sailsjs.org/) and [Ember](http://emberjs.com/), so you can rapidly create production-ready web applications. It takes away all the hassle setting up the full backend and frontend environment, embracing convention-over-configuration all the way, so you can focus just on shipping your app. Additionally this cli also supports Docker, using [Docker Compose](https://docs.docker.com/compose/), to automatically install dependencies such as your database and will make deployment easier.

Quickstart:
* `npm install -g sails sane-cli`
* `sane new project` creates a local project with [sails-disk](https://github.com/balderdashy/sails-disk). To install with [Docker](https://www.docker.com/) and production databases see [Options](http://sanestack.com/#sane-stack-options).
* `sane generate resource user name:string age:number` to generate a new API on the backend and models on the frontend
* `sane up` to start the sails server on `localhost:1337` as well as the ember dev server on `localhost:4200`.
* To work on your frontend-app you work as you would normally do with ember-cli on `localhost:4200`.
* You are now good to go.

**Note: If you use Docker, make sure you have [Docker Compose](http://docs.docker.com/compose/) installed. On Mac or Windows also [boot2docker](http://boot2docker.io/) and for Linux see: [https://docs.docker.com/installation/ubuntulinux/](https://docs.docker.com/installation/ubuntulinux/)**

##Documentation

The full documentation is available at: http://sanestack.com/

##Development

sane-cli is developed with ES6/7 functionality, using [traceur](https://github.com/google/traceur-compiler) to provide a cleaner code as well as a nice experience for us the developers.
To get started:
* `git clone https://github.com/artificialio/sane.git`
* `cd sane && npm install` to install the dependencies
* `npm link` to make sure you can test the master version globally
* If you add a new feature an according test would be appreciated
* `npm test` to run the test-suite

##Thanks
Thanks to [mphasize](https://github.com/mphasize) for creating [sails-generate-ember-blueprints](https://github.com/mphasize/sails-generate-ember-blueprints) which overwrites the default SailsJS JSON response to the one that Ember Data's `RESTAdapter` and `RESTSerializer` expects.
Thanks to [sails](https://github.com/balderdashy/sails) for that great backend framework
Thanks to [ember-cli](https://github.com/stefanpenner/ember-cli) contributors for all the great effort that has gone into this product and from which I have taken a lot of inspiration and code, especially in regards to testing.

##License
SANE Stack is [MIT Licensed](https://github.com/artificialio/sails-ember-starter-kit/blob/master/LICENSE.md).

## Built by

[gitter-badge]: https://badges.gitter.im/Join+Chat.svg
[gitter-badge-url]: https://gitter.im/artificialio/sane?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge
[travis-badge]: https://travis-ci.org/artificialio/sane.svg?branch=master
[travis-badge-url]: https://travis-ci.org/artificialio/sane
[david-badge]: https://img.shields.io/david/artificialio/sane.svg?style=flat
[david-badge-url]: https://david-dm.org/artificialio/sane
[appveyor-badge]: https://ci.appveyor.com/api/projects/status/oku88ae3kxddbw14/branch/master?svg=true
[appveyor-badge-url]: https://ci.appveyor.com/project/Globegitter/sane/branch/master
[npm-badge]: https://img.shields.io/npm/v/sane-cli.svg
[npm-badge-url]: https://www.npmjs.com/package/sane-cli
[bounty-badge]: https://www.bountysource.com/badge/team?team_id=58969&amp;style=bounties_received
[bounty-badge-url]: https://www.bountysource.com/teams/sane-stack?utm_source=Sane%20Stack&utm_medium=shield&utm_campaign=raised
[code-climate-badge]: https://codeclimate.com/github/artificialio/sane/badges/gpa.svg
[code-climate-badge-url]: https://codeclimate.com/github/artificialio/sane

Built with love by [Artificial Labs](http://artificial.io/) and [contributors](https://github.com/artificialio/sane/graphs/contributors) <3

Revision history:

6/17/2015 1:50 PM EST -

Copied from:
  Repo: https://github.com/ember-cli/ember-cli
  branch: master
  commit: 9c13432d0668980940df69fc587e1c9904f4cdef
  comment: Merge pull request #4300 from rwjblue/update-ember-release

6/17/2015 1:57 PM EST -

Copied from:
    Repo: https://github.com/artificialio/sane
    branch: master
    commit: f7ec792c7ec7e5c979c1f2707044bb6e46dd4cce
    comment: Merge pull request #156 from IanVS/fix_no-global-ember