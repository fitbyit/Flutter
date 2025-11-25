Use the GridView widget to display a grid of images.

```
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'GridView with Rounded Images',
      home: ImageGridScreen(),
    );
  }
}

class ImageGridScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Rounded Asset Images Grid'),
      ),
      body: Padding(
        padding: const EdgeInsets.all(8.0),
        child: GridView.count(
          crossAxisCount: 2, // 2 columns
          crossAxisSpacing: 8.0,
          mainAxisSpacing: 8.0,
          children: [
            ClipRRect(
              borderRadius: BorderRadius.circular(16),
              child: Image.asset('assets/image1.jpg', fit: BoxFit.cover),
            ),
            ClipRRect(
              borderRadius: BorderRadius.circular(16),
              child: Image.asset('assets/image2.jpg', fit: BoxFit.cover),
            ),
            ClipRRect(
              borderRadius: BorderRadius.circular(16),
              child: Image.asset('assets/image3.jpg', fit: BoxFit.cover),
            ),
            ClipRRect(
              borderRadius: BorderRadius.circular(16),
              child: Image.asset('assets/image4.jpg', fit: BoxFit.cover),
            ),
            ClipRRect(
              borderRadius: BorderRadius.circular(16),
              child: Image.asset('assets/image5.jpg', fit: BoxFit.cover),
            ),
            ClipRRect(
              borderRadius: BorderRadius.circular(16),
              child: Image.asset('assets/image6.jpg', fit: BoxFit.cover),
            ),
          ],
        ),
      ),
    );
  }
}

```

```
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  final List<String> imageUrls = [
    "https://picsum.photos/200/300?random=1",
    "https://picsum.photos/200/300?random=2",
    "https://picsum.photos/200/300?random=3",
    "https://picsum.photos/200/300?random=4",
    "https://picsum.photos/200/300?random=5",
    "https://picsum.photos/200/300?random=6",
  ];

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: Text("GridView Example")),
        body: GridView.count(
          crossAxisCount: 2,       // 2 columns
          crossAxisSpacing: 8,
          mainAxisSpacing: 8,
          padding: EdgeInsets.all(10),
          children: imageUrls.map((url) {
            return ClipRRect(
              borderRadius: BorderRadius.circular(10),
              child: Image.network(
                url,
                fit: BoxFit.cover,
              ),
            );
          }).toList(),
        ),
      ),
    );
  }
}
```
