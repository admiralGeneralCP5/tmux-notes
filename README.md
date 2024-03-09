# Tmux - terminal multiplexer
## Layers:

```txt
Session
┗━━Window
   ┗━━Pane
``` 

## Sessions:
| Action | Command |
| :--- | ---: |
| start a new session | tmux | 
| start a new session with custom name | tmux new -s \<name> |
| attach to last used session | tmux a | 
| attach to a specified session | tmux a -t \<name> | 
| detach from a session| ⌃B D | 
| | tmux detach |
| list sessions | tmux ls |

## Navigation & Killing
| Actions | Command |
| :--- | ---: |
| sleect session, window, and or pane | ⌃B W |
| kills the selected/current pane | ⌃B X |
| kills the selected/current window | ⌃B & |
| kill specified session | tmux kill-session -t \<name> |
| kill all sessions | tmux kill-server |
| enables scrolling | ⌃B [ |

## Windows:
| Action | Command |
| :--- | ---: |
| new window | ⌃B C |
| move to next window | ⌃B N |
| rename current window | ⌃B , |

## Panes:
| Action | Command |
| :--- | ---: |
| horizontal split | ⌃B % |
| vertical split | ⌃B " |
| switch panes with directional arrows | ⌃B ↑↓→← |
| show pane indexes | ⌃B Q |
| switch to pane by index | ⌃B Q \<index> |

## Turn Mouse On
#### For the current sessions:
```txt
⌃B :
set -g mouse on
⏎
```

#### For all sessions:
>make / edit the config file
```shell
nano .tmux.conf
```

>add this to the file
```txt
set -g mouse on
```