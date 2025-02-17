# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog][keepachangelog] and this project adheres to [Semantic Versioning][semver].

## v2.13.0

### Added

- `fillable_by` field for fields specification [#34]
- Source `tech.base`
- Source `references.base`
- Source `av.taxi`
- Source `pledge.house`

[#34]:https://github.com/avtocod/specs/issues/34

## v2.12.0

### Added 

- Field with path `repairs.history.items[].assessor.name` [#37]

### Fixed

- Field with path `repairs.history.items[].insurer.name` has a duplicate, one instance has been deleted [#37]

[#37]:https://github.com/avtocod/specs/issues/37

## v2.11.0

### Changed

- Migrate to the [Travis CI][travis-ci]
- **PHP SDK** minimal PHP version now is 7.0 _([version 5.6 is not supported since 31 Dec 2018][php-supported-versions])_
- **PHP SDK** code a little bit refactored for PHP version 7.0

### Added

- **PHP SDK** Static code analyzer `phpstan` installed as `dev` dependency

[php-supported-versions]:http://php.net/supported-versions.php
[travis-ci]:https://travis-ci.org/avtocod/specs

## v2.10.0

### Added

- Vehicle marks specifications
- Vehicle models specifications
- **PHP SDK** object `VehicleMark`
- **PHP SDK** object `VehicleModel`
- **PHP SDK** method `getVehicleMarksSpecification`
- **PHP SDK** method `getVehicleModelsSpecification`

## v2.9.0

### Added

- Field with path `additional_info.vehicle.modifications.was_modificated` [#25]
- Field with path `registration_actions.items[].identifiers.pts` [#27]
- Field with path `registration_actions.items[].identifiers.sts` [#27]
- Field with path `additional_info.vehicle.passport.has_dublicate` [#27]

[#25]:https://github.com/avtocod/specs/issues/25
[#27]:https://github.com/avtocod/specs/issues/27

## v2.8.0

### Added

- Field with path `accidents.has_accidents`
- Field with path `fines.has_fines`

## v2.7.0

### Added

- Field with path `tech_data.brand.logotype.uri`
- Field with path `insurance.osago.items[].date.end`
- Field with path `calculate.osago.price.current.yearly.min`
- Field with path `calculate.osago.price.current.yearly.max`
- Field with path `calculate.osago.price.moscow.yearly.min`
- Field with path `calculate.osago.price.moscow.yearly.max`
- Field with path `calculate.osago.price.moscow_region.yearly.min`
- Field with path `calculate.osago.price.moscow_region.yearly.max`

## v2.6.0

### Added

- Field with path `taxi.history.items[].license.issued`
- Field with path `taxi.history.items[].license.status`
- Field with path `taxi.history.items[].company.address`
- Field with path `taxi.history.items[].number_plate.is_yellow`
- Field with path `taxi.history.items[].vehicle.brand.normalized`
- Field with path `taxi.history.items[].vehicle.model.normalized`
- Field with path `taxi.history.items[].vehicle.color`
- Field with path `taxi.history.items[].vehicle.sts.number`
- Field with path `taxi.history.items[].vehicle.sts.date.receive`
- Field with path `taxi.history.items[].region.code`
- Field with path `taxi.history.items[].cancel.reason`
- Field with path `taxi.history.items[].cancel.note`

## v2.5.0

### Added

- Field with path `leasings.items[].lessor.company.name`
- Field with path `leasings.used_in_leasing`

## v2.4.0

### Added

- Field with path `fines.items[].article.code`
- Field with path `fines.items[].article.description`

## v2.3.0

### Added

- Field with path `accidents.history.items[].org.name` [#12]

## v2.2.0

### Added

- Field with path `accidents.insurance.items[].date.event`
- Field with path `accidents.insurance.items[].insurer.type`
- Field with path `accidents.insurance.items[].accident.description`
- Field with path `accidents.insurance.items[].damage.raw`
- Field with path `accidents.history.items[].damage.raw`

## v2.1.0

### Added

- Field with path `pledges.items[].type` [#9]
- Field with path `pledges.items[].in_pledge` [#9]
- Repository issues templates
- Repository PR template

## v2.0.0

### Added

- Field with path `diagnostic_cards.items[].inspection.place`
- Field with path `restrictions.registration_actions.has_restrictions`
- Field with path `taxi.used_in_taxi`
- Field with path `utilizations.was_utilized`
- Field with path `stealings.is_wanted`
- Field with path `customs.history.items[].specification.raw`
- Report example `./fields/default/examples/full.json`
- Report example `./fields/default/examples/empty.json`
- Source `base.moscow`
- Source `customs.base`

### Changed

- Fields paths now follows next rule - if **path** element contains some iterable data inside, path element ends with `[]`
- Fields types `number` changed to `numeric`
- Field with path `tech_data.engine.volume` types now is `['float']`
- Field with path `tech_data.engine.power.hp` types now is `['float']`
- Field with path `tech_data.engine.power.kw` types now is `['float']`
- Field with path `calculate.tax.moscow.yearly.amount` types now is `['integer']`
- Field with path `calculate.tax.regions.yearly.amount` types now is `['integer']`
- Field with path `calculate.osago.coefficients.regional.value` types now is `['float']`
- Field with path `calculate.osago.price.current.yearly.amount` types now is `['integer']`
- Field with path `calculate.osago.price.moscow.yearly.amount` types now is `['integer']`
- Field with path `calculate.osago.price.moscow_region.yearly.amount` types now is `['integer']`
- Field with path `accidents.history.items[].vehicle.year` types now is `['integer']`
- Field with path `fines.items[].amount.value` types now is `['float']`
- Field with path `fines.items[].amount.total` types now is `['float']`
- Field with path `fines.items[].discount.percent` types now is `['float']`
- Field with path `car_price.items[].engine.volume` types now is `['float']`
- File `identifiers_types_list.json` renamed to `types_list.json`
- Internal structure in file `types_list.json`
- Internal structure in file `sources_list.json`
- Readme file totally re-writed
- PHP SDK require PHP version `5.6.4` and above
- PHP SDK now require `illuminate/support` package
- PHP SDK "specifications" methods in class `Specifications` now returns Collections of typed objects (array before)
- Minimal `phpunit/phpunit` version now is `5.7.10`
- Tests updated
- CI configuration updated

### Removed

- File `./CODE_OF_CONDUCT.md`
- File `./CONTRIBUTING.md`
- File `./.styleci.yml` (configuration transferred into `styleci.io`)
- Fields **names**
- Report example `./fields/default/examples/blank.json`
- Report example `./fields/default/examples/WBAFG41000L194195.json`
- Report example `./fields/default/examples/Z94CB41AAGR323020.json`
- Report example `./fields/default/examples/A1111111111111111.json`

[keepachangelog]:https://keepachangelog.com/en/1.0.0/
[semver]:https://semver.org/spec/v2.0.0.html
[#12]:https://github.com/avtocod/specs/issues/12
[#9]:https://github.com/avtocod/specs/issues/9
