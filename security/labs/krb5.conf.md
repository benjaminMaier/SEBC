```
[libdefaults]
default_realm = BENJAMINMAIER.SG
dns_lookup_kdc = false
dns_lookup_realm = false
ticket_lifetime = 86400
renew_lifetime = 604800
forwardable = true
default_tgs_enctypes = arcfour-hmac
default_tkt_enctypes = arcfour-hmac
permitted_enctypes = arcfour-hmac
udp_preference_limit = 1
kdc_timeout = 3000
[realms]
BENJAMINMAIER.SG = {
kdc = ip-10-0-0-222.eu-west-1.compute.internal
admin_server = ip-10-0-0-222.eu-west-1.compute.internal
}
```