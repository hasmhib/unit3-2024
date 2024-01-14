```.py
class paint:
    #init initialization
    #To keep data and functions together and save in capsels

    def __init__(t, mat:str, price:int, cst:int):
        t.material = mat
        t.price = price
        t.cost = cst
        t.color = [255,255,255]
        # t.dimension = dim
        # t.weight = weight
        # t.serial_number = serial
        # t.capacity = cap
        print(f"Creating a paint with material {t.material}")

    def get_profit(t)->int:
        return t.price - t.cost

    def get_color(t):
        return t.color

    def paint(t, new_color:list):
        if len(new_color) == 3 and min(new_color) > -1 and max(new_color) > 256:
            t.color = new_color

        else:
            print("New color is invalid")

paint1 = paint(mat = "plastic", price = 100, cst = 80)
paint2 = paint(mat = "pigment", price = 500, cst = 480)
print(paint1.get_profit())
print(paint2.get_profit())
paint1.paint([125,0,0])
print(f"The color of the paint1 is {paint1.color}")
print(f"The color of the paint1 is {paint1.get_color()}")
```
