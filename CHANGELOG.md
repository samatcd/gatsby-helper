# Release Notes for Gatsby Helper

## 2.0.0 - 2022-05-03

### Added
- Added Craft 4 compatibility.

### Changed
- The `builds`, `deltas`, and `sourceNodes` components can now be configured via `craft\services\Plugins::$pluginConfigs`.

## 1.1.3 - 2021-04-13

### Changed
- The `elementType` field on the `UpdatedNode` GraphQL type can also be null.

## 1.1.2 - 2021-12-09

### Fixed
- Fixed a bug where Gatsby incremental sourcing would break if elements were updated that had no real GraphQL support.

## 1.1.1 - 2021-12-08

### Added
- Added the `elementType` field to the `UpdatedNode` GraphQL type.

### Fixed
- Fixed an error with sourcing updated elements when the `graphQlTypePrefix` option was used.

## 1.1.0 - 2021-12-01

### Changed
- Added the `craftVersion` GraphQL query that returns more data points for the sourcing plugin to use when construct its queries.

## 1.0.9.1 - 2021-11-30

### Fixed
- Fixed an error in the SQL query when fetching updated elements. Again. ([craftcms/gatsby-source-craft#57](https://github.com/craftcms/gatsby-source-craft/issues/57))

## 1.0.9 - 2021-11-30

### Added
- Add additional queries to funnel information to the sourcing plugin. ([craftcms/gatsby-source-craft#58](https://github.com/craftcms/gatsby-source-craft/issues/58))

### Changed
- Exposed interface names are now correctly prefixed. ([craftcms/gatsby-source-craft#58](https://github.com/craftcms/gatsby-source-craft/issues/58))

### Fixed
- Fixed an error in the SQL query when fetching updated elements. ([craftcms/gatsby-source-craft#57](https://github.com/craftcms/gatsby-source-craft/issues/57))

## 1.0.8 - 2021-11-25

### Fixed
- Fixed a bug where moving structure elements around would not trigger a Gatsby incremental build correctly. ([craftcms/gatsby-source-craft/#48](https://github.com/craftcms/gatsby-source-craft/issues/48))
- Fixed a deprecation error. ([#17](https://github.com/craftcms/gatsby-helper/issues/17))

## 1.0.7 - 2021-10-21

### Fixed
- Fixed a bug where Gatsby Helper plugin would return incorrect results for incremental sourcing queries. ([#16](https://github.com/craftcms/gatsby-helper/issues/16))

## 1.0.6 - 2021-10-18

### Changed
- The `nodesUpdatedSince` query now also accepts `site` argument that specifies sites to query for updated elements.

### Fixed
- Fixed a bug where it would be impossible to query for updated element in a disabled site. ([craftcms/gatsby-source-craft#50](https://github.com/craftcms/gatsby-source-craft/issues/50))

## 1.0.5 - 2021-09-02

### Fixed
- Fixed a bug where preview builds would not be triggered for entries that had no drafts.

## 1.0.4 - 2021-07-06

### Fixed
- Fixed various issues where plugin was overly eager to trigger Gatsby site and preview builds. ([#14](https://github.com/craftcms/gatsby-helper/issues/14))

## 1.0.3 - 2021-05-26

### Fixed
- Fix a bug where it was impossible to update to 1.02 on installations that used PostgreSQL.

## 1.0.2 - 2021-05-21

### Fixed
- Fixed a bug that could lead to a Gatsby content sourcing failure. ([#13](https://github.com/craftcms/gatsby-helper/issues/13))

## 1.0.1 - 2021-03-30

### Changed
- Source node types registered on `craft\gatsbyhelper\events\RegisterSourceNodeTypesEvent::$types` should now be indexed by the type’s interface name.

### Fixed
- Fixed a bug that could lead to a Gatsby content sourcing failure. ([#9](https://github.com/craftcms/gatsby-helper/issues/9))
- Fixed a bug where the “Build Webhook URL” said it could be set to an alias or environment variable, but didn’t actually support them. ([#10](https://github.com/craftcms/gatsby-helper/pull/10))

## 1.0.0 - 2021-03-16

### Added
- Added a new “Build Webhook URL” setting that triggers Gatsby site builds on element save, if set. ([#7](https://github.com/craftcms/gatsby-helper/issues/7))

### Fixed
- Fixed a Javascript error that would occur when saving an entry without previewing it. ([#6](https://github.com/craftcms/gatsby-helper/issues/6))

## 1.0.0-beta.2 - 2020-12-01

> {note} You will need to ensure that your “Preview Webhook URL” setting is set correctly after updating.

### Added
- Added the correct header to trigger Gatsby Cloud previews correctly. ([#5](https://github.com/craftcms/gatsby-helper/issues/5))
- Added the “Preview Webhook URL” setting.

### Removed
- Removed the “Preview Server URL” setting.

### Fixed
- Fixed a bug where queries that would not be defined by the GraphQL schema were exposed to Gatsby, anyway.
- Fixed a bug where it was impossible to not provide server port for the preview server url. ([#4](https://github.com/craftcms/gatsby-helper/issues/4))

## 1.0.0-beta.1 - 2020-11-03

### Added
- Initial release
