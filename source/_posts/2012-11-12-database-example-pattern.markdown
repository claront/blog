---
layout: post
title: "Database Example Pattern"
date: 2012-11-12 21:18
comments: true
categories: database pattern
---

When we tried to wrap up our four Beginning Resources last week we ran into a tiny snag.  Tyler was unable to run ``rake db:migrate`` and migrate the database locally because he didn't have a PostgreSQL database setup.

Which also exposed that we hadn't taken the time to configure a common Rails application setup pattern which is to not store any configuration file that can have passwords, like the ``database.yml`` file, in the repository.  And instead to provide either example or runtime generated versions of those files.

The most common approach for the ``database.yml`` file is to create a ``database.yml.example`` file in the ``RAILS_ROOT/config`` folder and have it setup with the project's [documented setup information](https://raw.github.com/rubycommcollege/campus/master/config/database.yml.example).  So we've impletmented that now and we're moving again in the right direction.  