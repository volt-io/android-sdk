# android-sdk

To use sdk library in your project:

1. add maven repository in `Settings.gradle` file

```kotlin
repositories {
        google()
        //...
        maven {
            url = uri("https://maven.pkg.github.com/volt-io/android-sdk")
            credentials {
                username = "$GITHUB_USERNAME"
                password = "$GITHUB_PERSONAL_TOKEN"
            }
        }
    }
```
* GITHUB_USERNAME - Github username whose personal token is used
* GITHUB_PERSONAL_TOKEN - [Personal Access Token (classic)](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens#creating-a-personal-access-token-classic)
  with `read:packages` scope

2. add dependency in module `build.gradle`

```kotlin
dependencies {
    //...
    implementation("io.volt:checkout-global-sdk:X.Y.Z")
}
```

Detailed documentation on how to use dependencies from github registry, can be found on [Working with Gradle registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-gradle-registry) page.
