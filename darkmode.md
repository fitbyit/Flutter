```
import 'package:flutter/material.dart';

void main() {
  runApp(MyThemeApp());
}

class MyThemeApp extends StatefulWidget {
  @override
  _MyThemeAppState createState() => _MyThemeAppState();
}

class _MyThemeAppState extends State<MyThemeApp> {
  bool _isDark = false;

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: ThemeData.light(),
      darkTheme: ThemeData.dark(),
      themeMode: _isDark ? ThemeMode.dark : ThemeMode.light,
      home: Scaffold(
        appBar: AppBar(
          title: Text("Theme Switch Example"),
        ),
        body: Center(
          child: Row(
            mainAxisAlignment: MainAxisAlignment.center,
            children: [
              Icon(Icons.light_mode),
              Switch(
                value: _isDark,
                onChanged: (value) {
                  setState(() {
                    _isDark = value;
                  });
                },
              ),
              Icon(Icons.dark_mode),
            ],
          ),
        ),
      ),
    );
  }
}

```
