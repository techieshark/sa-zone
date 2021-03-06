# Prerequisites

* This application requires Ruby. If you don't have it, [download and install here](https://www.ruby-lang.org/en/installation/).
* This application requires Rails.
* This application also requires Postgres SQL. If you don't have it, [download and install here](http://postgresapp.com/).

# Installation instructions

#### Clone the app to your machine:

    git clone https://github.com/codeforamerica/sa-zone.git
    cd sa-zone

#### Install the dependencies:

    bundle install

#### Create the database:

    bundle exec rake db:create
    bundle exec rake db:migrate
    bundle exec rake legistar_all:load
    bundle exec rake council_districts:load

*If you want to update or change these specific shapefiles, they exist in the lib/asset folder in the application.*

#### Run your application

    rails server

#### Troubleshooting

Make sure the postgis extension is properly loaded.

    SELECT POSTGIS_VERSION(); # succeeds if PostGIS objects are present.

#### You did it!

Now you can access your application at http://0.0.0.0:3000

# Copyright

Copyright (c) 2014 Code for America. Created by the Techzans team working in San Antonio (Amy Mok, Maya Benari, David Leonard). Released under the BSD license.
