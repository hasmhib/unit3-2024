# Quiz 042
<img width="1284" alt="Screenshot 2024-01-26 at 5 56 19 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/b8efaae0-fbcf-424d-b4f6-7ef962a861a6">

## Code

```py
## python file
from kivy.core.window import Window
from kivymd.app import MDApp
from kivymd.uix.screen import MDScreen

class MysteryPageA(MDScreen):
    def change_to_page_two(self):
        print("Changing to page B")
        self.parent.current = "MysteryPageB"

class MysteryPageB(MDScreen):
    pass
class quiz042(MDApp):
    def __init__(self, **kwargs):
        super().__init__(**kwargs)

    def build(self):
        pass

    def change_to_page_two(self):
        print("Changing to page A")
        self.parent.current = "MysteryPageA"

test = quiz042()
test.run()

## kivy file
ScreenManager:

    id: main_scr
    MysteryPageA:
        name: "MysteryPageA"

    MysteryPageB:
        name: "MysteryPageB"

<MysteryPageA>:
    MDLabel
        size_hint : .8, .8
        pos_hint: {"center_x":.5, "center_y":.8}
        text: "This is mystery page A you pressed the button"
        orientation: 'vertical'
        color: "black"


    MDRaisedButton:
        pos_hint: {"center_x":.5, "center_y":.5}
        text: "Go to mystery page B"
        on_press:
            root.parent.current = "MysteryPageB"

<MysteryPageB>:
    MDLabel
        size_hint : .8, .8
        pos_hint: {"center_x":.5, "center_y":.8}
        text: "This is mystery page B you pressed the button"
        orientation: 'vertical'
        color: "black"

    MDRaisedButton:
        pos_hint: {"center_x":.5, "center_y":.5}
        text: "Go to mystery page A"
        on_press:
            root.parent.current = "MysteryPageA"
```

## Proof of work
https://github.com/hasmhib/unit3-2024/assets/142870448/d91e4a4b-d061-46eb-9584-6b8053d6588f


## UML Diagram
