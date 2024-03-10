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
he application includes a financial tracking feature that accurately records and monitors the company's transactions such as expenses an income and visualize this by using pie charts. (Issue: _“I suffer with an financial losses due to incorrectly recorded orders”_)

### 3. Resource Management for Production:
The application implements a resource management system within the app that specifically visualize the materials that are available for making pillows. (Issue: _"I was not able to track the materials, and there are many times when resources were over-booked, and I had to buy materials again, losing profits."_) 

### 4. Comprehensive Order and Material Management:
The application provides detailed information about order and material management by using tables and graphs such as bar graphs. (Issue: _“There are lots of inefficiencies in order and material management and I need to calculate these every time.”_)

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

### Screen Manager
```.py
ScreenManager:

    id: main_scr
    MainScreen:
        name: "MainScreen"
    SecondScreen:
        name: "SecondScreen"
    ForgotPasswordScreen:
        name: "ForgotPasswordScreen"
    ResetPasswordScreen:
        name: "ResetPasswordScreen"
    MenuScreen:
        name: "MenuScreen"
    FinancesScreen:
        name: "FinancesScreen"
    CustomersScreen:
        name: "CustomersScreen"
    OrderScreen:
        name: "OrderScreen"
    InventoryScreen:
        name: "InventoryScreen"
```
The Screen Manger on kivy file provides a efficient way to organize and directs between different screens in an application.


### toggle password function _(class MainScreen, SecondScreen and ResetPasswordScreen)_

```.py
def toggle_password_visibility(self):
    # Toggle the visibility state
    self.password_visible = not self.password_visible

    # Find the password and confirm password fields by their ids
    password_field = self.ids.upass
    confirm_password_field = self.ids.cpass

# Code continued
```
This function, 'toggle_password_visibility', changes whether passwords are visible or hidden in the user interface. It flips the state of self.password_visible to its opposite value. Depending on the new visibility state, it either shows or hides the password. When passwords are set to be visible, the function changes an icon to an "eye" symbol to show that the passwords can be seen. On the other hand, when it hides the passwords, it changes the icon to "eye-off," signaling that the passwords are now not visible.


https://github.com/hasmhib/unit3-2024/assets/142870448/f628b1e6-27a1-488c-bc37-80fac4411fff

Fig. 8: _Demonstrating the 'toggle_password_visibility' function_


### Show dialog _(class LoginScreen and ForgotPasswordScreen)_

```.py
    def show_verification_failed_dialog(self):
        if not hasattr(self, 'verification_failed_dialog'):
            self.verification_failed_dialog = MDDialog(
                title="Verification Failed",
                text="Your email and security question answer do not match our records.",
                buttons=[
                    MDFlatButton(
                        text="OK",
                        theme_text_color="Custom",
                        on_release=lambda x: self.verification_failed_dialog.dismiss()
                    )
                ],
            )
        self.verification_failed_dialog.open()
```
This code is on eexample of implementation of pop-up dialog. This function, 'show_verification_failed_dialog', displays a dialog box when a user's verification attempt fails, specifically when their email and security question answer do not match the application's records.


<img width="max" alt="Screenshot 2024-03-11 at 1 54 14 AM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/b64a36ef-47fa-442e-873d-7b6369393b08">

Fig. 9: _An example of Dialog_

## Success Criteria 1: The website keeps users separate with an encrypted login system and even if they forget their passwords, the users can change their passwords if they remember security questions.

I supports the criteria by incorporating an encrypted login system that hashes passwords, offers a method for password recovery using security questions, and allows updates of user passwords. The 'verify_login' functions allows users to login the application. The 'get_hash' and 'check_hash' functions indicate the use of encryption for password management, while the 'verify_and_reset_password' and 'update_password' methods provide the way for password recovery and resetting.

### 'get_hash' function _(class DatabaseBridge)_

```.py
hasher = sha256_crypt.using(rounds = 30000)

def get_hash(text:str):
    return hasher.hash(text)
```
This code creates a function get_hash that uses SHA-256 algorithm to turn a given input (text) into a secure, hashed string, doing so through 30,000 rounds of processing.


### 'check_hash' function _(class DatabaseBridge)_

```.py
hasher = sha256_crypt.using(rounds = 30000)

def check_hash(input_hash, text):
    return hasher.verify(text, input_hash)
```
This code defines a function 'check_hash' that checks if a given input (text) matches a provided hashed string using the SHA-256 algorithm with 30,000 rounds of hashing.


### 'verify_login' function _(class MainScreen)_

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


###  'verify_and_reset_password' _(class ForgotPasswordScreen)_

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


### 'update_password' function _(class ResetPasswordScreen)_

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

This code updates a user's password. It first checks if the new password and its confirmation match and if they do, it hashes the new password and updates it in the 'users' database for the user with the corresponding email. If then update is successful, it shows a success pop-up message; if not, it displays an pop-up message showing an error.


