# Unit 3: PillowTrackPro: Smart Pillow Management
<img width="max" alt="Screenshot 2024-03-07 at 11 18 48 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/3f96cb05-999a-42ca-916e-fded01696dff">
DALL·E 2024-03-07 23.18.31 - Visualize a serene image of a pillow floating above the clouds under a starry night sky.

# Criteria A: Planning

## Problem definition
My client is the owner of a local pillow shop, managing her business with the help of three employees. She is facing significant challenges due to her usage of paper-based systems for managing client orders and tracking materials, which has led to inefficiencies and errors. This has led to difficulties in matching client orders with the materials ordered, causing inefficiencies and financial losses. For example, she recently encountered a situation where a large order for custom pillows was incorrectly recorded due to a misinterpretation of the handwriting on the order form. Consequently, the shop is losing money, and the stress of these financial losses is affecting the owner's quality of sleep, despite the fact that her business is designed to improve sleep quality.


## Proposed Solution
Considering the client's requirements, an adequate solution will be creating a computer program with a GUI(Graphical User Interface) that can store data in a database. Even though Xcode is one of the most popular programming languages used for macOS, I proposed to use Python. Python is a cross-platform programming language whereas Xcode is specifically designed for developing apps on Apple's platforms. As for the GUI, KivyMD is chosen for its elegance and simplicity [^1]. This GUI framework uses is structured in an object-oriented format and makes development easy compared to other GUI frameworks such as PyQT5[^2]. For the database, I have selected SQLite. SQLite is a free database that requires no additional server process and is implemented on a single file. It is designed to handle large amounts of data efficiently, making it suitable for storing all kinds of information related to the pillow company's informations [^3]. SQLite continuously updates its content, minimizing the risk of lost data in the event of a power failure or crash. Its cross-platform compatibility will enable future developers to expand the program to other platforms. In comparison to other databases available, SQLite is reliable, efficient, cost-friendly, and easy to use [^4].


## Success Criteria

### 1. User Access and Password Management:
The website keeps users separate with an encrypted login system and even if they forget their passwords, the users can change their passwords if they remember security questions. (Issue: _“I would like to have different users for my different workers. Furthermore, I am sure that I will eventually forget passwords and I will not be able to access this information.”_)

### 2. Financial Tracking Capability:
The application includes a financial tracking feature that accurately records and monitors the company's transactions such as expenses an income. (Issue: _“I suffer with an financial losses due to incorrectly recorded orders”_)

### 3. Resource Management for Production:
The application implements a resource management system within the app that specifically visualize the materials that are available for making pillows. (Issue: _"I was not able to track the materials, and there are many times when resources were over-booked, and I had to buy materials again, losing profits."_) 

### 4. Comprehensive Order and Material Management:
The application provides detailed information about order and material management by using tables and graphs such as pie charts and bar graphs. (Issue: _“There are lots of inefficiencies in order and material management and I need to calculate these every time.”_)

### 5. Order searching System:
The application allows the user to search for orders by materials. (Issue: _“I was not able to check who ordered what materials, it is difficult to check customer informations all the time.”_)



# Criteria B: Design:

## System Diagram
<img width="max" alt="Screenshot 2024-03-08 at 0 27 42 AM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/d9a3efec-87a8-4432-a03f-f8763e33dfc4">

Fig. 1: _System Diagram of the PillowTrackPro_

This is the visual representation of the system and how they relates to one another. This displays the input: Keyboard and Trackpad/Mouse to the output: Display. This diagram also showcases versions of the programming language (Python and KivyMD), the computer version and deatail (Processor, version, memory, etc), the module and database (python file and kivy file). 


## Wireframe Diagram
<img width="max" alt="image" src="https://github.com/hasmhib/unit3-2024/assets/142870448/073baca2-2040-4818-9ca4-32dc8bb85dd1">

Fig. 2: _Wireframe of the PillowTrackPro_

The wireframe diagram in Fig. 2 illustrates the proposed GUI interface and navigation flow of the application. It showcases the interconnectivity between different screens, with directional arrows directs from interactive buttons to indicate the users through the app. For example, the 'Login' screen allows users to either create an account by pressing 'Signin' button or or utilize the 'Forgot Password?' option, which leads the users to resetting their password. 

