# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.10.0]
As this release changes practically the entire interface of the crate, it is recommended that you
check out the [examples](https://github.com/mapeditor/rs-tiled/tree/master/examples) instead of the
changelog if you are migrating from an older version.

### Added
- Documentation to all crate items.
- Group layer support.
- Layer ID parsing.
- Object property parsing.
- Support for multiline string properties.
- SFML example.
- `Result` type.
- `Layer::parallax_x` & `Layer::parallax_y`.
- `Tileset::columns`.
- Missing derive and inline attributes.
- Tests for `zstd`-compressed files.


### Changed
- **Set the minimum Tiled TMX version to 0.13.**
- Refactor crate interface and internals to be more consistent, sound and easy to use.
- Hide GIDs as internal data; Provide a cleaner API.
- Contain all layer types in an enum as opposed to different containers.
- Rename `TiledError` to `Error`.
- `Tileset::tilecount` is no longer optional.
- Improve errors.
- Use `Color` type in color properties.
- Rename "colour"-related appareances to "color".
- Use `impl AsRef<Path>` where appropiate.
- Change `Tileset::image` to be a single image at most instead of a vector.
- Update README.
- Make layer and tileset names optional, defaulting to an empty string.
- Reorganize crate internally.
- Update `zstd` to `0.9`.

### Fixed
- Color parsing issues: #148

### Removed
- `Layer::layer_index`, as all layer types are now stored in a common container.
- `Map::source`, since it is known from where the load function was called.

## [0.9.5] - 2021-05-02
### Added
- Support for file properties.

### Fixed
- Parsing csv data without newlines (LDtk).

## [0.9.4] - 2021-02-07
### Added
- Support for layer offsets.

### Changed
- Feature gate zstd to allow targeting wasm32-unknown-unknown.

### Fixed
- Object visibility parsing.

## [0.9.3] - 2020-09-20
### Added
- Support for base64 and zstd compressed maps.
- Support for point objects.
- Support for infinite maps.

## [0.9.2] - 2020-05-09
### Added
- Properties to Tilesets.
- Test verifying `tileset.properties`.
- Tileset tile count parsing.
- Object `width` and `height` fields.

## [0.9.1] - 2020-03-29
### Changed
- Make fields on `Frame` `pub`.

## [0.9.0] - 2019-25-11 (?)
### Changed
- Migration to `rust 2018` and `?`
