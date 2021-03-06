4.2.1 / 2017-06-06
==================

* *BUGFIX* handle boms with profiles and other things by passing in System.properties 

4.2.0 / 2017-05-01
==================

* Add a `strictMode` flag - this will fail builds that have omitted versions that are not found in one of the recommendation sources

4.1.0 / 2017-03-14
==================

* Begin using `nebula.dependency-base` plugin.
    * Gives us `dependencyInsightEnhanced` task to show what was recommended instead of `selected by rule` in reasons

4.0.2 / 2017-02-03
==================

* Remove `getProjectConfiguration` deprecation warning on Gradle 3.4

4.0.1 / 2017-02-02
==================

* Close `InputStream` for properties and file based providers to avoid file locking issues on Windows

4.0.0 / 2017-02-01
==================

* BREAKING: Change to `ConflictResolvedStrategy`. First order recommendations will not auto-win, they will go through conflict resolution.

3.7.0 / 2016-12-13
==================

* Add `nebulaRecommenderBom` configuration as an alternative to the extension method `mavenBom`

3.6.3 / 2016-07-19
==================

* *BUGFIX* handle recommendations across a multiproject where subproject B depends on A which has a dependency it needs to pick up from recommendations

3.2.0 / 2016-01-11
==================

* Handle the gradle-dependency-lock V4 format

3.1.0 / 2015-12-03
==================

* Offer two strategies for how recommendations interact with transitive dependencies:
  - `ConflictResolved` - If there is no first order recommend-able dependency, a transitive will conflict resolve with dependencies in the recommendations listing
  - `OverrideTransitives` - If a recommendation conflicts with a transitive, pick the transitive

3.0.3 / 2015-11-04
==================

* Fixed bug where GString inputs to Maven BOM and Ivy module attribute were not appended with the file type

3.0.2 / 2015-10-15
==================

* Add a dependency on maven-module-builder which Gradle now shades

3.0.1 / 2015-09-15
==================

* Upgrade to Gradle 2.7

