# docker-compose-timeseries

## setup

**this requires docker-compose > 1.19!**

You must create the .env for this compose:

```
DOMAIN=[your-domain]
LETSENCRYPT_ACCOUNT_EMAIL=[email]
INFLUXDB_ADMIN_USER=[username]
INFLUXDB_ADMIN_PASSWORD=[password]
TELEGRAF_TTN_INFLUXDB_DB=[database name, optional defaults to "ttn"]
TELEGRAF_TTN_INFLUXDB_USER=[username]
TELEGRAF_TTN_INFLUXDB_PASSWORD=[password]
TTN_MESHED_USER=[ttn app name on meshed-au]
TTN_MESHED_PASSWORD=[ttn application password]
GRAFANA_ADMIN_USER=[username]
GRAFANA_ADMIN_PASSWORD=[password]
INFLUXDB_VERSION=1.7
TELEGRAF_VERSION=1.12.6
GRAFANA_VERSION=6.5.1
```

## notes

you might want to create a writing user for influxdb rather than using the influxdb admin user to write from telegraf, but it shouldnt really matter.

You can just set *TELEGRAF_TTN_INFLUXDB_USER* to the same value as *INFLUXDB_ADMIN_USER* and *TELEGRAF_TTN_INFLUXDB_PASSWORD* to the same value as *INFLUXDB_ADMIN_PASSWORD*