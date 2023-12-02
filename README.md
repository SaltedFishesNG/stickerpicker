Using `/devtools` -> Other -> Explore account data in Element Web (**not**
"room account data", must be the global one), edit the `m.widgets` account
data event to have the following content:

```json
{
    "stickerpicker": {
        "content": {
            "type": "m.stickerpicker",
            "url": "https://saltedfishesng.github.io/stickerpicker/?theme=$theme",
            "name": "Stickerpicker",
            "data": {}
        },
        "sender": "@you:matrix.server.name",
        "state_key": "stickerpicker",
        "type": "m.widget",
        "id": "stickerpicker"
    }
}

```

If you do not yet have a `m.widgets` event, simply create it with that content.
You can also [use the client-server API directly](https://spec.matrix.org/latest/client-server-api/#put-matrix-client-r0-user-userid-account-data-type) instead of using Element Web.
