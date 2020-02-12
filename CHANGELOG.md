# Changelog

## 0.7.0

* Change group to `nobody` instead of `nogroup`.

## 0.6.0

* Run as user `nobody` and group `nogroup` instead of `root`.
* Update Go to `v1.9.4`.

## 0.5.1

### Bug Fixes
* Include correct files in the docker build.

## 0.5.0

### Improvements
* Added home page with link to metrics.
* Added new fields to output parsed from passenger status command.
* Removed mentions of nginx as this exporter can support other integration modes.

### Breaking Changes
* Changed metrics prefix from `passenger_nginx` to `passenger`. This affects _all_ passenger metrics.
* Renamed metrics:
  * Changed `passenger_top_level_queue` to `passenger_top_level_request_queue`.
  * Changed `passenger_app_queue` to `passenger_app_request_queue`.
* Changed unit of passenger command timeout duration to seconds.
* Removed deprecated `code_revision` field from output parsed from passenger status command.