Once logged in, the 'Welcome' screen serves as a central hub, directing users to various sections of the application: 'Finances', 'Customers', 'Order', and 'Inventory'. These sections are designed for specific tasks within the app. For instance, the 'Finances Screen' will present options for visualizing financial data through pie charts and bar graphs, while the 'Order Screen' facilitates order placement and tracking. Additionally, the 'CustomerScreen' is used for managing customer information and orders, and the 'InventoryScreen' provides an overview and control of material stock levels.


## UML Diagram

Fig. 3: _This is the UML diagram of the PillowTrackPro._


## ER Diagram
<img width="max" alt="Screenshot 2024-03-07 at 11 53 30 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/d5e3429d-f779-4f01-b662-ed4e232d2f99">

Fig. 4: _This is the ER diagram of the PillowTrackPro_

This is the ER Diagram for the database illustrating four tables: users, finances, customers and inventory. The "users" table has a integer primary key 'id' and attributes like 'email', 'username', and 'password'. The "finances" table has a integer primary key 'id' and attributes 'current_money'. Another table "customers" has a integer primary key 'customer_id' and attributes like 'customer_address' and 'total_price_of_order'. Last table "material" has a integer priary key 'id' and two attributes 'material_name' and 'quantity'.  


## Flow Diagram
<img width="max" alt="Screenshot 2024-03-10 at 2 36 46 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/2068eae7-1491-4c56-99fc-acfc756cdbbc">

Fig. 5 _This is the flow diagram of the 'show_bar_graph'_

This is the flow diagram for the code that is designed to show a bar graph of customer pillow material distribution. This code collects data on what pillow materials customers prefer, creates a visual bar graph to show these preferences, saves the graph as an image, and then displays it.


## Flow Diagram


## Flow Diagram


## Test Plan


