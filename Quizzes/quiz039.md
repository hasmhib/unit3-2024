# Quiz 039
<img width="max" alt="Screenshot 2024-01-26 at 5 04 31 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/ec3831d8-faf7-4a1a-9ea4-460be949cddb">

## Code

```py
## python file
from kivymd.app import MDApp

class quiz039(MDApp):
    def build(self):
        self.count = 0
        return

    def button_pressed(self):
        the_label = self.root.ids.yoshi
        self.count += 1
        the_label.text = f"Count {self.count}"


test = quiz039()
test.run()

## kivy file
BoxLayout:
    orientation: 'vertical'

    MDLabel:
        text: 'Your Name'
        halign: 'center'
        md_bg_color: 'white'
        font_size: "34pt"
        pos_hint: {'center_x': 5, 'center_y': 1}

    MDRaisedButton:
        ids: color
        text: "Your Name"
        md_bg_color: "black"

        on_release: app.button_pressed()
```

## Proof of work
https://github.com/hasmhib/unit3-2024/assets/142870448/24907804-898e-4f76-bdc5-d2c284c2c2fe

## UML Diagram
