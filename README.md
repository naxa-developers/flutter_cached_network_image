# Cached network image
Widget now uses builders for the placeholder and error widget and uses sqflite for cache management. See the [docs](https://pub.dartlang.org/documentation/cached_network_image/latest/cached_network_image/cached_network_image-library.html) for more information.

> A fork of Cached network image with support for SVGs


## How to use
The CachedNetworkImage can be used directly or through the ImageProvider.

```dart
              CachedNetworkImage(
                imageUrl:
                    'https://www.svgrepo.com/download/48239/user-online.svg',
                placeholder: (context, url) =>
                    const CircularProgressIndicator(),
                errorWidget: (context, url, error) => const Icon(Icons.error),
                fadeOutDuration: const Duration(seconds: 1),
                fadeInDuration: const Duration(seconds: 3),
                width: 24.0,
                height: 24.0,
                fit: BoxFit.contain,
                color: Colors.red,
            ),
 ```

> Refer to https://github.com/Baseflow/flutter_cached_network_image for more usage instruction 
