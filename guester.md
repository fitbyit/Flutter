```
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: Text("GestureDetector Example")),
        body: Center(
          child: GestureDetector(
            onTap: () {
              print("Container tapped!");
            },
            child: Container(
              padding: EdgeInsets.all(20),
              color: Colors.blue,
              child: Text(
                "Tap Me",
                style: TextStyle(color: Colors.white, fontSize: 20),
              ),
            ),
          ),
        ),
      ),
    );
  }
}

```
