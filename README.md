# Fast ViewPager Library

## Add Dependencies

1. Add it in your root **build.gradle** at the end of repositories:
```gradle
repositories {
 ...
  maven { url 'https://jitpack.io' }
}
```
2. on module app **build.gradle** 
```gradle
implementation 'com.github.alfianyusufabdullah:spager:1.0.0'
```

## How To Use

first add this code on your layout

```xml
<com.alfianyusufabdullah.spager.widget.sViewPager
   android:id="@+id/mainPage"
   android:layout_width="match_parent"
   android:layout_height="match_parent" />
```
and add this on your Activity/Fragment
```java
oncreate(){

 sViewPager viewPager = findViewById(...);
 viewPager.initFragmentManager(getSupportFragmentManager());
 viewPager.addPages("One" , new PageOne());
 viewPager.addPages("Two" , new PageTwo());
 viewPager.addPages("Three" , new PageThree());
 viewPager.build();
 
}
```

if you wanna add tablayout just add this

```java
viewPager.addTabLayout(tabLayout);
```

and finally code like this 

```java
oncreate(){

 sViewPager viewPager = findViewById(...);
 viewPager.initFragmentManager(getSupportFragmentManager());
 viewPager.addPages("One" , new PageOne());
 viewPager.addPages("Two" , new PageTwo());
 viewPager.addPages("Three" , new PageThree());
 viewPager.addTabLayout(tabLayout);
 viewPager.build();
 
}
```

## TODO
* Use AppCompat & Design Library
* Jangan lupa baca Bismillah

## Screenshoot
<img src="https://github.com/alfianyusufabdullah/spager/raw/master/sample/screenshoot/ss1.png" width="250"> <img src="https://github.com/alfianyusufabdullah/spager/raw/master/sample/screenshoot/ss2.png" width="250"> <img src="https://github.com/alfianyusufabdullah/spager/raw/master/sample/screenshoot/ss3.png" width="250">

## License

    Copyright 2017 Alfian Yusuf Abdullah

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

     http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
