# Unit 3: PillowTrackPro: Smart Pillow Management
![61-YYD4UXCL _AC_UF1000,1000_QL80_](https://github.com/hasmhib/unit3-2024/assets/142870448/d41b9dcb-e7c8-4af6-866e-6fa6eced59a0)
A picture buuk "Bye-Bye Bad Dreams" by Erwin Beilhartz

# Criteria A: Planning

## Problem definition
My client is the owner of a local pillow shop, managing her business with the help of three employees. She is facing significant challenges due to her usage of paper-based systems for managing client orders and tracking materials, which has led to inefficiencies and errors. This has led to difficulties in matching client orders with the materials ordered, causing inefficiencies and financial losses. For example, she recently encountered a situation where a large order for custom pillows was incorrectly recorded due to a misinterpretation of the handwriting on the order form. Consequently, the shop is losing money, and the stress of these financial losses is affecting the owner's quality of sleep, despite the fact that her business is designed to improve sleep quality.


## Proposed Solution
Considering the client's requirements, an adequate solution will be creating a computer program with a GUI(Graphical User Interface) that can store data in a database. Even though Xcode is one of the most popular programming languages used for macOS, I proposed to use Python. Python is a cross-platform programming language whereas Xcode is specifically designed for developing apps on Apple's platforms. As for the GUI, KivyMD is chosen for its elegance and simplicity [^1]. This GUI framework uses is structured in an object-oriented format and makes development easy compared to other GUI frameworks such as PyQT5[ref]. For the window, 


## Success Criteria

### 1. User Access and Password Management:
The website keeps users separate with an encrypted login system and even if they forget their passwords, the users can change their passwords if they remember security questions. (Issue: _“I would like to have different users for my different workers. Furthermore, I am sure that I will eventually forget passwords and I will not be able to access this information.”_)

### 2. Financial Tracking Capability:
The application includes a financial tracking feature that accurately records and monitors the company's transactions such as expenses an income. (Issue: _“I suffer with an financial losses due to incorrectly recorded orders”_)

### 3. Resource Tracking for Production:
The application implements a resource tracking system within the app that specifically manages the materials used for making pillows. (Issue: _"I was not able to track the materials, and there are many times when resources were over-booked, and I had to buy materials again, losing profits."_) 

### 4. Comprehensive Order and Material Management:
The application provides detailed information about order and material management by using tables and graphs such as pie charts and bar graphs. (Issue: _“There are lots of inefficiencies in order and material management and I need to calculate these every time.”_)

### 5. Translation System:
The application provides both in Japanese and English for the international workers. (Issue: _“In my company there are many workers who don’t understand Japanese so I want the app to be both English and Japanese”_)

## Task Record



# Criteria B: Design:

## System Diagram
<img width="max" alt="Screenshot 2024-03-07 at 10 58 25 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/554b60a7-3413-43f9-9923-5ede3c4a79e3">

Fig1. _System Diagram of the PillowTrackPro_
This is the visual representation of the system and how they relates to one another. This displays the input: Keyboard and Trackpad/Mouse to the output: Display. This diagram also showcases versions of the programming language (Python and KivyMD), the computer version and deatail (Processor, version, memory, etc), the module and database (python file and kivy file). 


## Wireframe Diagram

Fig2. _Wireframe of the PillowTrackPro_


## UML Diagram

Fig3. _This is the UML diagram of the PillowTrackPro._


## ER Diagram
<img width="max" alt="Screenshot 2024-03-07 at 10 44 21 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/61841f22-6f98-43b0-8606-d1302c737dbe">

Fig4. _This is the ER diagram of the PillowTrackPro_
This is the ER Diagram for the database illustrating four tables: users, finances, customers and inventory. The "users" table has a integer primary key 'id' and attributes like 'email', 'username', and 'password'. The "finances" table has a integer primary key 'id' and attributes 'current_money'. Another table "customers" has a integer primary key 'customer_id' and attributes like 'customer_address' and 'total_price_of_order'. Last table "material" has a integer priary key 'id' and two attributes 'material_name' and 'quantity'.  



# Criteria C: Development



[^1]:https://stackshare.io/stackups/python-vs-xcode#:~:text=In%20summary%2C%20Python%20is%20a,complex%20syntax%20and%20limited%20compatibility. 
