# mackerel-client [![Build Status](https://travis-ci.org/mackerelio/mackerel-client-ruby.svg?branch=master)](https://travis-ci.org/mackerelio/mackerel-client-ruby)

mackerel-client is a ruby library to access Mackerel (https://mackerel.io/). CLI tool `mkr` is also provided.

## Usage

```ruby
@mackerel = Mackerel::Client.new(:mackerel_api_key => "<Put your API key")
host = @mackerel.get_host("<hostId>")
```

# CLI

## Host

* Get host(s) information from hostname or service, role.
```
mkr host info [--name foo] [--service service] [--role role]
```

* Set status of a host
```
mkr host status --host-id foo --status working
```

* Retire a host
```
mkr host retire --host-id foo
```

* Get status of a host (not implemented yet)
```
mkr host status --host-id foo
```

## Authentication
```
export MACKEREL_APIKEY=foobar
```
