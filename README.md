# Bazel cquery/aquery bug

Note that in this state, running the following command fails:

```
bazel cquery @bazel_skylib//...
```

If I remove lines 34-37 from the WORKSPACE file, note that running the above command still errors.

However, if I `touch .bazelignore`, it now succeeds(?!)

If I now undo the above modification to WORKSPACE, and remove/make empty the `.bazelignore` file, it also succeeds.
