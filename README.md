Exhibits a problem with compiling a project with scala-maven-plugin 4.2.4 on Windows.

Tested with Oracle jdk 8

Change scala-maven-plugin version to 4.2.0 or 3.3.2 and it will compile fine.

This sample project was created via `mvn archetype:generate` from `net.alchim31.maven:scala-archetype-simple` version `1.7`.
I only changed the version number of the scala-maven-plugin to `4.2.4`
