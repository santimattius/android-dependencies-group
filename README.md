# android-dependencies-group
Android dependencie definition

## Setup

Implemente remote dependencies script defined in this github repository:

``` groovy

buildscript {

    //apply script from android-dependencies-group repository.
    apply from: "https://raw.githubusercontent.com/santimattius/android-dependencies-group/main/versions.gradle"

    ....
}

```

## Use

``` groovy

dependencies {
    implementation fileTree(dir: 'libs', include: ['*.jar'])

    //Only version name
    implementation "org.jetbrains.kotlin:kotlin-stdlib-jdk7:$kotlin_version"

    //dependencies groups
    androidBasic()
    composeGroup()
    koin()
    accompanist()
    lifecycle()
    coil()
    coroutines()
    retrofit()
    room()
    testing()
    androidTests()

    implementation "androidx.multidex:multidex:$multidex_version"

}

```
