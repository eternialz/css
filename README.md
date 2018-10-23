# FRAMEWORK PROJECT

## css notes

- One theme file for a project
- Module structure
  - One generated mapping file to map theme variables to the modules variables, should be editable by user 
  - Mixins / Extends / Functions dependencies 
  - Modules dependencies using `<=`, `>=`, `~>`, ...
  - Set of rules and structure for modules and bundles development
  - module.json file
  - exemple:

```json
{
    "selector": "myclass",
    "version": "2.0.0",
    "author": "Sébastien Erfani",
    "url": "https://github.com/eternialz/base-module",
    "dependencies": {
        "base-extends": "~> 2.1.0",
        "base-mixins": "~> 2.1.0"
    },
    "unsupported": {
        "IE6-11": "Usage of custom properties"
    }
}
```

- Cli tool:
  - Build project
  - Import new modules and bundles
  - Generate new modules and bundles
  - Publish and update custom modules/bundles
  - Copy html template to clipboard from a module
  - Preview component or whole project in html file using modules mocks
  - Config file
  - Name conflicts

- Sourcemap generation

## File structure

### Project structure
```
    src
    ├── variables.sass
    ├── modules.json
    ├── modules.lock.json
    ├── config.json
    ├── browserlist
    │
    ├── custom-modules
    │   ├── mywebsite-typography
    │   ├── mywebsite-header
    │   └── ...
    │
    ├── modules
    │   ├── myframework-base
    │   ├── myframework-grid
    │   └── ...
    │
    └── vendors
        ├── normalize
        └── ...
```

### Module structure
```
    mymodule
    ├── module.json
    ├── mymodule.scss
    ├── _filename1.scss
    ├── _filename2.scss
    ├── _filename3.scss
    └── ...
```