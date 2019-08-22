# slide_popup_dialog

Popup dialog with slide mechanism.

![Gif Example](https://raw.githubusercontent.com/dhimasdewanto/slide_popup_dialog/master/readme_screenshot/example.gif)

## Code Example

```
class MyHomePage extends StatefulWidget {
  final String title;

  const MyHomePage({Key key, this.title}) : super(key: key);

  @override
  _MyHomePageState createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text(widget.title),
      ),
      body: Center(
        child: RaisedButton(
          child: Text("Press to open dialog"),
          onPressed: _showDialog,
        ),
      ),
    );
  }

  void _showDialog() {
    slide_popup.showSlideDialog(
      context: context,
      child: Text("Hello World"),
      barrierColor: Colors.white.withOpacity(0.7),
      pillColor: Colors.red,
      backgroundColor: Colors.yellow,
    );
  }
}
```
