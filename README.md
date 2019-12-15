# Follow Me App
[![hacs_badge](https://img.shields.io/badge/HACS-Default-orange.svg)](https://github.com/custom-components/hacs)
<br><a href="https://www.buymeacoffee.com/aneisch" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-black.png" width="150px" height="35px" alt="Buy Me A Coffee" style="height: 35px !important;width: 150px !important;" ></a>

_An app to allow easy coupling of entities_

## Installation

This app is best installed using [HACS](https://github.com/custom-components/hacs), so that you can easily track and download updates.

Alternatively, you can download the `follow_me` directory from inside the `apps` directory here to your local `apps` directory, then add the configuration to enable the `follow_me` module.

## How it works

You can define an instance of the app in your apps.yaml file for every "group" of leader/follower you have. When the leader turns on, the follower will, well... follow! Same goes for off. You can also make the follower assume the inverted state of the leader. Only works with on/off state. 

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
