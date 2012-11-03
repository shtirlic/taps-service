taps-service
============

Running [taps(simple database agnostic import/export app)](https://github.com/ricardochimal/taps) as self-hosted service.


Installation
------------

```bash
git clone git://github.com/shtirlic/taps-service.git
bundle install
```

Config
------

```bash
export DATABASE_URL=postgres://db_user:db_password@lremote_host/db_name
export TAPS_LOGIN=taps-service
export TAPS_PASSWORD=taps-super-taps
export TAPS_PORT=5000
```

Running
-------
taps-service is using [foreverb](https://github.com/DAddYE/foreverb) for daemonizing taps process

```bash
./bin/taps-service
```

```bash
foreverb start taps-service
```

Using
-----

Install taps gem

```bash
gem install taps
```

Pull database from taps-service host

```bash
taps pull postgres://local_dbuser:password@localhost/local_dbname http://taps-service:taps-super-taps@taps-service-host:5000
```

See more on [taps usage section](https://github.com/ricardochimal/taps#usage-client)