## Success Criteria 2: The application includes a financial tracking feature that accurately records and monitors the company's transactions such as expenses an income and visualize this by using pie charts.

I achieved the financial tracking feature by creating pie charts in the "FinancesScreen" with the 'show_pie_chart' function, and accurately recording transactions through the 'submit_order' function in the "OrderScreen". This functions allows for both monitoring of expenses and income, and their visualization.


### 'show_pie_chart' functions _(class FinanceScreen)_

```.py
def show_pie_chart(self):
    pie_charts_directory = os.path.join(os.getcwd(), 'temp')
    if not os.path.exists(pie_charts_directory):
        os.makedirs(pie_charts_directory)

    pie_chart_path = os.path.join(pie_charts_directory, 'finance_pie_chart.png')

    finance_data = self.get_finance_data()
    fig, ax = plt.subplots()
    ax.pie(finance_data['amounts'], labels=finance_data['categories'], autopct='%1.1f%%')
    plt.title('Finance Distribution')
    plt.savefig(pie_chart_path)
    plt.close(fig)

    self.ids.chart_container.clear_widgets()
    self.ids.chart_container.add_widget(Image(source=pie_chart_path))
```

This code generates a pie chart to visualize financial data and displays it within the user interface. It first checks if a directory for storing pie charts exists, creating one if not exists. Then, it prepares a file for the new pie chart. Using financial data gets back by 'get_finance_data', it creates the pie chart with percentages, create titles "Finance Distribution", and saves the chart to the plt.savefig path to adjust to the app. Finally, it clears any existing pie charts in the chart container and adds the newly created pie chart image for display.

<img width="max" alt="Screenshot 2024-03-11 at 0 39 02 AM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/1ee24916-4856-43d3-9a36-1acac4fd81b3">

Fig. 10: _An example of pie charts shown in "FinanceScreen" This example is 'Rent': 15000, 'Salaries': 30000, 'Utilities': 5000, 'Marketing': 10000_ 


### 'submit_order' function _(class OrderScreen)_

```.py
def submit_order(self):
# Address the terms

    MATERIAL_PRICES = {
        "Buckwheat hulls": 3000,
        "Low rebound urethane": 2500,
        "High resilience urethane": 3500,
        "Pipe": 3000,
        "Down": 5000,
        "Feather": 7000,
        "Polyester wadding": 6000,
        "Fiber": 6500
    }

    if not all([customer_name, customer_address, customer_phone_number, pillow_material, pillow_size, total_price]):
        print("Please fill in all fields.")
        return

    material_cost = MATERIAL_PRICES.get(pillow_material, 0)

    inventory_query = "SELECT id, quantity FROM inventory WHERE material_name = ?"
    inventory_item = main.db.search(inventory_query, (pillow_material,))

    required_quantity = 1

    if inventory_item and inventory_item[1] >= required_quantity:
    # Code continues
```

The 'submit_order function' processes customer orders by receiving inputs from users about informations such as customer name, address, phone number, pillow material, size, and the total price. The function checks make sure every informations are filled and verifies whether requested material is available by checking quantity 'inventory' table. After validation, it inserts the order details into the 'customer' table, updates the inventory to reflect the used materials, and adjusts the financial records to include the sale's revenue while substracting material costs. 


## Success Criteria 3: The application implements a resource management system within the app that specifically visualize the materials that are available for making pillows.

I fulfilled this success criteria by implementing three key functions: 'get_inventory_items' to fetch current material stock from the 'project3.db' database 'inventory' table, 'generate_inventory_ui' to create a user interface that displays these materials and their quantities, and 'update_inventory' to adjust quantity levels of materials based on user interactions.

### 'get_inventory_items' functions _(class InventoryScreen)_

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
This code retrieves the list of materials from the 'inventory' table. It then runs a query to select the ID, name, and quantity of each material. For each item found, it adds a dictionary with these informations to a list, then returns. This process gathers current quantity stock information and ready to be displayed or managed within the application.


### 'generate_inventory_ui' functions _(class InventoryScreen)_

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


### 'update_inventory' functions _(class InventoryScreen)_

```.py
def update_inventory(self, material_id, change):
    # Update inventory quantity in the database
    current_quantity = [item['quantity'] for item in self.inventory_items if item['id'] == material_id][0]
    new_quantity = max(0, current_quantity + change)  # Ensure quantity doesn't go below 0
    update_query = "UPDATE inventory SET quantity = ? WHERE id = ?"
    main.db.update(update_query, (new_quantity, material_id))
    # Code continues
```

This code updates the quantity of a specific material in the inventory database. It first finds the current quantity of the material by fetching its ID, then calculates the new quantity by adding the change (which can be positive change or negative change) and it ensures the quantity never goes below 0. Then, it updates the database with the new quantity for the material. Finally, it refreshes the inventory items and the user interface to show the updated values.


