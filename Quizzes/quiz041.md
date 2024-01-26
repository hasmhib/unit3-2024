# Quiz 041
<img width="max" alt="Screenshot 2024-01-26 at 5 52 46 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/fcdf9e71-8daf-46f9-866d-61304a185111">

## Code

```py
## python file
from kivymd.app import MDApp

class quiz041(MDApp):
    def build(self):
        self.count = 0
        pass

    def button_pressed(self, btn):
        the_tern = self.root.ids.tern
        the_tern.text = "It is X's turn"
        btn.md_bg_color = [1, 0, 0, 1]
        self.count += 1

        if self.count % 2 == 0:
            the_tern = self.root.ids.tern
            the_tern.text = "It is Y's turn"
            btn.md_bg_color = [1, 1, 0, 1]
            btn.text = "*"
            btn.font_size = "36pt"

        else:
            the_tern = self.root.ids.tern
            the_tern.text = "It is X's turn"
            btn.md_bg_color = [1, 0, 0, 1]
            btn.text = "#"
            btn.font_size = "36pt"

test = quiz041()
test.run()

## kivy file
Screen:
    size: 600, 500

    MDBoxLayout:
        orientation: "vertical"

        MDBoxLayout:
            orientation: "horizontal"
            size_hint_y: .166
            md_bg_color: "white"

            MDLabel:
                text: "Tic Tac Toe by Yosuke"
                halign: "center"
                font_size: "26pt"
                color: "black"

        MDBoxLayout:
            orientation: "horizontal"
            size_hint_y: .166
            md_bg_color: "white"
            MDLabel:
                id: tern
                text: "It is Y's turn"
                halign: "center"
                font_size: "14pt"
                color: "black"

        MDBoxLayout: # 3rd row
            orientation: "horizontal"
            size_hint_y: .166
            md_bg_color: "white"
            MDLabel:
                md_bg_color: "white"

            MDFlatButton:
                size_hint_x: 1
                size_hint_y: 1
                md_bg_color: "green"

                on_press:
                    app.button_pressed(self)

            MDFlatButton:
                size_hint_x: 1
                size_hint_y: 1
                md_bg_color: "green"

                on_press:
                    app.button_pressed(self)

            MDFlatButton:
                size_hint_x: 1
                size_hint_y: 1
                md_bg_color: "green"

                on_press:
                    app.button_pressed(self)

            MDLabel:
                md_bg_color: "white"

        MDBoxLayout: # 4th row
            orientation: "horizontal"
            size_hint_y: .166
            md_bg_color: "white"

            MDLabel:
                md_bg_color: "white"
            MDFlatButton:
                size_hint_x: 1
                size_hint_y: 1
                md_bg_color: "green"

                on_press:
                    app.button_pressed(self)

            MDFlatButton:
                size_hint_x: 1
                size_hint_y: 1
                md_bg_color: "green"

                on_press:
                    app.button_pressed(self)

            MDFlatButton:
                size_hint_x: 1
                size_hint_y: 1
                md_bg_color: "green"

                on_press:
                    app.button_pressed(self)

            MDLabel:
                md_bg_color: "white"

        MDBoxLayout: # 5th row
            orientation: "horizontal"
            size_hint_y: .166
            md_bg_color: "white"

            MDLabel:
                md_bg_color: "white"
            MDFlatButton:
                size_hint_x: 1
                size_hint_y: 1
                md_bg_color: "green"

                on_press:
                    app.button_pressed(self)

            MDFlatButton:
                size_hint_x: 1
                size_hint_y: 1
                md_bg_color: "green"

                on_press:
                    app.button_pressed(self)

            MDFlatButton:
                size_hint_x: 1
                size_hint_y: 1
                md_bg_color: "green"

                on_press:
                    app.button_pressed(self)

            MDLabel:
                md_bg_color: "white"

        MDBoxLayout:
            orientation: "horizontal"
            size_hint_y: .166
            md_bg_color: "white"


```

## Proof of work
https://github.com/hasmhib/unit3-2024/assets/142870448/f8795a9b-6757-4763-b65c-546c624089f8



## UML Diagram
![image](https://github.com/hasmhib/unit3-2024/assets/142870448/ad410b95-5c6f-4879-9db0-3dcfdb197d77)

