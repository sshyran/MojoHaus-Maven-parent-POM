<!---
 Licensed to the Apache Software Foundation (ASF) under one or more
 contributor license agreements.  See the NOTICE file distributed with
 this work for additional information regarding copyright ownership.
 The ASF licenses this file to You under the Apache License, Version 2.0
 (the "License"); you may not use this file except in compliance with
 the License.  You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

 Unless required by applicable law or agreed to in writing, software
 distributed under the License is distributed on an "AS IS" BASIS,
 WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 See the License for the specific language governing permissions and
 limitations under the License.
-->
# MojoHaus Parent

This is the parent pom for all [MojoHaus](https://www.mojohaus.org) Maven plugins and components.
 
[![Apache License, Version 2.0, January 2004](https://img.shields.io/github/license/apache/maven.svg?label=License)][license]
[![Maven Central](https://img.shields.io/maven-central/v/org.codehaus.mojo/mojo-parent.svg?label=Maven%20Central)](https://search.maven.org/search?q=g%3Aorg.codehaus.mojo+AND+a%3Amojo-parent)
[![JDKBuilds](https://github.com/mojohaus/mojo-parent/workflows/JDKBuilds/badge.svg)][jdkbuilds]
[![Main](https://github.com/mojohaus/mojo-parent/workflows/Main/badge.svg)][mainbuilds]
[![SitePublishing](https://github.com/mojohaus/mojo-parent/workflows/SitePublishing/badge.svg)][published-site]

## Releasing

* Make sure the milestone name is name like `artifactId-number`. In this case `artifactId` is `mojo-parent`
  and version is equalto the version of the pom without trailing `-SNAPSHOT`.
* Make sure `gpg-agent` is running.
* Execute `mvn -B release:prepare release:perform`

For publishing the site, do the following (for all kinds of project):

```
cd target/checkout
mvn verify site site:stage scm-publish:publish-scm
```

[license]: https://www.apache.org/licenses/LICENSE-2.0
[jdkbuilds]: https://github.com/mojohaus/mojo-parent/actions?query=workflow%3AJDKBuilds
[mainbuilds]: https://github.com/mojohaus/mojo-parent/actions?query=workflow%3AMain
[published-site]: https://www.mojohaus.org/mojo-parent/
