# Parent POM for Maven / Tycho / Eclipse projects

Parent POM for Maven to be used when developing Eclipse plug-ins / applications
using Tycho. Plug-ins for [Bndtools](https://bndtools.org/index.html) are
provided as well in order to create OSGi libraries.

The artifact can be consumed inside your project Maven *pom.xml* like this:

```xml
<parent>
  <groupId>com.hahnentt.maven</groupId>
  <artifactId>parent-eclipse</artifactId>
  <version>{VERSION}</version>
  <relativePath />
</parent>
```

## Maven consumption configuration

To configure the local *./m2/settings.xml* to consume GitHub packages as a
working Apache Maven registry, follow the official
[GitHub documentation](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-apache-maven-registry)!

## Releasing a new version

To release a new version, remove the *-SNAPSHOT* from the Maven version. For
example *1.0.0-SNAPSHOT* will become *1.0.0*. Pushing the changes will result
in a build including the release. Use the following commit message:
> Release v1.0.0

After that create a new GitHub release from that specific commit with a new tag
and title *v1.0.0*!

After that increment the version and add the *-SNAPSHOT* to the Maven version.
For example *1.0.0* will become *1.1.0-SNAPSHOT*. Pushing the changes will
result including the bill of material. Use the following commit message:
> Prepare next release
