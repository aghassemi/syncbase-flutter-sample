# Quick example using [Flutter](https://flutter.io) & [Syncbase](https://github.com/vanadium/mojo.syncbase)

## Prerequisite
- [Mojo](https://github.com/domokit/mojo) must be setup and `$MOJO_DIR` must point to it.
- [Flutter](http://flutter.io) You must have a clone of https://github.com/flutter/flutter. Please update the `pubspec.yaml` file
and set `flutter` and `flutter_tools` dependency paths to match your clone directory.

## To run
```
pub get
pub run flutter_tools build && \
pub run flutter_tools run_mojo \
  --mojo-path $MOJO_DIR/src \
  --android \
  --mojo-debug \
  --enable-multiprocess \
  --map-origin="https://mydartapp.mojoapps.io/=$PWD" \
  --args-for="https://mydartapp.mojoapps.io/packages/syncbase/mojo_services/android/syncbase_server.mojo --root-dir=/data/data/org.chromium.mojo.shell/app_home/syncbasedata" \
  --no-config-file
```

### To see logs from the [V23](https://v.io) framework
`adb logcat *:S vlog:*`
