Walkmod example for PMD and Gradle
========================================


If we run PMD, we have 3 errors acording a custom checkstyle configuration
at `src/main/resources/ruleset.xml` 

```
gradle check
```

But, if we build our project:

```
gradle walkmodPatch
```

Walkmod will create a `walkmod.patch` file in the root directory with our fixings.

Then, you can review it and, if you agree with those changes apply them
as follows:

```
git apply walkmod.patch
```

