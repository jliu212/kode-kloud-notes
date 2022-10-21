# Service Management With SYSTEMD

## SYSTEMD

[Serivce]
ExecStart

[Install]

## SYSTEMD tools

`systemctl`

- manage system state
- start stop
- enable disable
- list and manage units
- list and manage targets

`journalctl`
query systemd query

`systectl start`
`systemctl stop`
`systemctl restart`
`systemtcl reload`
`systemctl enable` enable when after automatcially reboot
`systemctl disable`

service state

- active: service running
- inactive: service3 stopped
- failed

`systemctl daemon-reload` reload the service manager

`systemctl edit project-mercury.service --full` restart the project without reload

`ssytem get-default`
`system set-defautl`

`systemctl list-units --all` list all the unites

`journalctl` trouble shooting issues as checks jourtnals and log entries
`jounralctl -b` from current boot
`jouralctl -u UNIT` for a specific unit
