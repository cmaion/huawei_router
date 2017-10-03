## Synopsis
A shell script to interact with Huawei 4G routers: status, SMS

Tested on:
* E5573Bs-320

## Installation

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
  ./huawei_router [status|network|month_stats|unread_count|purge_outbox]
  ./huawei_router send <phone> <msg>
  ./huawei_router request <api/...>
  ./huawei_router login_request <api/...>
$
```

Send a SMS:

```sh
$ ./huawei_router send <phone_number> "Test message"
[huawei_router] Connecting
[huawei_router] Requesting api/user/login
[huawei_router] Requesting api/sms/send-sms
[huawei_router] SMS sent successfully
$
```


## Author
[Cédric Maïon](https://github.com/cmaion)

## License
GPL3
