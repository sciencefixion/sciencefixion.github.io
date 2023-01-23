---
layout: post
title: GlitchCraft
categories: portfolio
image: /assets/img/glitchcraft.png
github: glitch_craft
permalink: /portfolio/glitchcraft/
front: true
---

## GlitchCraft

GlitchCraft is a Ruby on Rails application allowing users to glitch images. Users can search for a keyword which then returns an image from two APIs via the GlitchService Microservice. One of these images is then chosen to be glitched.

The first image returned is generated from scratch by DeepAI, and the second is returned based on human image tags from Pixabay. This gives users the unique option to glitch an image that is either what an AI thinks the search term represents or what humans tag an image as.

Despite the limitations of Ruby as it relates to visual media, the GlitchCraft team has been able to glitch images using only that language. We employ Google OAuth to authenticate users and images are stored with a mixture of Amazon Web Services’ S3 and Ruby on Rails’ ActiveStorage.

*Note: GlitchCraft is currently being updated and although it can be cloned and run successfully on a local machine, the production version is down temporarily.<br><br>**My areas of focus**:<br>The original concept was mine as was the implementation and combining of gems that would transform and store image files in a Postgres database retrieved by consuming two third party APIs and combining the data by exposing our own API via the GlitchService microservice. I also worked on a good deal of the styling.

## Relevant links

[GlitchCraft GitHub Repo](https://github.com/sciencefixion/glitch_craft)

[GlitchService Microservice GitHub](https://github.com/Kathybui732/glitch-service)

## Versions

Ruby 2.5.3
Rails 5.2.4.4

## Configuration

1. Run `git clone git@github.com:sciencefixion/glitch_craft.git`
2. `cd glitch_craft`
3. `bundle install`
4. `rake db:{create,migrate}`
5. `bundle exec figaro install`
6. Add your google client secret and ID to the application.yml file
7. `rails s`

## Test Suite

Run `bundle exec rspec`

## Microservices

This app depends on the [GlitchService microservice](https://damp-forest-93176.herokuapp.com/). GlitchService works in hand with GlitchCraft to consolidate two images that users can choose from to glitch.

## Contributors

[Dan Sehl's GitHub](https://github.com/dtsehl) &
[Linkedin](https://www.linkedin.com/in/danielsehl)

[Jane Greene's Github](https://github.com/janegreene) &
[Linkedin](https://www.linkedin.com/in/jane-greene-mba/)

[Kathy Bui's Github](https://github.com/Kathybui732) &
[Linkedin](https://www.linkedin.com/in/kathy-bui-87a27a1ab/)

[Rion's GitHub](https://github.com/sciencefixion) &
[Linkedin](https://www.linkedin.com/in/rion-h-7b3668b2/)

## Our App

### Schema

<p align="center">
 <img src="https://i.imgur.com/31bogeL.png">
</p>

### Welcome page

<p align="center">
 <img src="https://i.imgur.com/Bz6sJzN.png">
</p>

### User Dashboard

<p align="center">
 <img src="https://i.imgur.com/2aoh8Qu.jpg">
</p>

### Image Search Results

<p align="center">
 <img src="https://i.imgur.com/8UEzivt.jpg">
</p>

### Glitch an image

<p align="center">
 <img src="https://i.imgur.com/CjExz6m.jpg">
</p>

### FAQ

<p align="center">
 <img src="https://i.imgur.com/CcKkvEM.png">
</p>

### About Us

<p align="center">
 <img src="https://i.imgur.com/NKv7AwP.jpg">
</p>

## Wishlist

- We wanted a user’s personal gallery
- A community gallery of all user’s glitches
- A way to favorite someone else’s glitches to show up on user’s dashboard
- A way to up vote glitches user’s liked that could show up in a spotlight gallery
- More glitching functions: different glitches, maybe have a button to randomly select a glitch, and another button to select a certain glitch
- A way to let users upload their own images

## Known Issues

- Our production site isn't configured to use S3 yet, so it is not up and running
- Our app is not optimized for safari; images may not render
