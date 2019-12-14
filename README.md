# Follow Me App
[![hacs_badge](https://img.shields.io/badge/HACS-Default-orange.svg?style=for-the-badge)](https://github.com/custom-components/hacs)
<a href="https://www.buymeacoffee.com/aneisch" target="_blank"><img
src="https://www.buymeacoffee.com/assets/img/custom_images/orange_img.png"
alt="Buy Me A Coffee" style="height: 41px !important;width: 174px
!important;box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5)
!important;-webkit-box-shadow: 0px 3px 2px 0px rgba(190, 190, 190, 0.5)
!important;" ></a>

_An app to allow easy coupling of entities_

## Installation

This app is best installed using [HACS](https://github.com/custom-components/hacs), so that you can easily track and download updates.

Alternatively, you can download the `follow_me` directory from inside the `apps` directory here to your local `apps` directory, then add the configuration to enable the `follow_me` module.

## How it works

You can define an instance of the app in your apps.yaml file for every "group" of leader/follower you have. 

## App configuration

```yaml
follow_lamps:
  module: follow_me
  class: Follow
  leader: group.living_room_lamps
  follower: switch.entertainment_center_lights,switch.christmas_tree
```

key | optional | type | default | description
-- | -- | -- | -- | --
`module` | False | string | | The module name of the app.
`class` | False | string | | The name of the Class.
`leader` | False | string OR comma separated | | The entity_id(s) you want to lead.
`follower` | False | string OR comma separated | | The entity_id(s) you want to follow leader state.
`invert` | True | boolean | False | Invert behavior of leader (if a leader turns off, followers turn on).

## Issues/Feature Requests

Please feel free to open any issues or feature requests!