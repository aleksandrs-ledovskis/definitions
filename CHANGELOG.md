# Holiday definitions

## 5.0.0

Major semver bump due to changes related to the `year_ranges` option. The following keys have been renamed:

* `before` is now `until`
* `after` is now `from`

The behavior of these two options has not changed. To read more about the reasons behind this change please see the [associated ADR](doc/architecture/adr-002.md).

## 4.1.0

* Add new Emperor's Coronation Day holiday to `jp` (thanks to https://github.com/ttwo32)
* Add Thai Holidays (whoooo) (thanks to https://github.com/fabersky)
* Add Berlin's New International Women's Day to `de_be` (thanks to https://github.com/iGEL)
* Add Civic Holiday (Terry Fox Day) to `ca_mb` (thanks to https://github.com/akaspick)
* Fix Federal Reserve holidays for Independence Day (thanks to https://github.com/chadrschroeder)

## 4.0.0

Major semver bump due to changes in how non-standard regions will be handled going forward. Please see [issue-110](https://github.com/holidays/definitions/issues/110) for more details on this edge case and please also see the updates to our [SYNTAX guide](doc/SYNTAX.md#non-standard-regions) for the specified behavior going forward.

The following non-standard regions have been changed:

* `ecb_target` region changed to `ecbtarget`
* `federal_reserve` region changed to `federalreserve`
* `federal_reserve_banks` region changed to `federalreservebanks`
* `north_america_informal` region changed to `northamericainformal`
* `united_nations` region changed to `unitednations`
* `north_america` region changed to `northamerica`
* `south_america` region changed to `southamerica`

This change also includes updates to various other regions:

* Rename national sports day of `:jp` region from "体育の日" to "スポーツの日" (thanks to https://github.com/kunitoo)
* Fix 2020 `:jp` region holidays related tokyo olympics (thanks to https://github.com/kunitoo)
* Update Family Day date in `:ca_bc` region (thanks to https://github.com/roman-ih)
* Add Ukrainian holidays (`:ua` region code) (thanks to https://github.com/roman-ih)
* Add `federalreservebanks` region for observed bank holidays (thanks to Matt Hickman)

## 3.1.0

* Update `ch` to apply 'Neujahrstag' to overall region (thanks to https://github.com/phylor)
* Cosmetic spacing update for `us` definition, no behavior change

## 3.0.0

Major semver bump as the format for custom methods has been changed to complete [issue-24](https://github.com/holidays/definitions/issues/24). Downstream consumers will need to update to be able to parse them. However there are **no behavior changes** with this update.

In summary: we have switched to language-specific custom methods. Instead of a plain `source` field you will need a specific language implementation, e.g. `ruby`, `golang`, etc.

Currently we only have `ruby` but we can now expand these definitions for use in other languages. Please see the [custom methods ADR](doc/architecture/adr-001.md) for more in-depth information on why this change was made.

You can also view the updated ['Methods' section in the SYNTAX doc](doc/SYNTAX.md#methods) for more info and examples.

## 2.5.3

* Add missing `observed` logic for 'St. Patricks Day' in `gb_nir`

## 2.5.2

* Fix `de` issue cause by undefined `year_ranges` behavior in syntax

## 2.5.1

* Fix Federal Reserve Independence Day tests

## 2.5.0

* Change Emperor's Birthday for `jp` definitions (thanks to https://github.com/ttwo32)
* Add German Reformation  to four more states starting in 2018 (thanks to https://github.com/jensberke)
* Add 'La Mercè' to official holidays in Catalunya, Spain (thanks to https://github.com/fabersky)
* Fix Federal Reserve Saturday holidays (thanks to https://github.com/mikecanann)
* Fix the CoC link in CONTRIBUTING doc
* Remove ruby 2.2 and add ruby 2.5 to travis tests

## 2.4.0

* Add new holidays for Canada (thanks to https://github.com/alejandrok5)

## 2.3.0

* Fix typo in `:at` definitions (thanks to https://github.com/AlexMarold)
* Add holidays for Jersey and Guernsey (thanks to https://github.com/timkrins)
* Update Travis config to fix build issues related to imminent release of ruby 2.5

## 2.2.1

* Small updates to tests in the `:de` regions. No behavior changes.

## 2.2.0

* Audit provincial holidays in Canada (thanks to https://github.com/slucaskim)
* Add civic holiday for `ca_pe`  (thanks to https://github.com/slucaskim)
* Correct reformation day for `de` (thanks to https://github.com/spaceneedle2019)

## 2.1.1

* Comment out test for `추석` until a discussion can be had in [issue 69](https://github.com/holidays/definitions/issues/69) (nice)

## 2.1.0

Update the following regions:

* `ca_ab` - change 'Heritage Day' to informal
* `kr` - Update '추석 연휴' and `설날 연휴` for accuracy
* `cl` - Add 'San Pedro y San Pablo', update 'Encuentro de Dos Mundos', and add 'Día de las Iglesias Evangélicas y Protestantes'

## 2.0.0

* Update `tr`, `fedex` for accuracy
* Completely change the test format to no longer use ruby source code! Hooray! This should cause no behavior differences,
  any differences or changes in behavior should be considered a regression.

## 1.7.1

A small bugfix that resolves the naming issues of two regions in the 'index.yaml' file. No other outward changes.

## 1.7.0

Here are the changes:

* Add Estonian definitions
* Enhance France definitions
* Correct and enhance German definitions
* Enhance Portuguese definitions
* Add Malta definitions
* Add Serbian definitions
* Add Georgian definitions
* Use Orthodox easter calculations in appropriate regions
* Add Russian definitions
* Add Turkey definitions
* Enhance US definitions (lots of individual US states!)
* Update South Australian definitions

## 1.6.1

* Update `ca` test for correctness. See below for more information.

Unfortunately due to our current setup it is possible for definitions/tests in this repository to appear 'valid' but only
fail when we run them in the actual ruby holidays repo. This is a known issue (#42) and needs to be addressed.

In the meantime, this is a bugfix release to ensure we can release v5.6.0 of the ruby repo.

## 1.6.0

Updates to the following Canadian regions: `ca_ab, ca_bc, ca_mb, ca_nt, ca_nu, ca_on, ca_sk, ca_yt, ca_pe`

## 1.5.1

* Fix error in `fedex` custom method `day_after_thanksgiving`

## 1.5.0

* Update NYSE to fix observed NYD
* Use native language for KR
* Use native language for VI
* Update AU definitions for accuracy
* Update KR definitions to include lunar holiday calculations
* Add VI definitions

## 1.4.0

* :au - corrects holidays for certain regions
* :vi - reports holiday names in Vietnamese instead of English, adds 1 additional holiday (Giỗ tổ Hùng Vương)

## 1.3.0

* Add Travis badge to README
* Add Tunisian holidays
* Correct various Australian holidays
* Updates various German regions to be more accurate
* Changed 'nf' to 'nl' for Newfoundland & Labrador
* Changed 'yk' to 'yt'kkk

## 1.2.1

* Fix syntax and test errors in au and ca def tests

## 1.2.0

* updates jp defs to fix 'Foundation Day' name
* Fix ca defs for observed holidays
* Update au defs to have Christmas and Boxing Day for all of Australia instead of just individual territories
* Update ie defs to consolidate "St Stephen's Day" to use common method instead of custom method

## 1.1.0

* Add HK definitions
* Add KR definitions
* Fix small bug in JP definitions

## 2016 1.0.0

Initial creation of this repository

This contains all of the definitions currently in the holidays repository but split out into its own repository. It will
be added as a submodule of the ruby repository, which will be responsible for generating its final classes.

The idea is that we will have repositories for multiple languages and each language is responsible for using the definitions
as it sees fit.
