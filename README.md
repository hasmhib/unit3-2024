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
<img width="max" alt="Screenshot 2024-03-10 at 10 26 21 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/1920d80b-3296-4b1c-ad97-696d7964593a">

Fig. 3: _This is the UML diagram of the PillowTrackPro._

This is the UML diagram for the application, which displays the classes and methods that were used in its development. The diagram includes two main parent classes: MDApp and MDScreen. All subclasses inherit methods and attributes from these parent classes, as indicated by the arrows in the diagram.

The DatabaseBridge class in the diagram provides methods for establishing a connection to a SQLite3 database, searching for information within the database, saving information to the database, and closing the connection to the database.


## ER Diagram
<img width="max" alt="Screenshot 2024-03-07 at 11 53 30 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/d5e3429d-f779-4f01-b662-ed4e232d2f99">

Fig. 4: _This is the ER diagram of the PillowTrackPro_

This is the ER Diagram for the database illustrating four tables: users, finances, customers and inventory. The "users" table has a integer primary key 'id' and attributes like 'email', 'username', and 'password'. The "finances" table has a integer primary key 'id' and attributes 'current_money'. Another table "customers" has a integer primary key 'customer_id' and attributes like 'customer_address' and 'total_price_of_order'. Last table "material" has a integer priary key 'id' and two attributes 'material_name' and 'quantity'.  


## Flow Diagram
<img width="max" alt="Screenshot 2024-03-10 at 2 36 46 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/2068eae7-1491-4c56-99fc-acfc756cdbbc">

Fig. 5 _This is the flow diagram of the 'show_bar_graph'_

This is the flow diagram for the code that is designed to show a bar graph of customer pillow material distribution. This code collects data on what pillow materials customers prefer, creates a visual bar graph to show these preferences, saves the graph as an image, and then displays it.


## Flow Diagram
<img width="max" alt="Screenshot 2024-03-10 at 10 23 55 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/75f83466-f942-4538-8786-1f1aa8be012d">

Fig. 6 _This is the flow diagram of the 'update_password'_

This is the flow diagram of method updates a user's password after making sure it is correctly confirmed and then hash the new password in the database. If anything goes wrong such as the passwords don't match, it shows a pop-up messages to the user.


## Flow Diagram
<img width="max" alt="Screenshot 2024-03-10 at 3 18 01 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/4c136bde-8305-49dd-b244-7c6a28e582e2">

Fig. 7 _This is the flow diagram of the 'toggle_password_visibility'_

This is the flow diagram for the code that lets you switch between hiding and showing your password by clicking on an icon, and it changes the icon to match the password's visibility state.


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

## Development


## Success Criteria 1: The website keeps users separate with an encrypted login system and even if they forget their passwords, the users can change their passwords if they remember security questions.

I supports the criteria by incorporating an encrypted login system that hashes passwords, offers a method for password recovery using security questions, and allows updates of user passwords. The 'verify_login' functions allows users to login the application. The 'get_hash' and 'check_hash' functions indicate the use of encryption for password management, while the 'verify_and_reset_password' and 'update_password' methods provide the way for password recovery and resetting.

### 'get_hash' function

```.py
hasher = sha256_crypt.using(rounds = 30000)

def get_hash(text:str):
    return hasher.hash(text)
```
This code creates a function get_hash that uses SHA-256 algorithm to turn a given input (text) into a secure, hashed string, doing so through 30,000 rounds of processing.


### 'check_hash' function

```.py
hasher = sha256_crypt.using(rounds = 30000)

def check_hash(input_hash, text):
    return hasher.verify(text, input_hash)
```
This code defines a function 'check_hash' that checks if a given input (text) matches a provided hashed string using the SHA-256 algorithm with 30,000 rounds of hashing.


### 'verify_login' function

```.py
def verify_login(self):
    db_name = "project3.db"
    main.db = DatabaseBridge(db_name)

    username_or_email = self.ids.login_username_or_email.text.strip()
    password = self.ids.login_password.text.strip()

    query = "SELECT password FROM users WHERE username = ? OR email = ?"
    params = (username_or_email, username_or_email)

    result = main.db.search(query=query, params=params)

    # code continues
```

The verify_login method allow users to login to the application by validating their username (or email) and password against stored informations in the 'project3.db' database 'users' table. Firstly, this code connects to the database and fetches user inputs. It then checks the database whether a user with the provided username or email exists. If found, it checks whether the entered password matches the stored hashed password using a 'check_hash' method. If the match is successful, it clears the input fields, and navigates to the "MenuScreen." On the other hand, if the password does not match or no user is found, it displays a pop-up dialog letting users that the login attempt was unsuccessful.


