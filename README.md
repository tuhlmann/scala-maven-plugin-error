Exhibits a problem with compiling a project with scala-maven-plugin 4.2.4 on Windows.

Tested with Oracle jdk 8

Change scala-maven-plugin version to 4.2.0 or 3.3.2 and it will compile fine.

This sample project was created via `mvn archetype:generate` from `net.alchim31.maven:scala-archetype-simple` version `1.7`.
I only changed the version number of the scala-maven-plugin to `4.2.4`

Here's the full error that's occuring:

```
D:\entw\aktuell\conteneo\scala-maven-plugin-error>mvn compile
[INFO] Scanning for projects...
[INFO]
[INFO] ------------------------< example-proj:example >------------------------
[INFO] Building example 1.0-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
[INFO]
[INFO] --- maven-resources-plugin:2.6:resources (default-resources) @ example ---
[INFO] Using 'UTF-8' encoding to copy filtered resources.
[INFO] skip non existing resourceDirectory D:\entw\aktuell\conteneo\scala-maven-plugin-error\src\main\resources
[INFO]
[INFO] --- maven-compiler-plugin:3.1:compile (default-compile) @ example ---
[INFO] Nothing to compile - all classes are up to date
[INFO]
[INFO] --- scala-maven-plugin:4.2.4:compile (default) @ example ---
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  1.021 s
[INFO] Finished at: 2019-10-27T12:24:24+01:00
[INFO] ------------------------------------------------------------------------
[ERROR] Failed to execute goal net.alchim31.maven:scala-maven-plugin:4.2.4:compile (default) on project example: Execution default of goal net.alchim31.maven:scala-maven-plugin:4.2.4:compile failed: An API incompatibility was encountered while executing net.alchim31.maven:scala-maven-plugin:4.2.4:compile: java.lang.ExceptionInInitializerError: null
[ERROR] -----------------------------------------------------
[ERROR] realm =    plugin>net.alchim31.maven:scala-maven-plugin:4.2.4
[ERROR] strategy = org.codehaus.plexus.classworlds.strategy.SelfFirstStrategy
[ERROR] urls[0] = file:/C:/Users/tuhlmann/.m2/repository/net/alchim31/maven/scala-maven-plugin/4.2.4/scala-maven-plugin-4.2.4.jar
[ERROR] urls[1] = file:/C:/Users/tuhlmann/.m2/repository/org/apache/maven/maven-builder-support/3.3.9/maven-builder-support-3.3.9.jar
[ERROR] urls[2] = file:/C:/Users/tuhlmann/.m2/repository/com/google/guava/guava/18.0/guava-18.0.jar
[ERROR] urls[3] = file:/C:/Users/tuhlmann/.m2/repository/org/codehaus/plexus/plexus-interpolation/1.21/plexus-interpolation-1.21.jar
[ERROR] urls[4] = file:/C:/Users/tuhlmann/.m2/repository/javax/enterprise/cdi-api/1.0/cdi-api-1.0.jar
[ERROR] urls[5] = file:/C:/Users/tuhlmann/.m2/repository/org/eclipse/sisu/org.eclipse.sisu.inject/0.3.2/org.eclipse.sisu.inject-0.3.2.jar
[ERROR] urls[6] = file:/C:/Users/tuhlmann/.m2/repository/org/codehaus/plexus/plexus-component-annotations/1.6/plexus-component-annotations-1.6.jar
[ERROR] urls[7] = file:/C:/Users/tuhlmann/.m2/repository/org/apache/maven/reporting/maven-reporting-api/3.0/maven-reporting-api-3.0.jar
[ERROR] urls[8] = file:/C:/Users/tuhlmann/.m2/repository/org/eclipse/aether/aether-util/1.0.2.v20150114/aether-util-1.0.2.v20150114.jar
[ERROR] urls[9] = file:/C:/Users/tuhlmann/.m2/repository/com/google/inject/guice/4.0/guice-4.0-no_aop.jar
[ERROR] urls[10] = file:/C:/Users/tuhlmann/.m2/repository/aopalliance/aopalliance/1.0/aopalliance-1.0.jar
[ERROR] urls[11] = file:/C:/Users/tuhlmann/.m2/repository/org/sonatype/plexus/plexus-sec-dispatcher/1.3/plexus-sec-dispatcher-1.3.jar
[ERROR] urls[12] = file:/C:/Users/tuhlmann/.m2/repository/org/sonatype/plexus/plexus-cipher/1.4/plexus-cipher-1.4.jar
[ERROR] urls[13] = file:/C:/Users/tuhlmann/.m2/repository/org/apache/commons/commons-lang3/3.4/commons-lang3-3.4.jar
[ERROR] urls[14] = file:/C:/Users/tuhlmann/.m2/repository/org/apache/maven/shared/maven-dependency-tree/3.0.1/maven-dependency-tree-3.0.1.jar
[ERROR] urls[15] = file:/C:/Users/tuhlmann/.m2/repository/org/apache/commons/commons-exec/1.3/commons-exec-1.3.jar
[ERROR] urls[16] = file:/C:/Users/tuhlmann/.m2/repository/org/codehaus/plexus/plexus-utils/3.3.0/plexus-utils-3.3.0.jar
[ERROR] urls[17] = file:/C:/Users/tuhlmann/.m2/repository/org/codehaus/plexus/plexus-archiver/4.1.0/plexus-archiver-4.1.0.jar
[ERROR] urls[18] = file:/C:/Users/tuhlmann/.m2/repository/org/codehaus/plexus/plexus-io/3.1.1/plexus-io-3.1.1.jar
[ERROR] urls[19] = file:/C:/Users/tuhlmann/.m2/repository/org/apache/commons/commons-compress/1.18/commons-compress-1.18.jar
[ERROR] urls[20] = file:/C:/Users/tuhlmann/.m2/repository/org/iq80/snappy/snappy/0.4/snappy-0.4.jar
[ERROR] urls[21] = file:/C:/Users/tuhlmann/.m2/repository/org/tukaani/xz/1.8/xz-1.8.jar
[ERROR] urls[22] = file:/C:/Users/tuhlmann/.m2/repository/backport-util-concurrent/backport-util-concurrent/3.1/backport-util-concurrent-3.1.jar
[ERROR] urls[23] = file:/C:/Users/tuhlmann/.m2/repository/junit/junit/3.8.1/junit-3.8.1.jar
[ERROR] urls[24] = file:/C:/Users/tuhlmann/.m2/repository/org/apache/maven/maven-archiver/3.4.0/maven-archiver-3.4.0.jar
[ERROR] urls[25] = file:/C:/Users/tuhlmann/.m2/repository/org/apache/maven/shared/maven-shared-utils/3.2.1/maven-shared-utils-3.2.1.jar
[ERROR] urls[26] = file:/C:/Users/tuhlmann/.m2/repository/commons-io/commons-io/2.5/commons-io-2.5.jar
[ERROR] urls[27] = file:/C:/Users/tuhlmann/.m2/repository/org/apache/maven/doxia/doxia-sink-api/1.9/doxia-sink-api-1.9.jar
[ERROR] urls[28] = file:/C:/Users/tuhlmann/.m2/repository/org/apache/maven/doxia/doxia-logging-api/1.9/doxia-logging-api-1.9.jar
[ERROR] urls[29] = file:/C:/Users/tuhlmann/.m2/repository/org/apache/maven/shared/maven-invoker/3.0.1/maven-invoker-3.0.1.jar
[ERROR] urls[30] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-sbt/zinc_2.12/1.3.1/zinc_2.12-1.3.1.jar
[ERROR] urls[31] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-lang/scala-library/2.12.8/scala-library-2.12.8.jar
[ERROR] urls[32] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-sbt/zinc-core_2.12/1.3.1/zinc-core_2.12-1.3.1.jar
[ERROR] urls[33] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-sbt/zinc-apiinfo_2.12/1.3.1/zinc-apiinfo_2.12-1.3.1.jar
[ERROR] urls[34] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-sbt/compiler-bridge_2.12/1.3.1/compiler-bridge_2.12-1.3.1.jar
[ERROR] urls[35] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-sbt/zinc-classpath_2.12/1.3.1/zinc-classpath_2.12-1.3.1.jar
[ERROR] urls[36] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-lang/scala-compiler/2.12.8/scala-compiler-2.12.8.jar
[ERROR] urls[37] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-sbt/compiler-interface/1.3.1/compiler-interface-1.3.1.jar
[ERROR] urls[38] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-sbt/util-interface/1.3.0/util-interface-1.3.0.jar
[ERROR] urls[39] = file:/C:/Users/tuhlmann/.m2/repository/com/trueaccord/scalapb/scalapb-runtime_2.12/0.6.0/scalapb-runtime_2.12-0.6.0.jar
[ERROR] urls[40] = file:/C:/Users/tuhlmann/.m2/repository/com/trueaccord/lenses/lenses_2.12/0.4.12/lenses_2.12-0.4.12.jar
[ERROR] urls[41] = file:/C:/Users/tuhlmann/.m2/repository/com/lihaoyi/fastparse_2.12/0.4.2/fastparse_2.12-0.4.2.jar
[ERROR] urls[42] = file:/C:/Users/tuhlmann/.m2/repository/com/lihaoyi/fastparse-utils_2.12/0.4.2/fastparse-utils_2.12-0.4.2.jar
[ERROR] urls[43] = file:/C:/Users/tuhlmann/.m2/repository/com/lihaoyi/sourcecode_2.12/0.1.3/sourcecode_2.12-0.1.3.jar
[ERROR] urls[44] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-sbt/io_2.12/1.3.0/io_2.12-1.3.0.jar
[ERROR] urls[45] = file:/C:/Users/tuhlmann/.m2/repository/com/swoval/file-tree-views/2.1.3/file-tree-views-2.1.3.jar
[ERROR] urls[46] = file:/C:/Users/tuhlmann/.m2/repository/net/java/dev/jna/jna/4.5.0/jna-4.5.0.jar
[ERROR] urls[47] = file:/C:/Users/tuhlmann/.m2/repository/net/java/dev/jna/jna-platform/4.5.0/jna-platform-4.5.0.jar
[ERROR] urls[48] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-sbt/util-logging_2.12/1.3.0/util-logging_2.12-1.3.0.jar
[ERROR] urls[49] = file:/C:/Users/tuhlmann/.m2/repository/com/eed3si9n/sjson-new-core_2.12/0.8.3/sjson-new-core_2.12-0.8.3.jar
[ERROR] urls[50] = file:/C:/Users/tuhlmann/.m2/repository/jline/jline/2.14.6/jline-2.14.6.jar
[ERROR] urls[51] = file:/C:/Users/tuhlmann/.m2/repository/org/apache/logging/log4j/log4j-api/2.11.2/log4j-api-2.11.2.jar
[ERROR] urls[52] = file:/C:/Users/tuhlmann/.m2/repository/org/apache/logging/log4j/log4j-core/2.11.2/log4j-core-2.11.2.jar
[ERROR] urls[53] = file:/C:/Users/tuhlmann/.m2/repository/com/lmax/disruptor/3.4.2/disruptor-3.4.2.jar
[ERROR] urls[54] = file:/C:/Users/tuhlmann/.m2/repository/com/eed3si9n/sjson-new-scalajson_2.12/0.8.3/sjson-new-scalajson_2.12-0.8.3.jar
[ERROR] urls[55] = file:/C:/Users/tuhlmann/.m2/repository/com/eed3si9n/shaded-scalajson_2.12/1.0.0-M4/shaded-scalajson_2.12-1.0.0-M4.jar
[ERROR] urls[56] = file:/C:/Users/tuhlmann/.m2/repository/org/spire-math/jawn-parser_2.12/0.10.4/jawn-parser_2.12-0.10.4.jar
[ERROR] urls[57] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-lang/scala-reflect/2.12.8/scala-reflect-2.12.8.jar
[ERROR] urls[58] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-sbt/util-relation_2.12/1.3.0/util-relation_2.12-1.3.0.jar
[ERROR] urls[59] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-sbt/zinc-persist_2.12/1.3.1/zinc-persist_2.12-1.3.1.jar
[ERROR] urls[60] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-sbt/sbinary_2.12/0.5.0/sbinary_2.12-0.5.0.jar
[ERROR] urls[61] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-lang/modules/scala-xml_2.12/1.0.6/scala-xml_2.12-1.0.6.jar
[ERROR] urls[62] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-sbt/zinc-compile-core_2.12/1.3.1/zinc-compile-core_2.12-1.3.1.jar
[ERROR] urls[63] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-sbt/launcher-interface/1.0.0/launcher-interface-1.0.0.jar
[ERROR] urls[64] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-lang/modules/scala-parser-combinators_2.12/1.1.2/scala-parser-combinators_2.12-1.1.2.jar
[ERROR] urls[65] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-sbt/util-control_2.12/1.3.0/util-control_2.12-1.3.0.jar
[ERROR] urls[66] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-sbt/zinc-classfile_2.12/1.3.1/zinc-classfile_2.12-1.3.1.jar
[ERROR] urls[67] = file:/C:/Users/tuhlmann/.m2/repository/com/google/protobuf/protobuf-java/3.7.0/protobuf-java-3.7.0.jar
[ERROR] urls[68] = file:/C:/Users/tuhlmann/.m2/repository/org/scala-lang/modules/scala-java8-compat_2.12/0.9.0/scala-java8-compat_2.12-0.9.0.jar
[ERROR] Number of foreign imports: 1
[ERROR] import: Entry[import  from realm ClassRealm[maven.api, parent: null]]
[ERROR]
[ERROR] -----------------------------------------------------
[ERROR] : character to be escaped is missing
[ERROR] -> [Help 1]
[ERROR]
[ERROR] To see the full stack trace of the errors, re-run Maven with the -e switch.
[ERROR] Re-run Maven using the -X switch to enable full debug logging.
[ERROR]
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/PluginContainerException
```
