# Fake Copy Button Example

This is a demonstration of a **fake copy button** that shows it will copy `abc`, but it actually copies `cba`.

## Instructions

Click the button below, and it will show that it copies `abc`, but instead, it will actually copy `cba`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fake Copy Button</title>
    <script>
        function copyText() {
            const textToCopy = 'cba';  // This is what actually gets copied (reversed 'abc')
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
    <!-- This is the fake copy button -->
    <button onclick="copyText()">Copy abc</button>
</body>
</html>
