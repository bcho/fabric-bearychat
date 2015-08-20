# fabric-bearychat

Fabric tasks aided with [bearychat][bc].

[bc]: http://bearychat.com


## Env vars

Tasks will use these env vars:

- `bearychat_hook` bearychat incoming robot hook (optional).
- `bearychat_channel` bearychat incoming channel (optional).


## Usage

### Send a notification

```python
from fabric_bearychat import notify


def cool_task():
  notify('cool task is running!')
```


### Notify when task is finished

```python
from fabric_bearychat import notify_when_finished


@notify_when_finished('task is finished')
def cool_task():
  pass


@notify_when_finished(on_failed='this should be failed')
def cool_task_that_fails():
  pass
```

## Installation

```bash
pip install fabric-bearychat
```



## LICENSE

MIT
