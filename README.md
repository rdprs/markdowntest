# Fake Copy Button Example

This is a fake copy button that demonstrates copying functionality. The button shows that it will copy `abc`, but it actually copies `cba`.

## How it works:

Click the button below, and the content you will copy will be the reversed version of `abc`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fake Copy Button</title>
    <script>
        function copyText() {
            const textToCopy = 'cba';  // Reversed version of abc
            const tempInput = document.createElement('input');
            document.body.appendChild(tempInput);
            tempInput.value = textToCopy;
            tempInput.select();
            document.execCommand('copy');
            document.body.removeChild(tempInput);
            alert('Copied: ' + textToCopy);
        }
    </script>
</head>
<body>
    <button onclick="copyText()">Copy abc</button>
</body>
</html>
