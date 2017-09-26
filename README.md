# Java 'TimeAgo' multilanguage library 1.5.0

This is a Java port of the [jquery-timeago](https://github.com/rmm5t/jquery-timeago) plug-in.  Please visit the [jquery-timeago](http://rmm5t.github.com/jquery-timeago/) project page to read more about fuzzy timestamps.

This library is forked from Kevin Sawicki's 'java-timeago' to support more than only one language. Feel free to fork it and add your own!

#### It supports English, Spanish, Italian, French and German at the time.

## Importing into your project
### Maven
* Add the repository
```xml
<repository>
	    <id>jitpack.io</id>
	    <url>https://jitpack.io</url>
</repository>
```
* Add the dependency
```xml
<dependency>
	    <groupId>com.github.pedroadame</groupId>
	    <artifactId>Java-TimeAgo-Multilanguage</artifactId>
	    <version>1.5.0</version>
</dependency>
```
### Gradle
1. Add this to your build file (your app's module build.gradle if you're integrating it in Android with Android Studio)
```
repositories {
	    maven {
	        url "https://jitpack.io"
	    }
}
dependencies {
	        compile 'com.github.pedroadame:java-timeAgo-multilanguage:1.5.0'
}
```

> If you're using Android Studio, the build.gradle file would be like this:
```
android {
    compileSdkVersion 22
    buildToolsVersion "21.1.2"
    defaultConfig {
        applicationId "com.example.app"
        minSdkVersion 15
        targetSdkVersion 22
        versionCode 1
        versionName "0.1"
    }
    buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
        }
    }
    productFlavors {
    }
}
repositories {
    maven {
        url "https://jitpack.io"
    }
    //Other repositories... p.e. mavenCentral()
}
dependencies {
    compile fileTree(include: ['*.jar'], dir: 'libs')
    compile 'com.github.pedroadame:java-timeAgo-multilanguage:1.5.0'
    //Other libraries...
}
```

## Usage

```java
TimeAgo time = new TimeAgo("en"); //For English text.
//TimeAgo time = new TimeAgo("it"); //For Italian text.
//TimeAgo time = new TimeAgo("es"); //For Spanish text.
//TimeAgo time = new TimeAgo("de"); //For German text.
//TimeAgo time = new TimeAgo("fr"); //For French text.


long current = System.currentTimeMillis();
String minutes = time.timeAgo(new Date(System.currentTimeMillis()));	// returns "15 minutes ago"
String hours = time.timeUntil(new Date(System.currentTimeMillis()));	// returns "6 hours from now"
```


## Contribution

1. Fork this project
2. Add your locale in the messages.properties file, following the pattern that I already have (I'll do the rest ;) )
3. Open a pull request to this project's "dev" branch.

## Other

[MIT License](http://www.opensource.org/licenses/mit-license.html)
