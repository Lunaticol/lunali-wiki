# Obfuscate

[Power Type](https://lunali-wiki.readthedocs.io/en/latest/types/power_types/)

Causes player messages, username, and nametag to become obfuscated.

Type ID: `lunali:obfuscate`

| Field           | Type                                                                          | Default | Description                                                                            |
| --------------- | ----------------------------------------------------------------------------- | ------- | -------------------------------------------------------------------------------------- |
| `strength`      | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/)     | 0       | The strength of the obfuscation, applys to all booleans of Obfuscate. 1 = 100%, 0 = 0% |
| `username`      | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | false   | If the username in chat should be obfuscated.                                          |
| `chat_messages` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | false   | If chat messages should beobfuscated.                                                  |
| `nametag`       | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | false   | If your name tag should be obfuscated.                                                 |

!!! note

When Obfuscating the nametag, the characters will rapidly change. This is displayed in the tab menu aswell.

## Examples

```JSON
"obfuscate": {
    "type": "lunali:obfuscate",
    "strength": 0.2,
    "username": true,
    "chat_messages": false,
    "nametag": true
  }
```

This example will cause 20% of the players username and nametag to become obfuscated.
