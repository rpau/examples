Walkmod example for SonarQube and Gradle
========================================

First of all, you need to specify your `authToken` and `sonarHost` in
the `build.gradle` file.

Then run:

```
gradle walkmodPatch
```

Walkmod will create a `walkmod.patch` file in the root directory with our fixings.

Then, you can review it and, if you agree with those changes apply them
as follows:

```
git apply walkmod.patch
```

