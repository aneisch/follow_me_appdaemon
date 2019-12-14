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
