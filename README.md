# Parent POM for Maven / Tycho / Eclipse projects

Parent POM for Maven to be used when developing Eclipse plug-ins / applications
using Tycho.

The artifact can be consumed inside your project Maven *pom.xml* like this:

```xml
<parent>
  <groupId>com.hahnentt.maven</groupId>
  <artifactId>parent-eclipse</artifactId>
  <version>{VERSION}</version>
  <relativePath />
</parent>
```

## Building / deploying a new version

To build this parent POM run the following command:

> mvn clean verify install

To deploy this parent POM to the GitHub Maven repository run the following
command. Make sure that the GitHub server is configured in your *settings.xml*:

> mvn clean verify deploy -Pdeploy

Don't deploy snapshot versions other than for testing. When deploying a new
version make sure always to remove the **-SNAPSHOT** from the version!

### *settings.xml* template

```xml
<servers>
  <server>
    <id>github</id>
    <username>thahnen</username>
    <password>{GITHUB_TOKEN}</password>
  </server>
</servers>```
