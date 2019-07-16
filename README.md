# Magento 1.9.X Local Docker Environment

A robust environment for local Magento 1.X development with docker. Easily bring up, tear down, and test your Magento 1.X application without fear of impacting your business workflow.

## Purpose
The Magedocker environment is intended to be a local environment for Magento 1.X that simulates the most common LAMP + Redis stack that is used for Magento 1.X.

## Minimum Requirements
* Docker
    * Windows
    * Mac
    * Linux

## Features
* PHP 5.6 & PHP 7.2

## Use Cases (User Stories)
We intend to support the following common use cases:
* [Working with an existing Magento 1.X Project](./docs/stories/existing-project.md)
* [Complete Teardown and Reinstall](./docs/stories/teardown-and-setup.md)
* [Working with MySQL](./docs/stories/working-with-mysql.md)
* [Switching between PHP 5.6 and PHP 7.2](./docs/stories/php-switching.md)

## Frequently Asked Questions
To avoid unnecessary Issues, there is documentation on commonly asked questions:
* [Common FAQs](./docs/faqs/faq.md)
* [What commands do I need to know and where are they run?](./docs/faqs/commands.md)