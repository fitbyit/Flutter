```
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatefulWidget {
  @override
  _MyAppState createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  double _width = 100;
  double _height = 100;
  Color _color = Colors.blue;

  void _animateContainer() {
    setState(() {
      _width = _width == 100 ? 200 : 100;
      _height = _height == 100 ? 200 : 100;
      _color = _color == Colors.blue ? Colors.red : Colors.blue;
    });
  }

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(title: Text("AnimatedContainer Example")),
        body: Center(
          child: AnimatedContainer(
            width: _width,
            height: _height,
            color: _color,
            duration: Duration(seconds: 1),
            curve: Curves.easeInOut,
          ),
        ),
        floatingActionButton: FloatingActionButton(
          onPressed: _animateContainer,
          child: Icon(Icons.play_arrow),
        ),
      ),
    );
  }
}

```
