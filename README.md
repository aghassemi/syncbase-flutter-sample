# Quick example using [Flutter](https://flutter.io) & [Syncbase](https://github.com/vanadium/mojo.syncbase)

## Prerequisite
[Mojo](https://github.com/domokit/mojo) must be setup and `$MOJO_DIR` must point to it.

## To run
```
pub upgrade
pub run sky_tools build && \
pub run sky_tools run_mojo \
  --mojo-path $MOJO_DIR/src/mojo/devtools/common/mojo_run \
  --android \
  --mojo-debug \
  -- \
  --enable-multiprocess \
  --map-origin="https://mydartapp.mojoapps.io/=$PWD" \
  --args-for="https://mydartapp.mojoapps.io/packages/syncbase/mojo_services/android/syncbase_server.mojo --root-dir=/data/data/org.chromium.mojo.shell/app_home/syncbasedata" \
  --no-config-file \
  --free-host-ports
```

### To see logs from the [V23](https://v.io) framework
`adb logcat *:S vlog:*`