```.py
def verify_and_reset_password(self):
    user_email = self.ids.email.text.strip()
    favorite_teacher = self.ids.favorite_teacher_answer.text.strip()

    query = "SELECT * FROM users WHERE email = ? AND favorite_teacher_answer = ?"
    params = (user_email, favorite_teacher)
    result = main.db.search(query=query, params=params)

    if result:
        reset_screen = self.manager.get_screen('ResetPasswordScreen')
        reset_screen.user_email = user_email  # Pass the email to the ResetPasswordScreen
        self.parent.current = "ResetPasswordScreen"
    else:
        self.show_verification_failed_dialog()
```

This code allows a user to reset their password by verifying their email and the answer to a security question (their favorite teacher during elementary school). If the information matches a record in the database, it directs the user to a "ResetPasswordScreen" where they can set a new password. If the verification fails, it shows an error pop-up dialog saying that your email and security question does not match.


### 'update_password' function

```.py
def update_password(self):
    user_email = self.user_email.strip()
    new_password = self.ids.new_pass.text.strip()
    confirm_password = self.ids.confirm_pass.text.strip()

    self.clear_input_fields()

    if not new_password or new_password != confirm_password:
        self.show_popup("Error", "Passwords do not match.")
        return

    # Hash the new password here
    hashed_new_password = get_hash(new_password)

    update_query = "UPDATE users SET password = ? WHERE email = ?"
    params = (hashed_new_password, user_email)
    # code continues
```

This code updates a user's password. It first checks if the new password and its confirmation match. If they do, it hashes the new password and updates it in the 'users' database for the user with the corresponding email. If the update is successful, it shows a success pop-up message; if not, it displays an pop-up message showing an error.


## Success Criteria 2: The application includes a financial tracking feature that accurately records and monitors the company's transactions such as expenses an income.




## Success Criteria 3: The application implements a resource management system within the app that specifically visualize the materials that are available for making pillows.

I fulfilled this success criteria by implementing three key functions: 'get_inventory_items' to fetch current material stock from the 'project3.db' database 'inventory' table, 'generate_inventory_ui' to create a user interface that displays these materials and their quantities, and 'update_inventory' to adjust stock levels of materials based on user interactions.

### 'get_inventory_items' functions

```.py
def get_inventory_items(self):
    query = "SELECT id, material_name, quantity FROM inventory"
    results = main.db.search(query=query, multiple=True)
    inventory_items = []
    for result in results:
        inventory_items.append({
            'id': result[0],
            'material_name': result[1],
            'quantity': result[2]
        })
    return inventory_items
```
This code retrieves the list of materials from the 'inventory' table. It runs a query to select the ID, name, and quantity of each material. For each item found, it adds a dictionary with these informations to a list, then returns. This process gathers current stock information and ready to be displayed or managed within the application.

### 'generate_inventory_ui' functions

```.py
def generate_inventory_ui(self):
    self.ids.inventory_list.clear_widgets()
    for item in self.inventory_items:
        material_id = item['id']
        material_name = item['material_name']
        quantity = item['quantity']
        # Code continues
```

This code creates the UI (user interface) for the 'InventoryScreen', showing each material's name and quantity that are stored in 'inventory' table. For each item, it sets up a horizontal layout with a label for the material name, a text field showing the quantity, and buttons to increase or decrease the quantity. When these buttons are clicked, they updates the inventory, adjusting the stock levels accordingly.


### 'update_inventory' functions

```.py
def update_inventory(self, material_id, change):
    # Update inventory quantity in the database
    current_quantity = [item['quantity'] for item in self.inventory_items if item['id'] == material_id][0]
    new_quantity = max(0, current_quantity + change)  # Ensure quantity doesn't go below 0
    update_query = "UPDATE inventory SET quantity = ? WHERE id = ?"
    main.db.update(update_query, (new_quantity, material_id))
    # Code continues
```

This code updates the quantity of a specific material in the inventory database. It first finds the current quantity of the material by fetching its ID, then calculates the new quantity by adding the change (which can be positive or negative) and it ensures the quantity never goes below 0. Then, it updates the database with the new quantity for the material. Finally, it refreshes the inventory items and the user interface to show the updated values.


## Success Criteria 4: The application provides detailed information about order and material management by using tables and graphs such as pie charts and bar graphs.




## Success Criteria 5: The application allows the user to search for orders by materials. 




# Criteria D: Functionlaity

## Demonstration video
https://drive.google.com/file/d/1tz2VrezD6CRP31pPIW8PfwshkYrk4gmb/view?usp=drive_link 



[^1]: Python vs Xcode: What are the differences? https://stackshare.io/stackups/python-vs-xcode#:~:text=In%20summary%2C%20Python%20is%20a,complex%20syntax%20and%20limited%20compatibility 
[^2]: Top 10 Python GUI Frameworks Compared. https://www.activestate.com/blog/top-10-python-gui-frameworks-compared/
[^3]: SQLite. (n.d.). SQLite Features. https://www.sqlite.org/features.html
[^4]: SQL Tutorial. (n.d.). What is SQLite? https://www.sqlitetutorial.net/what-is-sqlite/

