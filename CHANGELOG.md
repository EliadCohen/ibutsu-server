Version 2.2.2
=============

* Actually copy the source in the importers
* Fix the requestBody of the User endpoint in the OpenAPI spec

Version 2.2.1
=============

* Rename some methods to ensure unique operationIds
* Fix some issues in the import API
* Trim whitespace from filters (closes #342)
* Add the ability to add new projects
* add logging for lock

Version 2.2.0
=============

* Fix version number in About dialog
* Add support for a dark theme
* Update PatternFly

Version 2.1.4
=============

* Fix a bug with the dashboard
* Bump async from 2.6.3 to 2.6.4 in /frontend

Version 2.1.3
=============

* Check if the first argument passed to on_failure is a dict
* new endpoint filter for frontend
* fix AttributeError: 'NoneType' object has no attribute 'project'
* fix docker-compose command in README
* Update version number

Version 2.1.2
=============

* Re-release to try to fix previous release mess

Version 2.1.1
=============

* Allow user's name to be edited
* Various bug fixes and enhancements

Version 2.1.0
=============

* Add project management for administrators
* Ignore persistent data
* Update the Getting Started documentation
* Add data persistence to ibutsu-pod.sh script
* Bump minimist from 1.2.5 to 1.2.6 in /frontend
* Add basic user management
* Add a development Docker Compose file

Version 2.0.3
=============

* Add an ellipsis to the heatmap labels
* Move admin creation into environment variables
* fix ibutsu-pod script
* Allow to import tests cases without time attr

Version 2.0.2
=============

* Fall back to older id fields
* Prevent a possible null result id
* Prevent a possible null run id

Version 2.0.1
=============

* Clear projects and dashboards when logging out. Fixes #295
* fix metadata reading during test import
* Bump url-parse from 1.5.3 to 1.5.10 in /frontend
* Bump follow-redirects from 1.14.7 to 1.14.8 in /frontend
* newbie fixes
* Bump nanoid from 3.1.23 to 3.2.0 in /frontend
* Only filter on env if an env is not null
* Add some logging and a URL check (#284)
* Bump follow-redirects from 1.14.1 to 1.14.7 in /frontend
* Add JWT secret to template files

Version 2.0.0
=============

* Estimate count on test-history page
* Small improvements to the test history tab
* Hide username/password related components when user login is disabled (#279)
* Add test history tab to Result page (#276)
* Address some issues raised by static analysis (#278)
* Convert USER_LOGIN_ENABLED to bool if given as env var
* Get a user's primary e-mail on GitHub if they have no public e-mail address (#272)
* Add a way to disabled basic auth for non-superadmins
* Add get_user_list endpoint
* Fix keycloak login (#270)
* Update docker image names (#267)
* Show login progress feedback (#266)
* Add build_deploy script for App-SRE builds (#265)
* A single jUnit XML file is a single test run, refactor the importer to take this into account
* Some code refactoring after static analysis. (#245)
* Implement MetaFilter with separate field and value (#225)
* Adjustments for app-sre deployment (#256)
* Fix small FE bug on user profile page
* Add superadmin user after upgrading db
* Add a task for adding users/project owners
* Add superadmin to the ocp template files
* Add ability to create superadmin user on startup
* Allow logging in by hitting 'Enter'
* Require superadmin token for running admin task
* Update pods script to create an admin user, a project, standardise on echo, and make the output prettier. (#247)
* Some small fixes to ENV vars
* Split templates into one file for each
* Update @greatsumini/react-facebook-login
* Fix Jenkins Job View
* Allow superadmins to update projects
* Support adding users to projects
* Add project info to the profile page
* Filter runs/results on user projects, if none specified
* Bump url-parse from 1.5.1 to 1.5.3 in /frontend (#234)
* Bump tmpl from 1.0.4 to 1.0.5 in /frontend (#233)
* Bump tar from 6.1.0 to 6.1.11 in /frontend (#232)
* Add authentication and authorisation to Ibutsu
* Promote user property data to metadata
* Add babel core dependency
* Switch from 'babel-eslint' to '@babel/eslint-parser'
* Update and re-apply pre-commit (#216)
* Support adding artifacts to test runs (#215)

Version 1.13.4
==============

* Update default timeouts in OCP templates (#204)
* Fixed a spelling error (#212)
* Fix the archive import
* Set failed reports as failed in the DB
* Add support for run_id, hiding filter chips in FilterTable
* Fix bulk_update endpoint
* Add a checkbox select filter for exceptions
* Add docs reference for backend/settings.yaml
* Migrate to use the Furo theme in the docs. Looks much nicer and provides both a light and dark theme
* add support for import metadata (#194)
* Update OCP template config
* Update readme with badges

Version 1.13.3
==============

* Add a script to build a settings file at container runtime
* Small changes to dockerfiles
* Add a script to start ibutsu in a podman pod
* Sync aborted runs from the last 3 hrs
* Small bugs fixes
* Also fix possibility that duration is None is update_run task
* Handle 'None' results in the task controller
* Change the user when copying over the application
* Use Ubi8 images
* Build worker, schedule too
* Add a build image stage in tests.yaml
* remove travis.yml
* Change from travis to gh action

Version 1.13.2
==============

* Fix division by 0 in the jenkins heatmap
* Change 204 to 206
* Add an API endpoint to check the status of a task
* Small changes to OCP templates
* Update pre-commit; add in task for syncing aborted runs
* Update the Python dependencies (#169)

Version 1.13.1
==============

* Pin SqlAlchemy to 1.3.23 (#158)

Version 1.13.0
==============

* Fix bugs in the OpenAPI specification, and make sure to drop the 'data' attribute before sending it out (#153)
* Use 'id' rather than 'name'
* Use 'in' rather than dict.get()
* updated importer to work with older style junit xml
* Use the number of collected tests
* Add a note on how to generate the changelog (#148)
* Actually count when we are filtering on very small subset of rows
* oc create -f will just create the template, we need to process it
* Add cronjob/job for nightly vacuuming of database

Version 1.12.2
==============

* Add ocp templates for backup cronjob
* Add in tasks to prune old runs and results from the DB
* Also index requirements
* Fix filters on reports
* Add a upgrade function to add gin indexes on metadata.tags
* Added EmptyObject component for missing results/runs (#133)
* Validate UUID in OpenAPI spec and controllers
* Just use "ls" rather than "ls -ltr"

Version 1.12.1
==============

* Release 1.12.1
* Remember tab + updates (#115)
* Update API spec to allow null values in Runs (#118)
* Pass project along with file when importing via the UI (closes #110) (#116)
* Remove reference to MongoDB in docs
* Add a button for deleting a single widget from a dashboard
* Add some documentation about filters, fixup docs elsewhere
* Add a button to delete dashboards
* Add some default fields and specify whether it's required
* Add custom filters for some widgets
* Bring the CHANGELOG up to date (#103)
* Add a new option to the release script to update the changelog (#102)

Version 1.12.0
==============

* Create a UI to add dashboards and widgets (#100)
* Build the custom dashboards (#99)
* Build the dashboard API (#96)
* Create a way to upgrade databases on the fly (#95)

Version 1.11.4
==============

* Frontend updates to show the annotation in the heatmap
* Add endpoint to update multiple runs at a time
* Fix result tree page crash on junit imported run
* Add xfail/xpass to widget calculations
* Fix loading of result component
* Add `summary.tests` to the `numeric_fields`
* Allow filtering by JSON run summary fields
* Sort recent builds by `start_time` rather than `build_number` (#84)
* Fix bugs #78 and #79 (#83)

Version 1.11.3
==============

* Fix bugs #78 and #79 (#83)
* Fix issue #75 (#80)
* Fix task tests (#80)
* Updates to support xfail in Ibutsu
* Update file pruning for PSQL

Version 1.11.2
==============

* Fix an additional bug with the project selector

Version 1.11.1
==============

A new bug fix release in the 1.11.x series, this fixes the following bugs:

* Screenshots not showing up on the results page
* Project selector causes a blank screen when trying to change project
* Widget grouping by `metadata.component` instead of `component`

Version 1.11.0
==============

In order to overcome some performance and other issues, and due to MongoDB's license changes,
Ibutsu has now migrated to use PostgreSQL.

Version 1.10.2
==============

* Fix a small celery error `Cannot mix new and old setting keys`

Version 1.10.1
==============

* Fix styling of count skips on Jenkins Job Analysis page (#29)
* [Heatmap] Sort builds by `start_time`, not the string `build_number`
* [Heatmap] Use an aggregation to get the correct number of jobs that exist in the DB
* [Heatmap] Don't show columns in which all the plugins failed
* Add link to JIRA issues.redhat.com
* Convert failure classification table into its own component
* Expose the `count_skips` parameter in the UI (#24)
* Check to make sure `start_time` exists

Version 1.10.0
==============

* Add a switch to change from overall health from bar to area chart
* Show active filters and make exception name clickable in failure classification table
* Apply a limit to the amount of runs from which we create the JJV
* Make failure classification table expandable, to aid in debugging
* Add a tooltip to the generic area chart
* Fix warnings for links, limit reports to 1e5 documents
* Make links open in a new tab
* Add link to submit upstream issue, make links open in new tab
* Limit documents returned by reports to a reasonable number
* Add trademark and file retention policy to About modal
* Add a link to the docs on the about modal
* Limit the number of results we can display in the results table.
* Made run-list component and env pills clickable for filtering
* Update the rtd conf file location
* Fix the `master_doc` for Sphinx
* Make the docs requirements file match the config file
* Add readthedocs config
* Change Travis config to support both Python and JS
* Initial import from Gitlab

Version 1.9.0
=============

* Allow for displaying 70, 150 builds in the Overall Health and Build Duration
* Show tags if they are available in the metadata
* Add filters to the Jenkins Job page
* Use Linkify to create a link for the `skip_reason`
* Add a link to the jenkins build url on the Jenkins Job page

Version 1.8.1
=============

* Update the logo and background in the About modal
* Add in a task to delete files > 256 KiB
* Don't retry pruning task
* Tweak the UI to make things look better
* Change pruning to remove files older than 3 months
* Update to run only once, not every minute
* Add the line chart BE endpoint and FE widget

Version 1.8.0
=============

* Upgrade to the latest version of PatternFly4
* small fix so this text doesn't display when the widget is loading
* Some small fixes, add link to analysis page on dashboard
* Add a widget endpoint and FE View component for a Jenkins Analysis View
* Add in a chgrp and chmod for the image
* Fix Dockerfile for the celery beat scheduler
* Add artifact pruning as a periodic task
* Add in 'Dependency Outage' as a classification
* Add in a task to delete old artifact files
* Add 'Unknown' to classification dropdown
* Fix KeyError on prod
* Fix for non-null fields in Jenkins Job View

Version 1.7.4
=============

* "Classify failures" tab added to the Run page, allows for classification of multiple test failures at a time
* Added Jenkins Job BE endpoint for aggregating results of any Jenkins Job
* Tables refactored into a common `FilterTable` component
* Enabled classification dropdown for skipped results
* More visible description for `ParamDropdown` on widgets
* Added in dropdown for settings the number of builds in Vortex Heatmap
* Added in support for custom page components, added a Jenkins Job View

Version 1.7.3
=============

* Add a generic dropdown for changing widget params in the FE
* Add in a common component widgets can use as a header that includes a refresh
* Add KVP for source on run detail page
* Sort alphabetically in run aggregator widget
* Fix rounding in run aggregator
* Fix the URL for frontend version checking
* Fix the filters on the run page not being read from the URL
* Fix the ordering in `update_run` to use the new `start_time` column
* Improve the execution time of `_get_recent_run_data`

Version 1.7.2
=============

* Make failure classification available on error results as well as failed results
* Update all references of `starttime` to `start_time`
* Add a task for adding metadata.project to runs/results
* Create a task to add `start_time` to all results
* Expand the tree to the level of the python files by default
* Change heatmap links to go to the run page
* Use .get to avoid KeyError
* Add exception handling for older run IDs
* Add the DB task to celery
* Add a task to recreate runs from results
* Update the OpenAPI spec to follow what we're doing
* Add in some documentation about importing results
* Fixup the junit xml importer
* Adding a doc-requirements file for packages required to build the docs
* Use componentDidUpdate rather than the eventEmitter for widgets
* Make a start on the documentation
* Add the category dropdown for skips
* Add in the result-aggregator widget endpoint
* Fix for percentage colouring in results tree on run page

Version 1.7.1
=============

* Fix tree nodes that were incorrect when test params contain paths
* Fix a bug where the test result pane was not updated after clicking a new node
* Hide the search bar until it actually works
* Add a spinner when the tree is loading
* Start with a fresh tree when the tab is loaded again
* Write some tests around some of the above functions

Version 1.7.0
=============

* Expand the results tree page in the run view
* Add in a result aggregator endpoint (for future widget)
* Add project to widget queries
* UI tweaks

Version 1.6.0
=============

* Add a skip reason to the result details page
* Rearrange run summary page to allow for more details/metadata to be displayed in the future
* Move test tree and results into tabs on run details page
* Add project selector drop
* Implement support for project selector dropdown (i.e. automatic filtering based on project selected)

Version 1.5.1
=============

* Remove API for static widgets
* Add project lookups in all the relevant places
* Add in loading and dynamic chart height
* Fix the parameter error in the widgets

Version 1.5.0
=============

* Create new widget framework
* Create new Jenkins heatmap widget
* Create new result summary widget
* Create new run aggregator widget
* Remove the old static widgets from the dashboard
* Fix some issues with the FileUpload component
* Write some tests for the FileUpload component
* Write some other JavaScript tests
* Add filter by source on run list page
* Fix a small filtering bug

Version 1.4.4
=============

* Support partial archives in the importer.
* Support updated archives
* Fix a couple issues in displaying dates
* Add getOperationMode, add handling of 'exists' operator
* Make UI filter operations depend on the field that is selected

Version 1.4.3
=============

* Support multi select from dropdown menus when using "in" operation
* Add in `MultiValueInput` widget for "in" operation on results and run pages
* Add error handling to all tables
* Add empty states to all tables
* Add spinners to all tables
* Update the Docker setup
* Add in unix timestamp `start_time` to the run object
* Add filters to the run page
