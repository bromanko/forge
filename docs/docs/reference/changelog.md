# Changelog

#### 0.4.12 (May 8th, 2018)

* Fix processing of k8s directories that only contain subdirectories: [#193](https://github.com/datawire/forge/issues/193)

#### 0.4.11 (April 27th, 2018)

* Only process .yml and .yaml files underneath the k8s dir: [#186](https://github.com/datawire/forge/issues/186)

#### 0.4.10 (April 26th, 2018)

* Properly handle sub-directories of the k8s manifest dir: [#183](https://github.com/datawire/forge/issues/183)

#### 0.4.9 (April 5th, 2018)

* Use a heuristic to ignore kubernetes service.yaml files during discovery: [#61](https://github.com/datawire/forge/issues/61)

#### 0.4.8 (April 4th, 2018)

* Change the forge log file to includ the user and date: [#171](https://github.com/datawire/forge/issues/171)

#### 0.4.7 (March 27th, 2018)

* Add a `verify: false` option for use with self-signed docker registries: [#141](https://github.com/datawire/forge/issues/141)

#### 0.4.6 (March 13th, 2018)

* Exclude storage classes from forge delete: [#162](https://github.com/datawire/forge/issues/162)
* Fix forge delete for clusterrole and cluseterrolebinding: [#163](https://github.com/datawire/forge/issues/163)

#### 0.4.5 (March 8th, 2018)

* Fix delete of resources in namespaces: [#160](https://github.com/datawire/forge/issues/160)

#### 0.4.4 (March 6th, 2018)

* Make the branch * pattern match when there is no branch: [#157](https://github.com/datawire/forge/issues/157)
* Make build.images include containers by name as well as filename: [#158](https://github.com/datawire/forge/issues/158)

#### 0.4.3 (Feb 22nd, 2018)

* Add profiles to forge.yaml: [#146](https://github.com/datawire/forge/issues/146)
* Add a local docker registry: [#145](https://github.com/datawire/forge/issues/145)

#### 0.4.2 (Feb 16th, 2018)

* Make docker user and password optional in forge.yaml
* Make `forge delete` faster
* Add service and profile arguments to `forge list`

#### 0.4.1 (Feb 9th, 2018)

* Don't tag or delete namespaces: [#139](https://github.com/datawire/forge/issues/139)

#### 0.4.0 (Feb 8th, 2018)

* Added list, delete, and deploy --prune for [managing services](managing-services.md): [#139](https://github.com/datawire/forge/issues/139)
* Added [service metadata](metadata.md) to forge resources: [#139](https://github.com/datawire/forge/issues/139)
* Added support for gcloud auth: [#143](https://github.com/datawire/forge/issues/143)
* Added support for imagebuilder: [#138](https://github.com/datawire/forge/issues/138)

#### 0.3.25 (Jan 22nd, 2018)

* Make namespace required and improve the documentation: #125

#### 0.3.24 (Jan 16th, 2018)

* Allow container names to be customized: #46
* Allow --includeIPRanges to be passed to Istio: #121
* Publish internal API docs
* Better schema documentation

#### 0.3.23 (Dec 1st, 2017)

* Prevent concurrent git pulls for monorepo style usage: [#109](https://github.com/datawire/forge/issues/109)

#### 0.3.22 (Dec 1st, 2017)

* Fix bad reference to CLIError.

#### 0.3.21 (Nov 30th, 2017)

* Only git pull for services auto cloned into .forge: [#109](https://github.com/datawire/forge/issues/109)
* Use a single shared .forge for each service tree: [#107](https://github.com/datawire/forge/issues/107)
* Added a search-path option to forge.yaml for local services: [#106](https://github.com/datawire/forge/issues/106)
* Use shallow cloning: [#105](https://github.com/datawire/forge/issues/105)

#### 0.3.20 (Nov 28th, 2017)

* Flatten nested service dependencies into the topmost .forge directory.

#### 0.3.19 (Nov 28th, 2017)

* Add the --no-color option to git log. This fixes [#99](https://github.com/datawire/forge/issues/99)

#### 0.3.18 (Nov 27th, 2017)

* Add extra debug logging when querying ECR.

#### 0.3.17 (Nov 7th, 2017)

* Set default encoding to UTF-8.
* Added `forge pull` command: [#90](https://github.com/datawire/forge/issues/90)

#### 0.3.16 (Nov 7th, 2017)

* Added first class support for ECR, and GCR: [#70](https://github.com/datawire/forge/issues/70)

#### 0.3.15 (Nov 6th, 2017)

* Fixed unfiled bug in version computation. (Missing errno import.)

#### 0.3.14 (Oct 27th, 2017)

* Fixed unfiled bug in handling of undefined variables in jinja2 templates.

#### 0.3.13 (Oct 24th, 2017)

* Fixed unfiled bug in handling of service dependencies.
* Fixed unfiled bug in handling of .gitignore.

#### 0.3.12 (Oct 24th, 2017)

* Added --branch command line argument.

#### 0.3.11 (Oct 23rd, 2017)

* Fixed handling of service dependencies: [#74](https://github.com/datawire/forge/issues/74)

#### 0.3.10 (Oct 17th, 2017)

* Added access to branch variable from service.yaml.
* Use branch variable to provide preview endpoint in the java-gradle-spark example.

#### 0.3.9 (Oct 16th, 2017)

* Added support for profiles: See the [profiles documentaiton](profiles.md) for more details.

#### 0.3.8 (Oct 13th, 2017)

* Fixed regression: don't swallow errors on apply.

#### 0.3.7 (Oct 9th, 2017)

* Fixed image existence check for ECR.

#### 0.3.6 (Oct 6th, 2017)

* Fixed bug in copy logic when subdirectories are used in the sources list.

#### 0.3.5 (Oct 6th, 2017)

* Avoid terminal being messed up from docker commands.

#### 0.3.4 (Oct 6th, 2017)

* Fixed gcr integration: [#67](https://github.com/datawire/forge/issues/67)

#### 0.3.3 (Oct 6th, 2017)

* Incremental rebuild of containers. See [here](customize-container-builds.md) for documentation.
* Additional documentation on customizing container builds. (See above link.)

#### 0.3.2 (Sep 29th, 2017)

* Warn on undefined jinja variables as a prelude to enabling strict mode: [#64](https://github.com/datawire/forge/issues/44)
* Display output of rendered service yaml when it fails to parse

#### 0.3.1 (Sep 29th, 2017)

* Improved CLI output: [#32](https://github.com/datawire/forge/issues/32)
* Respect .gitignore when computing versions: [#44](https://github.com/datawire/forge/issues/44)
* Added config object to service.yaml schema: [#22](https://github.com/datawire/forge/issues/22)
* Moved workdir to .forge: [#40](https://github.com/datawire/forge/issues/40)

#### 0.3 (Sep 12th, 2017)

* Restructured CLI and improved documentation: [#27](https://github.com/datawire/forge/issues/27)
* Added 'build metadata' command to show all variables and metadata that can be interpolated: [#30](https://github.com/datawire/forge/issues/30)

#### 0.2.16 (August 23, 2017)

* Added a schema for service.yaml: [#22](https://github.com/datawire/forge/issues/22)
* Added support for customizing docker builds: [#33](https://github.com/datawire/forge/issues/33)

#### 0.2.14 (August 23, 2017)

* Add version to build metadata.

#### 0.2.13 (August 23, 2017)

* Add command line arg: -n,--namespace=<name> for deploy.

#### 0.2.12 (August 22, 2017)

* Pass the K8S_NAMESPACE environment variable through to kubectl

#### 0.2.11 (August 21, 2017)

* noop release for travis

#### 0.2.10 (August 16, 2017)

* Change to standalone pex binary for easier distribution/installation.
* Compute version based on service subdirectory rather than entire repo.

#### 0.2.9 (July 24, 2017)

* Environment based customization of service configuration: [#23](https://github.com/datawire/forge/issues/23)
* Make the forge setup validation image configurable:  [#24](https://github.com/datawire/forge/issues/24)

#### 0.2.8 (July 13, 2017)

* Service level dependencies: [#8](https://github.com/datawire/forge/issues/8), [#16](https://github.com/datawire/forge/issues/16)
* Search for service.yaml in parent directories: [#20](https://github.com/datawire/forge/issues/20)

#### 0.2.7 (July 12, 2017)

* Don't blow up when there is no USER variable set: [#18](https://github.com/datawire/forge/issues/18)

#### 0.2.6 (July 7, 2017)

* Reduce some noise when reporting errors.

#### 0.2.5 (June 30, 2017)

* Added istio support: [#13](https://github.com/datawire/forge/issues/13)

#### 0.2.4 (June 30, 2017)

* Less noise on setup.

#### 0.2.3 (June 26, 2017)

* Clearer reporting of docker authentication errors.

#### 0.2.2 (June 26, 2017)

* Omit stack trace for expected errors.

#### 0.2.1 (June 26, 2017)

* Pin eventlet version dependency.

#### 0.2 (June 26, 2017)

* Better output and improved error reporting for background tasks.
* Improved docs around global config and docker password: [#11](https://github.com/datawire/forge/issues/11)
* Clarified setup output and provide better defaults: [#10](https://github.com/datawire/forge/issues/10), [#6](https://github.com/datawire/forge/issues/6)

#### 0.1 (May 24, 2017)

* Initial release

**Still have questions? Ask in our [Gitter chatroom](https://gitter.im/datawire/forge) or [file an issue on GitHub](https://github.com/datawire/forge/issues/new).**
