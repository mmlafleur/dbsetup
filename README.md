# DBSETUP

A CLI tool that reads an [HCL](https://github.com/hashicorp/hcl) configuration file and makes changes to databases.

See [example.hcl](example.hcl) for an example configuration file.

## Building

Using [Go](https://golang.org/) and [gox](https://github.com/mitchellh/gox) installed properly:

```bash
# download deps if not already installed locally
go get

# build for existing platform
go build

# build for all platforms
gox
```

## Caveats

### Where Query

As of right now, `=` is the only type of where query supported.

### NULL Values

To use a `NULL` value in either a where or update map, use the string `"NULL"` and it will be used as `NULL`.

