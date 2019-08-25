# slide_popup_dialog

Popup dialog with slide mechanism. Use it like AlertDialog or SimpleDialog.

![Gif Example](https://raw.githubusercontent.com/dhimasdewanto/slide_popup_dialog/master/readme_screenshot/example.gif)

## How to use

1. Add slide_popup_dialog to your package's pubspec.yaml, then intall it.

2. Import package.

```
import 'package:slide_popup_dialog/slide_popup_dialog.dart' as slideDialog;
```

3. Add this method to your State Widget.
```
void _showDialog() {
  slideDialog.showSlideDialog(
    context: context,
    child: Text("Hello World"),
  );
}
```

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
    slideDialog.showSlideDialog(
      context: context,
      child: Text("Hello World"),
      barrierColor: Colors.white.withOpacity(0.7),
      pillColor: Colors.red,
      backgroundColor: Colors.yellow,
    );
  }
}
```

![Gif Example](https://raw.githubusercontent.com/dhimasdewanto/slide_popup_dialog/master/readme_screenshot/more_example.gif)
