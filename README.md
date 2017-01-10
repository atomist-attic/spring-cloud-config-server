# Atomist 'spring-cloud-config-server'

[![Build Status](https://travis-ci.org/atomist-rugs/spring-cloud-config-server.svg?branch=master)](https://travis-ci.org/atomist-rugs/spring-cloud-config-server)
[![Slack Status](https://join.atomist.com/badge.svg)](https://join.atomist.com)

This [Rug](http://docs.atomist.com/) archive contains a generator for a [Spring Cloud Config Server][spring-cloud-config-server] project.  Take a look inside the
`.atomist` folder.

Atomist content is under the `.atomist` directory. You can compile, run and edit the Java project.

This readme will be replaced with a project readme upon project generation.

[spring-cloud-config-server]: https://cloud.spring.io/spring-cloud-config/

## Rugs

### NewGitBackedSpringCloudConfigServer

The NewGitBackedSpringCloudConfigServer Generator creates a new [Spring
Cloud Config Server][spring-cloud-config-server] project.

[spring-cloud-config-server]: https://cloud.spring.io/spring-cloud-config/

[<img src="http://images.atomist.com/button/create-project.png" width="267" alt="Create a project with Atomist"/>](https://api.atomist.com/v1/projects/generators/35c508f8-0127-480b-a91f-a1c3b00b6532)

#### Prerequisites

There are no prerequisites to running this generator.

#### Parameters

To run this generator you must supply the following parameters.

Name | Required | Default | Description
-----|----------|---------|------------
`project_name` | Yes | |  A valid GitHub repository name.  It must be 21 characters or less to avoid truncating name when the its Slack channel is created.
`artifact_id` | No | myartifact | Maven artifact ID, e.g., "fiddle-riddle".
`group_id` | No | mygroup |  Maven group ID, e.g., "com.pany.project".
`version` | No | 0.1.0-SNAPSHOT | [Semantic version][semver] of the project.
`description` | No | My new project | A brief description of the project.
`root_package` | No | com.myorg | The root package for the generated service class.
`git_repo_location` | No | https://github.com/atomist-rugs/sample-config-repo | a Git repository location for configuration to serve (i.e. https://github.com/atomist-rugs/sample-config-repo)"

[semver]: http://semver.org

#### Running

Run it as follows:

```
$ cd parent/directory
$ rug generate atomist-rugs:spring-cloud-config-server:NewGitBackedSpringCloudConfigServer \
    my-config-server \
    artifact_id=my-config-server \
    group_id=uk.co.lndn \
    version=0.1.0-SNAPSHOT \
    description="Spring Cloud Config Server for my environment" \
    root_package=uk.co.lndn.electronic \
    git_repo_location=https://github.com/atomist-rugs/sample-config-repo
```

Note the first parameter, the `project_name`, is different in that you
do not need to supply the name of the parameter, just the value.  This
is because the `project_name` parameter is required for all
generators.  This will create a directory named `my-config-server` and
populate it with a working [Spring Cloud Config Server][spring-cloud-config-server].  If you are happy
with the change, commit the changes.

[spring-cloud-config-server]: https://cloud.spring.io/spring-cloud-config/

```
$ cd my-config-server
$ git init
$ git add .
$ git commit -m 'Initial version generated by Atomist'
```

See the README in the generated project for further instructions.

## Support

General support questions should be discussed in the `#support`
channel on our community Slack team
at [atomist-community.slack.com][slack].

If you find a problem, please create an [issue][].

[issue]: https://github.com/atomist-rugs/spring-cloud-config-server/issues

## Development

You can build, test, and install the project locally with
the [Rug CLI][cli].

[cli]: https://github.com/atomist/rug-cli

```
$ rug test
$ rug install
```

To create a new release of the project, simply push a tag of the form
`M.N.P` where `M`, `N`, and `P` are integers that form the next
appropriate [semantic version][semver] for release.  For example:

[semver]: http://semver.org

```
$ git tag -a 1.2.3
```

The Travis CI build (see badge at the top of this page) will
automatically create a GitHub release using the tag name for the
release and the comment provided on the annotated tag as the contents
of the release notes.  It will also automatically upload the needed
artifacts.

---
Created by [Atomist][atomist].
Need Help?  [Join our Slack team][slack].

[atomist]: https://www.atomist.com/
[slack]: https://join.atomist.com/
