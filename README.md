# WP Essentials Heroku

A composer [metapackage](https://getcomposer.org/doc/04-schema.md#type) of essential
plugins & libraries for WordPress projects served in Heroku environment.

With metapackage it is possible to install and update multiple packages without
adding individual packages to the project's composer file.

## Installation

`$ composer require frc/wp-essentials-heroku`

## Included packages

- `frc/wp-env-heroku-cleardb`
- `frc/wp-env-heroku-jawsdb`
- `frc/wp-env-heroku-jawsdb-maria`
- `frc/wp-env-heroku-redis`
- `frc/wp-env-heroku-sendgrid`
- `frc/wp-env-heroku-amazon-aws`
- `deliciousbrains/wp-amazon-s3-and-cloudfront`
- `frc/sendgrid-email-delivery-simplified`
- `wpackagist-plugin/redis-cache`
- `frc/wp-amazon-c3-cloudfront-clear-cache`
- `frc/wp-gforms-s3-upload`
- `frc/wp-gravityforms-cloud-export`
- `frc/wp-transients-api`
- `frc/wp-multilingual-options-page`

## Cloudfront

Each site that uses Cloudfront needs the following variables:

```
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
C3_DISTRIBUTION_ID
```

In most cases the `AWS_...` variables are already set in Heroku's environment variables. If setting `C3_DISTRIBUTION_ID` doesn't work, try adding it to the plugin directly after it's activated, via Settings > Cloudfront settings.