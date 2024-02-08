# Python-QR-Code-Generator

## Code

```pyhton
pip install qrcode
```

1. Set/get the link for generating QR code
2. Make a QR code from the link
3. Save QR code as image file

[Link](https://1drv.ms/f/s!AlzwURrv0oH2hNdgjNdAghiayuF3DQ?e=KJQUXA)

```python
import qrcode

inputLink = "https://1drv.ms/f/s!AlzwURrv0oH2hNdgjNdAghiayuF3DQ?e=KJQUXA"
qr = qrcode.QRCode(version = 1, box_size = 10, border = 2)
qr.add_data(inputLink)
qr.make(fit = True)
img = qr.make_image(fill_color = "black", back_color = "white")

img.save("TkinterPolice.png")
print("Done")
```

```pyhton
import qrcode

inputLink = input("Enter link: ")
qr = qrcode.QRCode(version = 1, box_size = 10, border = 2)
qr.add_data(inputLink)
qr.make(fit = True)
img = qr.make_image(fill_color = "black", back_color = "white")
img.save("QR.png")

print("Done!")
```