| Description                                 | Test Type        | Input                                                                                                                                                                                                     | Expected Output                                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Test for Registration System                | Unit test        | 1. Run the project3.py file.   2. Click the "Signup" button on the application screen.   3. Input the information in each text field.   4. Click "Submit"                                                 | After clicking the "Signup" button, the screen shifts to the "Register" screen. After the user input all the informations,                                                                                                                                                                                                                                                                                           |
| Test for Login System                       | Unit test        | 1. Run the project3.py file.   2. Enter the appropriate information in each text field.   3. Click the "Login" button on the application screen.                                                          | After entering all the appropriate information and if the user can log in successfully, the screen shifts to "Menu Screen". If the user presses the "Login" button without entering anything or the user does not exist or the password doesn't match,  a pop-up message will appear letting the user know that the login failed.                                                                                    |
| Test for Forgot Password System             | Unit test        | 1. Run the project3.py file.   2. Click the "Forgot Pass?" button on the application screen.   3. Input the security question and email in each text field.   4. Click "Verify and Reset Password".       | When the user presses the "Forgot pass?" button, it should direct the user to the "Forgot Password?" screen. If the user is able to enter the appropriate security question and email, it should jump to the "Reset Password" screen. If not, a pop-up message will appear that tells the user that your email and security question answers do not match our records.                                               |
| Test for Reset Password System              | Unit test        | 1. Verify and Reset Password.   2. Enter the new password and confirm the new password.   3. Click "Update Password".  4. Click "Login" to go back to "Login Screen".                                     | When the user successfully comes to the reset screen, they can enter the new password and confirm it. If the user successfully enters the new password and it is confirmed, a pop-up message will appear that says "Password updated successfully" and if not, the pop-up message says "An error occurred during update". Also, they can go back to the "Login Screen" if they press "Login" button.                 |
| Test for Logout System                      | Unit test        | 1. Login   2. Click the logout button on the "Menu Screen".                                                                                                                                               | When the logout button is pressed, a pop-up message will appear telling you that once you log out, you need to log in again. If the user clicks the "YES" button inside a pop-up message, it will direct the user back to the "login screen".                                                                                                                                                                        |
| Test for Adding a New Order                 | Integration test | 1. Login to the application.   2. Navigate to the "Order" screen.   3. Fill in the order details (customer name, address, phone number, pillow material, pillow size, total price).  4. Submit the order. | The order details should be validated and saved to the database without errors. The inventory should be updated accordingly, decreasing the quantity of the used material. A success dialog should appear confirming the order submission. If any material is not sufficient, a warning dialog should appear instead.                                                                                                |
| Test for Viewing Customer Information       | Integration test | 1. Login to the application.   2. Navigate to the "Customers" screen.                                                                                                                                     | The screen should display a list of all customers and their order details fetched from the database. The information should match the records accurately.                                                                                                                                                                                                                                                            |
| Test for Financial Overview Display         | Integration test | 1. Login to the application.   2. Navigate to the "Finances" screen.                                                                                                                                      | The finances screen should display a pie chart and bar graph representing the company's financial distribution and customer pillow material distribution. The data should accurately reflect the current financial status and inventory details stored in the database.                                                                                                                                              |
| Test for Inventory Management               | Integration test | 1. Login to the application.   2. Navigate to the "Inventory" screen.  3. Adjust the quantity of materials using the '+' and '-' buttons.                                                                 | The inventory screen should list all materials with their current quantities. Adjusting the quantities should immediately update the database and reflect on the UI without errors.                                                                                                                                                                                                                                  |
| Test for Updating Customer Order            | Integration test | 1. Login to the application.   2. Navigate to the "Customers" screen.   3. Select a customer order and update its details.   4. Submit the changes.                                                       | The selected customer's order should be updated in the database with the new details provided. The "Customers" screen should reflect the changes immediately. If the changes affect the inventory or financials, those modules should update accordingly.                                                                                                                                                            |
| Test for Deleting a Customer Order          | Integration test | 1. Login to the application.   2. Navigate to the "Customers" screen.   3. Select a customer order and delete it.                                                                                         | The selected customer order should be removed from the database. The "Customers" screen should update to no longer show the deleted order. If the order had previously affected the inventory or financials, those modules should adjust to reflect the order's removal.                                                                                                                                             |
| Test for Pie Chart and Bar Graph Generation | Unit test        | 1. Login to the application.   2. Navigate to the "Finances" screen.   3. Request to view the pie chart or bar graph.                                                                                     | The application should generate and display the pie chart and bar graph based on the current data within the database. The pie chart should accurately represent the financial distribution among different expense categories and the remaining balance. The bar graph should accurately represent the distribution of customer pillow materials. There should be no errors or discrepancies in the data displayed. |
| Test for Password Complexity and Validation | Unit test        | 1. Navigate to the "Signup" or "Reset Password" screen.   2. Enter a password that does not meet the complexity requirements.                                                                             | The system should validate the password against the complexity requirements and provide immediate feedback if the password is not strong enough, prompting the user to choose a different password before allowing the submission.                                                                                                                     


## Record of Task