## Success Criteria 4: The application provides detailed information about order and material management by using tables and graphs such as bar graphs.

I fulfilled this criteria by implementing the 'show_bar_graph' functions in the "FinancesScreen" class for showcasing customer preferences based on the data stored in 'customers' table. Furthermore, I utilized the 'update_table' function in the "OrderScreen" class to manage and display detailed information about orders, including materials used.


### 'show_bar_graph' functions _(class FinanceScreen)_

```.py
def show_bar_graph(self):
    bar_graph_directory = os.path.join(os.getcwd(), 'bar_graph')
    if not os.path.exists(bar_graph_directory):
        os.makedirs(bar_graph_directory)

    bar_graph_path = os.path.join(bar_graph_directory, 'customer_pillow_material_graph.png')

    default_materials = {
        "Buckwheat hulls": 0,
        "Low rebound urethane": 0,
        "High resilience urethane": 0,
        "Pipe": 0,
        "Down": 0,
        "Feather": 0,
        "Polyester wadding": 0,
        "Fiber": 0
    }

    # Query to count each pillow material type
    pillow_material_query = """
    SELECT customer_pillow_material, COUNT(*) as material_count 
    FROM customers 
    GROUP BY customer_pillow_material
    """

    pillow_material_data = self.execute_query(pillow_material_query)

    if pillow_material_data:
        # Update counts for materials found in the query
        for material, count in pillow_material_data:
            if material in default_materials:  # Ensure that only expected materials are counted
                default_materials[material] += count

    materials = list(default_materials.keys())
    counts = list(default_materials.values())

    # Plotting the bar graph    
    # Code continues
```
This code creates a bar graph showing the distribution of pillow materials based on customer preferences and displays it within the application. It first ensures a directory for storing bar graphs exists, then generates a path for the new graph. It sets initial counts of various pillow materials to zero and queries the 'customers' table to add these counts based on actual customer data that are stored in the 'customers' database. Using this data, it plots a bar graph with materials on the x-axis and quantity on the y-axis, saves the graph to the 'bar_graph' path, and then updates the application's UI to display the new graph by clearing previous images in the chart container and adding the new bar graph image.

<img width="max" alt="Screenshot 2024-03-11 at 0 48 04 AM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/8194d969-4fc8-4898-aae5-a50a61cca65b">

Fig. 11: _An example of bar graphs shown in "FinanceScreen"_


### 'update_table' functions _(class CustomerScreen)_

```.py
def update_table(self):
    data = main.db.search(query="SELECT customer_id, customer_name, customer_address, customer_phone_number, customer_pillow_material, customer_pillow_size, total_price_of_ordered_pillow FROM customers", multiple=True)
    self.data_table.row_data = data
```
This code updates a table in the application with customer order details by fetching data from the database and setting it as the new row data for the table.



## Success Criteria 5: The application allows the user to search for orders by materials. 

I fulfilled this criteria by implementing the "OrderScreen" class and function 'search_by_material'. This function enables users to specify a material and outputs all orders that used that particular material in pop-up dialog, showcasing the application's capability to filter and display order information based on material criteria.


### 'search_by_material' function _(class OrderScreen)_

```.py
def search_by_material(self):
    material = self.ids.search_material.text
    if not material or material == 'Select Material':
        self.show_popup("Error", "Please select a material to search.")
        return

    # Execute the search query
    results = main.db.search(
        "SELECT customer_name, customer_phone_number FROM customers WHERE customer_pillow_material = ?",
        (material,))

    # Ensure results is a list (even for no or single result)
    # Code continues
```

This function retrieves the selected material from the user interface, choose the materials, and then queries the 'customers' table for orders that match the requested material. Based on the query results, it either displays the matching orders to the pop-up screen or let the user know that no orders were found for the selected material, effectively allowing users to filter orders by material type.

<img width="max" alt="Screenshot 2024-03-11 at 1 13 18 AM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/bfe33163-b4d2-47a8-93d8-d152e6e1c12e">

Fig. 12: _An example of 'search_by_material' shown in "OrderScreen"_


# Criteria D: Functionlaity

## Demonstration video
https://drive.google.com/file/d/1tz2VrezD6CRP31pPIW8PfwshkYrk4gmb/view?usp=drive_link 


[^1]: Python vs Xcode: What are the differences? https://stackshare.io/stackups/python-vs-xcode#:~:text=In%20summary%2C%20Python%20is%20a,complex%20syntax%20and%20limited%20compatibility 
[^2]: Top 10 Python GUI Frameworks Compared. https://www.activestate.com/blog/top-10-python-gui-frameworks-compared/
[^3]: SQLite. (n.d.). SQLite Features. https://www.sqlite.org/features.html
[^4]: SQL Tutorial. (n.d.). What is SQLite? https://www.sqlitetutorial.net/what-is-sqlite/

