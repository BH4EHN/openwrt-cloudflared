# OpenWRT-Cloudflared

OpenWRT package of [Cloudflare Argo Tunnel client](https://developers.cloudflare.com/argo-tunnel/) ([Github](https://github.com/cloudflare/cloudflared))

## Prebuilt release

Prebuilt ipk can found in [releases](https://github.com/BH4EHN/openwrt-cloudflared/releases)

## Build it myself

- clone this repo to OpenWRT source or sdk `packages` subdirectory
- (optional) uncomment `upx` action in `Makefile` file `Build/Compile` section if `upx` is present in OpenWRT build environment, this can reduce almost 80% of go executable file size
- run `make menuconfig` or append `CONFIG_PACKAGE_cloudflared=y` to `.config` file
- run `make ./package/bh4ehn/cloudflared/compile` and wait for compile
- check `./bin/packages/<arch>/cloudflared_<version>_<arch>.ipk`

## How to use

- [Cloudflare Argo Tunnel offical document quickstart](https://developers.cloudflare.com/argo-tunnel/quickstart)
- [`cloudflared/cmd/cloudflared/main.go`](https://github.com/cloudflare/cloudflared/blob/master/cmd/cloudflared/main.go)
- [`cloudflared/cmd/cloudflared/access/cmd.go`](https://github.com/cloudflare/cloudflared/blob/master/cmd/cloudflared/access/cmd.go)
- [`cloudflared/cmd/cloudflared/tunnel/cmd.go`](https://github.com/cloudflare/cloudflared/blob/master/cmd/cloudflared/tunnel/cmd.go)