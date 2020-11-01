<a href="https://photon-platform.net/">
    <img src="https://photon-platform.net/user/images/photon-logo-banner.png" alt="photon" title="photon" align="right" height="120" />
</a>


# photon ✴ Organization

## 0.1.0
> structure, style and logic for content about organizations

---

![GitHub release](https://img.shields.io/github/v/tag/photon-platform/grav-theme-photon)

- [configuration](#configuration)
- [templates](#templates)
- [scaffolds](#scaffolds)
- [scss](#scss)
- [assets](#assets)
- [languages](#languages)

# configuration
blueprints.yaml

fields:
- enabled
- built_in_css
- built_in_js
- notes

Before configuring this plugin, you should copy the `user/plugins/photon-organization/photon-organization.yaml` to `user/config/plugins/photon-organization.yaml` and only edit that copy.

Here is the default configuration and an explanation of available options:

```
enabled: true
built_in_css: true
built_in_js: true

description: Custom Text added by the **photon-organization** plugin (disable plugin to remove)
```

Note that if you use the admin plugin, a file with your configuration, and named photon-organization.yaml will be saved in the `user/config/plugins/` folder once the configuration is saved in the admin.


# blueprints

```sh
blueprints
└── organization.yaml
```

### Organization
organization.yaml
extends: article
fields:
- header.data.organization
  - .@type
  - .name
  - .email
  - .telephone
  - .url
  - header.data.organization.location
    - header.data.organization.location.address
      - header.data.organization.location.address.streetAddress
      - header.data.organization.location.address.postOfficeBoxNumber
      - header.data.organization.location.address.addressLocality
      - header.data.organization.location.address.addressRegion
      - header.data.organization.location.address.postalCode
      - header.data.organization.location.address.addressCountry
    - header.data.organization.location.geo
      - header.data.organization.location.geo.latitude
      - header.data.organization.location.geo.longitude

# templates

```sh
templates
├── _articles
│   ├── _block
│   │   └── organization_collection.html.twig
│   ├── organization-excerpt.html.twig
│   └── organization.html.twig
├── _json-ld
│   └── organization.html.twig
└── organization.html.twig
```

# scaffolds

```sh
scaffolds
└── organization.md
```

# scss

```sh
scss
├── articles
│   └── _organization.scss
├── templates
│   └── _organization.scss
└── organization.scss
```

# assets

```sh
assets
├── organization.css
├── organization.css.map
└── organization.js
```

# languages

```sh
languages
└── en.yaml
```


## Installation

- all photon plugins are installed as git submodules. More on that later.



## Configuration


## Usage

Select template type when creating a new page

## Credits


## To Do

- [ ] Future plans, if any


copyright &copy; 2020
