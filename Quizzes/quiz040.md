# Quiz 040
<img width="max" alt="Screenshot 2024-01-26 at 5 16 20 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/41552c0c-0b03-463a-9cb6-3eac4bfe36e5">

## Code

```py
## python file
from kivymd.app import MDApp

class quiz040(MDApp):
    def build(self):
        return

    def button_pressed(self):
        button_color = self.root.ids.text
        button_color.md_bg_color = "black"
        button_color.color = "white"

test = quiz040()
test.run()

## kivy file
Screen:
    size: 600,400

    MDLabel:
        id: text
        text: "Your Name"
        pos_hint: {"x_center":.5, "y_center":.5}
        font_size: "45pt"
        halign: "center"

    MDRaisedButton:
        id: button
        md_bg_color: "blue"
        size_hint: .1, .1
        font_size: "10pt"
        text: "Dark mode"
        on_press:
            app.button_pressed()

```

## Proof of work
https://github.com/hasmhib/unit3-2024/assets/142870448/74343372-1f9d-43b8-9d56-b6f2099c455e


## UML Diagram
![image](https://github.com/hasmhib/unit3-2024/assets/142870448/7a250947-85be-487d-8937-8983e7eb36ae)

