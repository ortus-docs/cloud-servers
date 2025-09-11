# Changelog for BoxLang MiniServer for Ubuntu 24.04 LTS

## Version 1.5.0
### Changed
* Bump BoxLang version to 1.5.0+41
* Systemd daemon for manage BoxLang MiniServer process is now `boxlang-site`

### Added
* startBoxLangSite.sh script is now on charge to start|stop BoxLang MiniServer process through boxlang-site Systemd daemon
    - It checks if there is custom site under `/web/boxlang-site/wwwroot` placed by users and if there is a server.json file, if not start default ColdBox Application under `/web/boxlang-site/default`

## Version 1.4.0
### Added
* Bump BoxLang version to 1.4.0

## Version 1.3.0
### Added
* BoxLang update to 1.3.0

## Version 1.1.0
### Added
* BoxLang MiniServer now support URL Rewrites
### Removed
* Nginx Reverse Proxy

## Version 0.3.0

* Initial Release

