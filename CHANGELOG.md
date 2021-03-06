# Instant Analytics Changelog

## 1.1.7 - 2020.04.16
### Fixed
* Fixed Asset Bundle namespace case

## 1.1.6 - 2020.04.06
### Changed
* Updated to latest npm dependencies via `npm audit fix` for both the primary app and the docs
* Updated deprecated functions for Commerce 3

### Fixed
* Fixed an issue where an error would be thrown if a brand field didn't exist for a given Product Type

## 1.1.5 - 2020.02.05
### Fixed
* Fixed the logic used checking the **Create GCLID Cookie** setting by removing the not `!`

## 1.1.4 - 2020.01.15
### Added
* Added **Create GCLID Cookie** setting to control whether ID creates cookies or not

## 1.1.3 - 2019.11.25
### Added
* Add currency code to transaction event

### Changed
* Replace use of order number (UID) with the much more human friendly order reference
* Documentation improvements

## 1.1.2 - 2019.11.01
### Changed
* Fixed an issue that would cause it to throw an error on the settings page if you didn't have ImageOptimized installed

## 1.1.1 - 2019.09.27
### Changed
* Fixed an issue on the Settings page where it would blindly pass in null values to `getLayoutById()`
* If you're using Craft 3.1, Instant Analytics will use Craft [environmental variables](https://docs.craftcms.com/v3/config/environments.html#control-panel-settings) for secrets
* Fixed an issue where `get_class()` was passed a non-object
* Updated Twig namespacing to be compliant with deprecated class aliases in 2.7.x
* Updated build system and `package.json` deps as per `npm audit`

## 1.1.0 - 2018.11.19
### Added
* Added Craft Commerce 2 support for automatic sending of Google Analytics Enhanced eCommerce events  

### Changed
* Retooled the JavaScript build system to be more compatible with edge case server setups

## 1.0.11 - 2018.10.05
### Changed
* Updated build process

## 1.0.10 - 2018.08.25
### Changed
* Fixed an issue integrating with SEOmatic

## 1.0.9 - 2018.08.25
### Changed
* Fixed an issue where the return type-hinting was incorrect
* Handle cases where a `null` IAnalytics object is returned

## 1.0.8 - 2018.08.24
### Changed
* Fixed an issue where manually using the `{% hook isSendPageView %}` would throw an error

## 1.0.7 - 2018.08.24
### Added
* Added welcome screen after install
* Automatically set the `documentTitle` from the SEOmatic `<title>` tag, if SEOmatic is installed
* Automatically set the `affiliation` from the SEOmatic site name, if SEOmatic is installed

### Changed
* Lots of code cleanup
* Moved to a modern webpack build config for the Control Panel
* Added install confetti

## 1.0.6 - 2018.03.22
### Added
* Send only the path, not the full URL to Google Analytics via `eventTrackingUrl()`
* Gutted the Commerce service, pending Craft Commerce 2

## 1.0.5 - 2018.02.01
### Added
* Renamed the composer package name to `craft-instantanalytics`

## 1.0.4 - 2018.01.10
### Changed
* Set the documentPath for events, too

## 1.0.3 - 2018.01.08
### Changed
* Fixed an issue with parsing of the `_ga`_ cookie

## 1.0.2 - 2018.01.02
### Changed
* Fixed the `eventTrackingUrl` to work properly

## 1.0.1 - 2017.12.06
### Changed
* Updated to require craftcms/cms `^3.0.0-RC1`
* Switched to `Craft::$app->view->registerTwigExtension` to register the Twig extension

## 1.0.0 - 2017-10-27
### Added
- Initial release
