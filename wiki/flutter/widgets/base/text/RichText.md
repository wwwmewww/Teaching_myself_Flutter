# RichText 富文本

    ```dart
    RichText(
      style: DefaultTextStyle.of(context).style,
      text: TextSpan(children: [
        TextSpan(text: "It's "),
        TextSpan(text: "all", style: myBoldStyle),
        TextSpan(text: " widgets"),
      ]),
    )
    ```
