# Cached network image
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

## How to use
The CachedNetworkImage can be used directly or through the ImageProvider.

```dart
CachedNetworkImage(
	imageUrl:'https://www.svgrepo.com/download/48239/user-online.svg',
    placeholder: (context, url) => const CircularProgressIndicator(),
    errorWidget: (context, url, error) => const Icon(Icons.error),
    fadeOutDuration: const Duration(seconds: 1),
    fadeInDuration: const Duration(seconds: 3),
    width: 24.0,
    height: 24.0,
    fit: BoxFit.contain,
    color: Colors.red,
),
 ```

