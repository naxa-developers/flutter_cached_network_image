# Cached network image
<<<<<<< HEAD
> A fork of Cached network image with support for SVGs
Refer to https://github.com/Baseflow/flutter_cached_network_image for more usage instruction 
## Warning: This library isn't well tested, create an issue if something breaks for you.

## Installation 
```
  cached_network_image:
    git:
      url: git@github.com:naxa-developers/flutter_cached_network_image.git
      ref: develop
```
=======
[![pub package](https://img.shields.io/pub/v/cached_network_image.svg)](https://pub.dartlang.org/packages/cached_network_image)
<!--[![Build Status](https://app.bitrise.io/app/4e1f9622c1f3458e/status.svg?token=sgBpcZPCUQwW37Z9J494HA&branch=master)](https://app.bitrise.io/app/4e1f9622c1f3458e)-->

A flutter library to show images from the internet and keep them in the cache directory.
>>>>>>> 7cd663ef5ad95e2da8e296f591757acad289b44a

## How to use
The CachedNetworkImage can be used directly or through the ImageProvider.
Both the CachedNetworkImage as CachedNetworkImageProvider have minimal support for web. It currently doesn't include caching.

With a placeholder:
```dart
CachedNetworkImage(
<<<<<<< HEAD
	imageUrl:'https://www.svgrepo.com/download/48239/user-online.svg',
    placeholder: (context, url) => const CircularProgressIndicator(),
    errorWidget: (context, url, error) => const Icon(Icons.error),
    fadeOutDuration: const Duration(seconds: 1),
    fadeInDuration: const Duration(seconds: 3),
    width: 24.0,
    height: 24.0,
    fit: BoxFit.contain,
    color: Colors.red,
=======
        imageUrl: "http://via.placeholder.com/350x150",
        placeholder: (context, url) => CircularProgressIndicator(),
        errorWidget: (context, url, error) => Icon(Icons.error),
     ),
 ```
 
 Or with a progress indicator:
 ```dart
CachedNetworkImage(
        imageUrl: "http://via.placeholder.com/350x150",
        progressIndicatorBuilder: (context, url, downloadProgress) => 
                CircularProgressIndicator(value: downloadProgress.progress),
        errorWidget: (context, url, error) => Icon(Icons.error),
     ),
 ```


````dart
Image(image: CachedNetworkImageProvider(url))
````

When you want to have both the placeholder functionality and want to get the imageprovider to use in another widget you can provide an imageBuilder:
```dart
CachedNetworkImage(
  imageUrl: "http://via.placeholder.com/200x150",
  imageBuilder: (context, imageProvider) => Container(
    decoration: BoxDecoration(
      image: DecorationImage(
          image: imageProvider,
          fit: BoxFit.cover,
          colorFilter:
              ColorFilter.mode(Colors.red, BlendMode.colorBurn)),
    ),
  ),
  placeholder: (context, url) => CircularProgressIndicator(),
  errorWidget: (context, url, error) => Icon(Icons.error),
>>>>>>> 7cd663ef5ad95e2da8e296f591757acad289b44a
),
 ```

