# android-gradle-action

Run Android Gradle tasks with GitHub Actions.

## Note
This action may not be required to run Android builds.

Instead, you can simply try to execute the gradle wrapper in the GitHub action VM with :

```yaml
- name: Run tests
  run: ./gradlew test
```

## Example

```yaml
name: Android Gradle CI

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2

    - name: Run Gradle command
      uses: jojo243/android-gradle-action@2.0.0
      with:
        # The gradle command you wish to run (required)
        # Here, `./gradlew test` will be run
        script: test
```
