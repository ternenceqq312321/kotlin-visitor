# Kotlin-Visitor Documentation 
Visitor can use this app to scan the QR code and start chatting.

## Installation Instructions
Add the following dependency to your build.gradle file:
```
android {
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }
}
        
dependencies {
    implementation fileTree(dir: 'libs', include: ['*.jar'])
    implementation"org.jetbrains.kotlin:kotlin-stdlib-jdk7:$kotlin_version"
    implementation 'androidx.appcompat:appcompat:1.1.0'
    implementation 'androidx.core:core-ktx:1.1.0'
    implementation 'androidx.constraintlayout:constraintlayout:1.1.3'
    testImplementation 'junit:junit:4.12'
    androidTestImplementation 'androidx.test.ext:junit:1.1.1'
    androidTestImplementation 'androidx.test.espresso:espresso-core:3.2.0'
    implementation 'com.kotlinvisitor:app:1.0.1'
}
```

Make sure minSDKVersion change to 21 in your build.gradle file:
```
 minSdkVersion 21
```

Add these lines to your project's build.gradle file:
```
allprojects {
    repositories {
        google()
        jcenter()
        maven {
            url 'https://jfrog.infinacle.com/artifactory/libs-release-local'
        }
    }
}
```

Add these line to your AndroidManifest.xml file: 
```
<activity android:name="io.chativo.visitor.MainActivity"/>
```
