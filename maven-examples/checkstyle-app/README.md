Walkmod example for Checkstyle and Maven
========================================


If we run checkstyle, we have 2 errors acording a custom checkstyle configuration
at `src/main/resources/checkstyle.xml` 

```
mvn checkstyle:check
```

But, if we build our project:

```
mvn package
```

Walkmod will create a `walkmod.patch` file in the root directory with our fixings. 
However, if for any reason, you want to skip Walkmod, you can simply add `-DskipWalkmod` 
into your `mvn package`.

Then, you can review it and, if you agree with those changes apply them
as follows:

```
git apply walkmod.patch
```

