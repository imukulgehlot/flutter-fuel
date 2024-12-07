
### #AppIcon #Icon #URL  
**Goal:** Get app icons formatted for all platforms.  
- [Icon Kitchen](https://icon.kitchen/i/H4sIAAAAAAAAA02OsQ6DMAxE%2F8VdGQpj1s6VKsFWdTCJEyISjJLQqkL8e5OwdLHOJ%2Fvu7fBGt1EEsYPCMA8TeQKh0UVqQJvhu%2BYVrEdD0MBobuw4ZOfSUqu7LnvaPFApu5iSkXgF0V0bCNZM6ZQjp8T%2B1I50dY%2Fyd8c4%2F3X1El2NAUlLolD7%2BgkrgbRBuoKQCqECkcJGOcWz2lzhfwIuKrBV%2BcZyzPNDI7yOH3SPR8%2FiAAAA)  

---

### #AppIcon #Icon #Pubspec #Yaml  
**Goal:** Set Flutter app icons for all platforms.  

Run this in the terminal:  
```bash
dart run flutter_launcher_icons
```
Place following in project's Pubspec.yaml file (Configure these & more specs as per the requirement)
```yaml
flutter_launcher_icons:
  ios: false
  android: true
  image_path: "assets/images/app_icon.png"
  remove_alpha_ios: true
  adaptive_icon_background: "#000000"
  adaptive_icon_foreground: "assets/images/app_icon.png"
  min_sdk_android: 21 # android min sdk min:16, default 21
```

---
### #UpgradeProject #AndroidProject #Project #CompileSDK #Build.Gradle #AGP #Kotlin #Version 
**Goal:** An script to automatically upgrade Android project to latest version. (Comes handy when time-traveling with legacy code)
- [Auto-Upgrade Andoid Project](https://gist.github.com/bizz84/605e2ca2088cb4acb7a076ca993f41cd)  

---

###  #LadyBug #AndroidStudio #Upgrade #Update #UpgradeProject #AndroidProject #Project #CompileSDK #Build.Gradle #AGP #Kotlin #Version #BuildFail
**Goal:** Multiple Snnipets to make your project run again after Android Studmajor 
- Open Android folder in Android Studio & Update to Gradle 8.9
- Upate this on settings.gradle:
```gradle
 id "com.android.application" version "8.3.2" apply false
```

- Add following code in subprojects section of project level build gradle:
```gradle
afterEvaluate { project ->
    if (project.hasProperty('android')) {
        project.android {
            if (namespace == null) {
                namespace project.group
            }
        }
    }
}
```



- In app level build grade:
```gradle
ndkVersion “25.1.8937393"
```
- Add following code in app level build gradle if notifications not working in compileSDK 35+:
In android->compile options:
```gradle
coreLibraryDesugaringEnabled true
```

And in dependencies section:
```
coreLibraryDesugaring 'com.android.tools:desugar_jdk_libs:2.1.2’
```



- [Deadly working snippet](https://github.com/flutter/flutter/issues/156304#issuecomment-2397707812)
- Upgrade possible pub packages

- मौज करो
---


