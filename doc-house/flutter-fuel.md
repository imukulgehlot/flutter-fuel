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
Place following in project's Pubspec.yaml file
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



