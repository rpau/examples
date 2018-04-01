Walkmod example for Maven
========================================

Running walkmod from this command:

```
mvn package
```

Walkmod will create a `walkmod.patch` file in the root directory with our fixings.
The fixings to apply are described in the walkmod.xml file.

However, if for any reason, you want to skip Walkmod, you can simply add `-DskipWalkmod`
into your `mvn package`.

Then, you can review it and, if you agree with those changes apply them
as follows:

```
git apply walkmod.patch
```
