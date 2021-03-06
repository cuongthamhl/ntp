## ANXS - ntp [![Build Status](https://travis-ci.org/ANXS/ntp.png)](https://travis-ci.org/ANXS/ntp)

Ansible role which installs and configures ntp.


#### Requirements & Dependencies
- Tested on Ansible 1.3 or higher.


#### Variables

```yaml
ntp_driftfile: "/var/lib/ntp/ntp.drift"
ntp_statsdir: "/var/log/ntpstats/"
ntp_leapfile: "/etc/ntp.leapseconds"
ntp_servers: ["0.pool.ntp.org", "1.pool.ntp.org", "2.pool.ntp.org", "3.pool.ntp.org"]

ntp_restricts:
  - "restrict 0.pool.ntp.org nomodify notrap noquery"
  - "restrict 1.pool.ntp.org nomodify notrap noquery"
  - "restrict 2.pool.ntp.org nomodify notrap noquery"
  - "restrict 3.pool.ntp.org nomodify notrap noquery"
  - "restrict default kod notrap nomodify nopeer noquery"
  - "restrict 127.0.0.1 nomodify"
  - "restrict -6 default kod notrap nomodify nopeer noquery"
  - "restrict -6 ::1 nomodify"
```


#### Testing
This project comes with a VagrantFile, this is a fast and easy way to test changes to the role, fire it up with `vagrant up`

See [vagrant docs](https://docs.vagrantup.com/v2/) for getting setup with vagrant


#### License

Licensed under the MIT License. See the LICENSE file for details.


#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/ANXS/ntp/issues)!
