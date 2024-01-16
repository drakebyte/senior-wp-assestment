# Test Project

Test project for senior dev.
Approach:
- be as simple as possible, but also potentially scalable and modular
- so i created inheritance, singletons or abstract classes
- also, i could have go with custom table to log the votes, but went with post meta and cookie to keep it simple, and because from the description it didn't seem relevant for the admin to see which IP voted what
- i implemented only IP now but the same logic can be used to log votes by user ID
- i went with s imple approach to the design too, it is not pixel perdect, i made the emojis as characters only, instead of an icon font or SVG, but these are easy to be implemented as needed.
- the code can be further optimised, but given the time frame, i left it as it is, and only optimised the individual files
- i used webpack and composer for showcase purposes
- the voting is implemented on the SINGLE view
- i used a filter hook to attach the form, but it can be made a custom block if needed, or a shortcode too. not implemented yet as it wasn't a requirement
- i hashed the ip addresses with md5 to protect them and for GDPR reasons
- to prevent javascript hacking, to vote multiple times, the php part of the ajax also makes sure to have only one vote
- the last vote per post is stored in a cookie for the user. if user id based voting will be implemented, these can be also stored in the DB

## Requirements

- [PHP](http://php.net/) >= 7.2
- [WordPress](https://wordpress.org/) >= 5.0
- Composer
- Node.js
- Npm
- Git

## Before activation
- Development only:
  - run `composer install`
  - run `npm install`
  - run `npm run build`
- Go to WP Admin and make sure the plugin is enabled
- open a single post and find the widget below it
- composer and other dev files are not needed for distro package, we include the vendors in the final package

### Documentation

This theme uses a few frameworks and packages. Here are some useful links for you to get up to speed on the most
important ones. I recommend going through them.

- [WordPress PHP Coding Standards](https://make.wordpress.org/core/handbook/best-practices/coding-standards/php/): the
  PHP style and formatting is validated against these standards.
- [Sass Guidelines](https://sass-guidelin.es/): the SCSS syntax and formatting is validated according to these
  guidelines. In general, the entire guide is very useful, but there are some things we handle differently (excluding
  the syntax and formatting).
