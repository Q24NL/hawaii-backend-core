# Hawaii Backend Core

## Create a release
1. Make sure all tests pass.
2. Edit `pom.xml` and increase the version.
3. Commit and tag the changes, do not push:
```shell
export VERSION=" ... "
git commit -m "Release ${VERSION}."
git tag -a ${VERSION} -m "Release ${VERSION}."
unset VERSION
```
4. Update the `pom.xml`, set the version to the next development (`-SNAPSHOT`) version.
5. Commit and push:
```shell
git add .
git commit -m "Development version."
git push --tags
git push 
```
