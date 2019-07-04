# Devcamp Portfolio App

> This is a Ruby on Rails 5 application that allows users to create their own portfolios.

## Features

- Real time chat engine for comments
- Blog
- Portfolio
- Drag and drop interface

## Development Concepts

### Generators

#### Model

It is the way to connect the app to the database and persist its data.

``` rails g model feature_name attribute_name:attribute_type ```

Creates:

- Model
- Migration (ruby class to manipulate the database; in this case to create a database table for the model)


#### Controller

It does not talk to the database. Useful to create hardcoded pages.

``` rails g controller path_name_in_plural page_name ```

Creates:

- Controller
- Route
- View

#### Resource

Very skinny scaffolds. Most commom to use beucase it does not give bloated code.

``` rails g resource feature_name attribute_name:attribute_type ```

Creates:

- Model
- Migration
- Route
- Controller
- View (directory only)

#### Migration

It is used to add, change or take away attributes from a database table.

``` rails g migration description attribute_name:attribute_type```

Rails convention to define a description: operation_attribute_table
Eg: add_title_to_blogs

Creates:

- Migration

#### Scaffold

It generates a completed CRUD functionality for a given feature.
*Be careful*: It gives a lot of things may not be useful and cause potential issues later on.

``` rails g scaffold feature_name attribute_name:attribute_type ```

Creates:

- Model
- Migration
- Route
- Controller
- Views

### Permalinks

Non-changeable address for the page. Used by search engines to look for the page.

#### FriendlyId

Permalink plugin for ActiveRecord. It gives a specific slug for a resource id.

How-to: https://github.com/norman/friendly_id