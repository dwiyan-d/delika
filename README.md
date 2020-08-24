import 'package:flutter/material.dart';

void main() {
  runApp(
    MaterialApp(
      debugShowCheckedModeBanner: false,
      title: 'Kyy Mobile',
      home: new SettingAppbar(),
    ),
  );
}

class SettingAppbar extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        leading: Icon(Icons.reorder),
        title: new Text("Kyy App Mobile",),
        actions: <Widget>[
          IconButton(
            icon: Icon(Icons.home, color: Colors.blue),
            onPressed: () {},
          ),
          
          IconButton(
            icon: Icon(Icons.chat_bubble, color: Colors.blue),
            onPressed: () {},
          ),
          IconButton(
            icon: Icon(Icons.build, color: Colors.red),
            onPressed: () {},
          ),
        ],
      ),
      drawer: Drawer(
          child: ListView(
            padding: EdgeInsets.all(9.0),
            children: const <Widget>[
              DrawerHeader(
                decoration: BoxDecoration(
                  color: Colors.red,
                ),
                child: Text(
                  'Drawer Header',
                  style: TextStyle(
                    color: Colors.white,
                    fontSize: 24,
                  ),
                ),
              ),
              ListTile(
                leading: Icon(Icons.message),
                title: Text('hubungi saya'),
              ),
              ListTile(
                leading: Icon(Icons.account_circle),
                title: Text('data diri saya'),
              ),
              ListTile(
                leading: Icon(Icons.settings),
                title: Text('pengaturan'),
              ),
            ],
          ),
        ),
    );
    
  }
}