| Task No |                       Planned Action                       |                                                                                Planned Outcome                                                                                | Time estimate | Target completion date | Criterion |
|:-------:|:----------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|:-------------:|:----------------------:|:---------:|
| 1       | Meet with the client                                       | Have a meeting with the client and identify their problems. Brainstorm solutions and establish a plan to help resolve the client's problem.                                   | 20 min        | Feb 20                 | A         |
| 2       | Write out the problem definition                           | Clarify and write out the problem definition on the repositiory.                                                                                                              | 15 min        | Feb 20                 | A         |
| 3       | Write out proposed solution for the client                 | Brainstorm and clarify the justification of the resolution to client's problem.                                                                                               | 15 min        | Feb 22                 | A         |
| 4       | Define and write out success criteria                      | Clarify and write out the success criteria discussed and decided with client to resolve their problem.                                                                        | 15 min        | Feb 24                 | A         |
| 5       | Database design and implementation                         | Design the database for users, transactions, and inventory. Implement the database using SQLite.                                                                              | 30 min        | Feb 24                 | B         |
| 6       | Development of DatabaseBridge and other functions          | Implement DatabaseBridge class for this project and create functions for hashing and verification.                                                                            | 2 hours       | Feb 24                 | B,C       |
| 7       | User interface design for login and registration           | Design user-friendly interfaces for login and registration using KivyMD.                                                                                                      | 4 hours       | Feb 25                 | C         |
| 8       | Implement login functionality                              | Develop the logic for user authentication, including password hashing and session management.                                                                                 | 4 hours       | Feb 27                 | C         |
| 9       | Implement registration functionality                       | Develop the registration process, including user data validation, password hashing, and storing new user records.                                                             | 1 hour        | Mar 1                  | C         |
| 10      | Implement forgot password and reset functionalities        | Create interfaces and functions for password resetting, including security questions and email verification steps.                                                            | 3 hours       | Mar 3                  | C         |
| 11      | Develop the main menu and navigation system                | Implement the main menu GUI, enabling navigation between different sections of the application (ex. Finance, Orders, and inventory).                                          | 1 hour        | Mar 3                  | C         |
| 12      | Financial data visualization feature development           | Develop the finances screen, incorporating data visualization elements (pie charts and bar graphs) to represent financial insights and customer pillow material distribution. | 5 hours       | Mar 3                  | C         |
| 13      | Follow up meeting with client                              | Showing the application to the client and asking for their opinion on the application's current progress.                                                                     | 30 min        | Mar 3                  | A         |
| 14      | Customer information and order management system           | Create a code to manage customer information and orders, including GUIs for data entry and display using tables.                                                              | 2 hour        | Mar 4                  | C         |
| 14      | Inventory management system development                    | Implement inventory tracking and management features, integrating with the order processing system by adding and substracting materials.                                      | 5 hours       | Mar 4                  | C         |
| 15      | Enhance application security                               | Apply security best practices, including password encryption and registration.                                                                                                | 2 hour        | Mar 4                  | C         |
| 16      | Optimize application performance                           | Double-check all functions and debug if any bug is found; code function that would validate the input and ensure that input successes.                                        | 1 hour        | Mar 4                  | C         |
| 17      | Conduct final testing and client review                    | Flow diagrams for the different codes, and some brief explanations.                                                                                                           | 1 hour        | Mar 6                  | C         |
| 18      | Gather client's feedback                                   | Collect feedback from clients, and prioritize features and fixes small issues.                                                                                                | 1 hour        | Mar 6                  | C         |
| 19      | Create UML Diagram and write a brief description           | Have a clear UML Diagram that accurately shows the different classes and methods used with a brief explanation.                                                               | 30 min        | Mar 8                  | B         |
| 20      | Write the test plans                                       | Processes one by one and take to test the program and the expected outcome of each test is recorded.                                                                          | 1 hour        | Mar 8                  | B         |
| 21      | Create flow diagrams and write brief explanations for each | Have accurate flow diagrams for different parts of the porogram with brief explanations.                                                                                      | 1 hour        | Mar 9                  | B         |
| 22      | Finish Criteria C                                          | Write the descriptions of the code and the details of the techniques that were used.                                                                                          | 4 hours       | Mar 10                 | C         |
| 23      | Finish video for Criteria D                                | Video evidence of all the success criterias functioning and working within the developed applicaiton.                                                                         | 30 min        | Mar 10                 | D         |

# Criteria C: Development

## Technique Used
1. OOP paradigm
2. KivyMD Library
3. Relational databases
4. SQLite, ORM
5. functions
6. if statements
7. for loop

## Python file: "main.py"

### Setting up the file:

```.py
from kivy.core.window import Window
from kivymd.app import MDApp
from kivymd.uix.button import MDFlatButton
from kivymd.uix.label import MDLabel
from kivymd.uix.menu import MDDropdownMenu
from kivymd.uix.screen import MDScreen
from kivymd.uix.dialog import MDDialog
from kivymd.uix.datatables import MDDataTable
from kivy.metrics import dp
from kivymd.uix.textfield import MDTextField
from kivymd.uix.button import MDRaisedButton
from kivymd.uix.boxlayout import MDBoxLayout
from kivy.uix.image import Image
from Project.my_library import DatabaseBridge
import sqlite3
import matplotlib.pyplot as plt
import os
```





[^1]: Python vs Xcode: What are the differences? https://stackshare.io/stackups/python-vs-xcode#:~:text=In%20summary%2C%20Python%20is%20a,complex%20syntax%20and%20limited%20compatibility 
[^2]: Top 10 Python GUI Frameworks Compared. https://www.activestate.com/blog/top-10-python-gui-frameworks-compared/
[^3]: SQLite. (n.d.). SQLite Features. https://www.sqlite.org/features.html
[^4]: SQL Tutorial. (n.d.). What is SQLite? https://www.sqlitetutorial.net/what-is-sqlite/

