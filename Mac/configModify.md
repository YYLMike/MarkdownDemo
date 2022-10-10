# Keyboard
### For macbook pro 13-inch, change "~" to esacpe, "command+~" to "`" and "option+command+~" to force quit
***
- Refer [mapping-a-physical-escape-key-on-a-macbook-pro-with-touch-bar](https://mybyways.com/blog/mapping-a-physical-escape-key-on-a-macbook-pro-with-touch-bar "mapping-escape")
- Install [Karbiner-elements and Karbiner-event-viewer](https://karabiner-elements.pqrs.org "karbainer-org")
- Modify `~/.config/karabiner/karabiner.json` by adding code to "rules: " inside the "[]"
```json
       rules: [
          {
            "description": "A Grave Escape",
            "manipulators": [
                {
                    "type": "basic",
                    "from": 
                        { "key_code": "grave_accent_and_tilde" },
                    "to": 
                        [ { "key_code": "escape" } ]
                },{
                    "type": "basic",
                    "from": { 
                        "key_code": "grave_accent_and_tilde", 
                        "modifiers": { "mandatory": [ "command" ] } 
                    },
                    "to": [ { "key_code": "grave_accent_and_tilde" } ]
                },{
                    "type": "basic",
                    "from": { 
                        "key_code": "grave_accent_and_tilde", 
                        "modifiers": { "mandatory": [ "option", "command" ] }
                    },
                    "to": [ {
                        "key_code": "escape",
                        "modifiers": [ "option", "command" ]
                    } ]
                }
            ]
          }
        ]
```
- Might modify the **security and privacy configuration of Mac** to allow karbiner to monitor keyboard 
- Use karbiner_event_viewer to check new configuration works
