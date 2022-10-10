Keyboard
======
1. For macbook pro 13-inch, change "~" to esacpe, "command+~" to "`" and "option+command+~" to force quit
  a. Install from https://karabiner-elements.pqrs.org
  b. modify ~/.config/karabiner/karabiner.json by adding code to "rules: []" inside the "[]"
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
  c. use karabiner_viewer to check new configuration works
  p.s. might change the security setup to allow karabiner to monitor keyboard 
