# gradle-sample

A sample Gradle project.

## Setup

The Gradle distribution is hosted on a private server that requires authentication. Credentials are passed via `GRADLE_OPTS` so they stay out of `gradle-wrapper.properties`.

### direnv (recommended)

1. Install [direnv](https://direnv.net/) if you haven't already.
2. Create a `.envrc` in the project root:

   ```sh
   export GRADLE_OPTS="-Dgradle.wrapperUser=jamie -Dgradle.wrapperPassword=gradle"
   ```

3. Allow it:

   ```sh
   direnv allow
   ```

Now any `./gradlew` command will automatically pick up the credentials.

### Manual

Export the variable before running Gradle:

```sh
export GRADLE_OPTS="-Dgradle.wrapperUser=jamie -Dgradle.wrapperPassword=gradle"
./gradlew build
```
