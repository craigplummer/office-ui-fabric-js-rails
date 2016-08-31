# office-ui-fabric-core-rails

[![Gem Version](https://badge.fury.io/rb/office-ui-fabric-js-rails.svg)](https://badge.fury.io/rb/office-ui-fabric-js-rails)

office-ui-fabric-rails integrates the [Office UI Fabric JS](https://github.com/OfficeDev/office-ui-fabric-js) framework from Microsoft into the Rails Asset Pipeline

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'office-ui-fabric-js-rails'
```

And then execute:

    bundle

## Usage

### Add Office UI Fabric to your CSS

#### CSS

Add the following line to the end of your `app/assets/stylesheets/application.css` file:

```
*= require fabric
```

If you also wish to use the [Fabric components](http://dev.office.com/fabric/components) then you should also add

```
*= require fabric.components
```

#### Sass

If you are using Sass then you can add the following to your application.scss instead:

```
@import "Fabric";
```

If you also wish to use the [Fabric components](http://dev.office.com/fabric/components) then you should also add

```
@import "Fabric.Components";
```

Or you can just import the components you wish to use from the components directory. The names match those listed on the [fabric site](http://dev.office.com/fabric/components). E.g to include the Breadcrumb component add

```
@import "components/Breadcrumb"
```

### Add Office UI Fabric to your JS

Add the following to your `app/assets/javascripts/application.js` file:

```
//= require fabric
//= require fabric.templates
```

For information on how to use the Office UI Fabric framework see the [documentation](http://dev.office.com/fabric)

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/craigplummer/office-ui-fabric-js-rails.

For issues with Office UI Fabric itself please use https://github.com/OfficeDev/Office-UI-Fabric

## License

The [Office UI Fabric](https://github.com/OfficeDev/Office-UI-Fabric) framework and the rest of the office-ui-fabric-js-rails project are licenced under the [MIT License](https://opensource.org/licenses/mit-license.html)
