This issue peculiarly does not impact `./gradlew compileJava`, but does cause intellij to fail compilation using java-17.

Creating the following diff in [build.gradle](build.gradle) allows intellij to successfully build the project:

```diff
javaVersions {
-    libraryTarget = 17
+    libraryTarget = 11
}
```