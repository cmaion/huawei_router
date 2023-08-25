## Synopsis
A shell script to interact with Huawei 4G routers: status, SMS, restart and switch between 3G/4G/auto

Tested on:
* E5573Bs-320, B525s-23a

## Installation

Requires `curl`, `sed`, `base64` and `sha256sum`.
Set router ip, login and password in ~/.huawei_router:

```sh
$ vi ~/.huawei_router
ROUTER=192.168.1.1
LOGIN=admin
PASSWD=admin
```


## Usage

```sh
$ ./huawei_router
Usage:
  ./huawei_router [status|network|restart|month_stats|unread_sms_count|purge_sms_outbox|signal]
  ./huawei_router read_sms
  ./huawei_router send_sms <phone> <msg>
  ./huawei_router delete_sms <sms_id>
  ./huawei_router signal <3g|4g|auto>
  ./huawei_router request <api/...>
  ./huawei_router login_request <api/...>
$
```

Send a SMS:

```sh
$ ./huawei_router send_sms <phone_number> "Test message"
[huawei_router] Connecting
[huawei_router] Requesting api/user/login
[huawei_router] Requesting api/sms/send-sms
[huawei_router] SMS sent successfully
$
```

Restart:

```sh
$ ./huawei_router restart
[huawei_router] Connecting
[huawei_router] Requesting api/user/login
[huawei_router] Requesting api/device/control
[huawei_router] Restarted
```


## Author
[Cédric Maïon](https://github.com/cmaion)

## License
GPL3
