# Kotlin-Visitor Documentation 
Visitor can use this app to start chatting.

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

Add these lines to your project's build.gradle.
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

## Using the SDK
1. `ApiKey` -> Obtain the API key from the Widget Settings.
2. `Email` -> Enter your email.
3. `Environment` -> Enter the environment. Example: 'UAT' 
4. `IdReference` -> Enter your email here or a GUID. The value sets here must be unique.
5. `IdReferenceType` -> Enter the visitor type. Example: 'guest'
6. `Name` -> Enter your name.
7. `Language` -> Enter the language. Example: 'en-US' or 'zh-CN'

#### Enter the code below to open the chat application
```
infiniDesk.apiKey = Config.API_KEY
infiniDesk.email = Config.EMAIL
infiniDesk.env = Config.ENVIRONMENT
infiniDesk.idRef = Config.ID_REFERENCE
infiniDesk.idRefType = Config.ID_REFERENCE_TYPE
infiniDesk.name = Config.NAME
infiniDesk.lang = Config.LANGUAGE
val intent = InfiniHelpDesk.getInstance().startChat(infiniDesk, this)
startActivityForResult(intent,1)
```

#### Enter the code below for import purpose
```
package com.myapplication

import com.infinihelpdesk.utils.InfiniHelpDesk
import com.infinihelpdesk.utils.InfiniHelpDeskIntent
```
