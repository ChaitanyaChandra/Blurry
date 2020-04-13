[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-Blurry-brightgreen.svg?style=flat)](https://android-arsenal.com/details/1/2192)
[![License](https://img.shields.io/badge/license-Apache%202-blue.svg)](https://www.apache.org/licenses/LICENSE-2.0)
[![Download](https://api.bintray.com/packages/wasabeef/maven/blurry/images/download.svg)](https://bintray.com/wasabeef/maven/blurry/_latestVersion)

`Blurry` is an easy blur library for `Android`.

![logo](art/blurry.png)

Screenshot
---

![Demo](art/blurry.gif)

How do I use it?
---

### Setup

##### Dependencies
```groovy
dependencies {
    compile 'jp.wasabeef:blurry:3.x.x'
}
```

### Functions

**Overlay**

Parent must be ViewGroup

```kotlin
Blurry.with(context).radius(25).sampling(2).onto(rootView)
```

**Into**  
```kotlin
// from View
Blurry.with(context).capture(view).into(imageView)
```

```kotlin
// from Bitmap 
Blurry.with(context).from(bitmap).into(imageView)
```

**Blur Options**

- Radius
- Down Sampling
- Color Filter
- Asynchronous Support
- Animation (Overlay Only)

```java
Blurry.with(context)
  .radius(10)
  .sampling(8)
  .color(Color.argb(66, 255, 255, 0))
  .async()
  .animate(500)
  .onto(rootView);
```

Requirements
--------------
Android 3.+ (API 14)
