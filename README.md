## Synopsis
A shell script to interact with Huawei 4G routers: status, SMS

Tested on:
* E5573Bs-320, B525s-23a


## Usage

```sh
$ ./huawei_router
Usage:
  ./huawei_router [status|network|month_stats|unread_sms_count|purge_sms_outbox]
  ./huawei_router read_sms
  ./huawei_router send_sms <phone> <msg>
  ./huawei_router delete_sms <sms_id>
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


## Author
[Cédric Maïon](https://github.com/cmaion)

## License
GPL3
