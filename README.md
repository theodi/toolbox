This repository powers the [ODI Toolbox Website](http://toolbox.theodi.org/). This README describes how to contribute to the toolbox.

## Tell Me About The ODI Toolbox

The [ODI Toolbox](http://toolbox.theodi.org/) is intended for organisations working with open data. It’s a suite of open source software that enables publication, assessment of - and collaboration on - open data.
 
The toolbox was developed by the ODI Labs Team. ODI Labs follows the GDS Services Agile development framework. ODI Labs matured(sic) Open Data Pathway and Open Data Certificates to Live status. Both services function as open data Assessment Tools. Several of the other tools developed during the first quarter of 2016 are currently in the beta stage. These data publication prototypes  are intended to help organisations understand what their data is, what they can do with their data and what their users might want. Each app meets a different need. 

* Open Data Assessment Services
    * [Open Data Certificates](https://certificates.theodi.org/): a tool to assess the quality of open data releases, and award a “kite mark”-like certificate.
    * [Open Data Pathway](http://pathway.theodi.org/): a tool to help organisations assess their readiness for open data publishing, and help them identify where they need to focus their improvement efforts.
* Open Data Publication Tools
    * [CSVlint](https://csvlint.io/): a validation tool for CSV files, supporting both Frictionless Data and CSV on the Web standards.
    * [Octopub](https://octopub.io/): a simple publishing tool for open data, allowing publishers to release data without having complex infrastructure set up.
    * [Bothan](https://bothan.io/): a metrics tracking and dashboarding tool designed for open publication of metrics data.
    * [Comma Chameleon](http://comma-chameleon.io/): a desktop editor for CSV files, targeted at creating quality open data that is ready for reuse.

(To find out more detail about each of the tools, check them out on the [Toolbox Website](http://toolbox.theodi.org/))

The tools of the ODI Toolbox are built to interoperate with other services - including other tools in the suite! Take CSVlint for example. The [CSVlint service](http://csvlint.io/) is a Rails application that provides an online continuous validation service. Octopub integrates this service into published datasets that feature CSV files. The CSVLint service is powered by the [Ruby gem](https://github.com/theodi/csvlint) of the same name, which can be used locally as a command line tool or within any ruby application. The CSVlint gem CSVlint also features in Comma Chameleon - which supports CSV validation within the app - via TravellingRuby.
 
Hopefully this brief example gives a sense of what we’re trying to build with the ODI toolbox - as OSS ecosystem around data collaboration, publication and assessment
 
(to learn more about ODI’s vision for OSS data tools, check out the [Public Roadmap](https://trello.com/b/2xc7Q0kd/labs-public-toolbox-roadmap) (see below for details), or follow our blog)

## Why We Welcome Contributions

The Open Data Institute is committed to building a strong, fair, and sustainable data economy. We believe that entails involving everybody in the publication and consumption of open data. That’s why we have such a strong focus on data publication in our existing tools - we want **everybody** to be involved in publishing data.
 
The Toolbox grew out of ODI Labs engagement with the open data software ecosystem. Noticing gaps in the types of data tools available Labs developed MVP experimental products intended to plug those gaps. We hope these provocations get everyone thinking. We’d like for the community working in open data software to either fill the identified gaps in other ways, use our work to continue filling those gaps (even locate as yet unidentified gaps!) or contribute to our tools to improve their utility. 
 
We look to OSS success stories like Ruby, Github and Adapt and we want to build an ecosystem of OSS tools that support Open Data - like OKFN’s JKAN. We know we can’t do this all by ourselves, nor would we see this as the best way forward - we aspire to build with developments in the ecosystem. We want to build an OSS community around the Toolbox and hope you can be part of it!
 
We’re focusing on opening the ODI Toolbox to open source contributions to enable users to adapt the tools to their needs by contributing to our code base. We value growing an engaged community to collectively and collaboratively chart a route through our codebase. That way we can identify urgent bug fixes can be applied quickly.


## How to Contribute to the ODI Toolbox

### File an Issue for Resolution

If you encounter a problem or have a recommendation for our tools please file an issue in the relevant toolbox repository
 
**Many eyes make all bugs shallow.** 
We can’t keep track of all the snags that arise across the Toolbox, so if you notice something please let us know.
 
**Suggest a minor enhancement:** 
We’re not just interested in catching bugs - if you notice something that could be improved about the Tool - whether it’s an interface enhancement or an optimisation suggestion we’re interested to hear from you

### Provide Feedback on the Public Roadmap

The Public Roadmap board lists cards for new features or improvements to these tools, and is intended as an overview of upcoming developments for each tool in the Toolbox.
The Roadmap tracks future directions for each of the toolbox. You can consider it as the feature backlog for the entire toolbox and per toolbox application. 
You can also vote and comment on cards to express which ones are most important to you

### Contribute code to our Toolbox

see the next sections for full details

## Contributing Code

If you’re a developer interested in Open Data familiar with any of the following technologies we’d like to interest you in collaborating on our Toolbox
 
* Ruby
* Ruby on Rails
* Node.js
* HTML, CSS and Javascript Frameworks

By participating in this project, you agree to abide by our [Code of Conduct](https://github.com/theodi/bothan/blob/master/.github/CODE_OF_CONDUCT.md).

If this is your first time contributing to the ODI’s codebase you will need to [create a fork of this repository](https://help.github.com/articles/fork-a-repo/).

Each tool's README contains instructions to get your Development environment running locally. There will be additional instructions on running the test suite for each repo. Consult these prior to making any contribution.

### Code Review Process 

All contributions to the codebase - whether fork or pull request - will be reviewed per the below criteria.
To increase your chances of your push being accepted please be aware of the following
- Write [well formed commit messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
- Follow our style guide recommendations
- Write tests for all changes (additions or refactors of existing code). 
- Of the github integrations we use two will be utilised to check appraise your contribution. In order of priority these are
    - Travis ensures that all tests (existing and additions) pass
    - Travis/Coveralls ensures that overall test coverage for lines of code meets a certain threshold. If this metric dips below what it previously was for the repository you’re pushing to then your PR will be rejected
    - Gemnasium ensures dependencies are up to date
- Once your PR is published and passes the above checks a repository administrator will review your contribution. Where appropriate comments may be provided and amendments suggested before your PR is merged into Master.
- Once your PR is accepted you will be granted push access to the repository you have contributed to! Congratulations on joining our community, you’ll no longer need to work from forks.

#### Push Access
If you make a contribution to another repository in the Toolbox you will be expected to repeat this process. This is necessary as there is variance across our toolboxes - from different web frameworks (e.g. Bothan [Sinatra] vs CSVlint, Octopub, Pathway and Certificates [Rails]) to different underlying code (Comma Chameleon built on Javascript via the Electron runtime)

### Code Style Guide

We follow the same code style conventions as detailed in Github’s [Ruby Style Guide](https://github.com/github/rubocop-github/blob/master/STYLEGUIDE.md)

### Getting Started

#### Development Tools
 
[Git](https://help.github.com/articles/set-up-git/): Git is a version control system prerequisite to distributed software development
[Github Client](https://help.github.com/desktop/guides/getting-started/): The Github client is a GUI that facilitates some of the operations required for git VCS. It is not as powerful as some of the other options (Gittower, other paid options) but it is free
 
Feel free to use whatever text editor or IDE you prefer for coding. If you’re using Atom then we’ve found the following packages helpful for working on the toolbox
* Cucumber
* Jekyll
* Pretty JSON
* RubySyntaxReplacer

#### Setting up your dev environment

* Windows
* Linux
    * At the ODI we do not use these platforms for development. If you use either OS for OSS development with the languages and libraries that we do please consider contributing some documentation to this README 
* Mac
    * All subsequent instructions in this guide are intended for Mac OSX platforms. We’ve included the instructions relevant for the most recent release of OSX

##### Ruby Development Tools
 
We use rbenv as several repos in our Toolbox employ varying versions of ruby and ruby on rails. Rbenv is a ruby version management tool like rvm - and you may use rvm if you prefer. If you would like to utilise Rbenv please follow the following steps.

* [Install Homebrew](https://coolestguidesontheplanet.com/installing-homebrew-on-macos-sierra-package-manager-for-unix-apps/) - Rbenv can be installed using the Homebrew package manager.
* After installing Homebrew it’s advisable to run `brew doctor` to check if any issues occurred during install
* [Install Rbenv](https://github.com/rbenv/rbenv#homebrew-on-mac-os-x)
* Then install [ruby-build](https://github.com/rbenv/ruby-build#installing-with-homebrew-for-os-x-users)
    * (if you encounter errors with the above try: 
      `git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build`
      `brew install ruby-build`
      )
* Almost there - to complete the set up run the following
    * `echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.profile`
    * `echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.profile
       rbenv rehash`
       
To test that rbenv is working correctly on Mac OS run the following  
`rbenv install 2.1.8*`  
`* or the ruby version stipulated in the repository you wish to work on`
`rbenv rehash`
`ruby -v`

You should now see a different ruby version to the base install on your system (ruby 2.4.0 in the case of MacOS)

Finally install bundle
`Gem install bundle`

##### Rails Development Tools
 
Ruby on Rails additionally requires you install and run Redis (Postgres) and MySQL servers. If you already have these on your development machine you can skip their respective install steps in this [following guide](https://gorails.com/setup/osx/10.12-sierra)