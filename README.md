# User Management System

## Overview

This project is a straightforward Python user management system. Classes for managing users, verifying user data, and carrying out different tasks including adding, editing, and removing users are all included.


## Classes and Methods

### `User` Class

- **Purpose**: Uses information like the user ID, name, last name, email, password, and birthday to represent a user.- **Methods**:
  - `__init__(self, user_id, name, surname, email, password, birthday)`: Initializes a new user.
  - `get_details(self)`: Returns the user's details as a formatted string.
  - `get_age(self)`: Calculates and returns the user's age.

### `UserService` Class

- **Purpose**: Maintains a user list and offers tools for adding, locating, removing, and updating users.
- **Methods**:
  - `add_user(cls, user)`: Adds a user to the list.
  - `find_user(cls, user_id)`: Finds and returns a user by their ID.
  - `delete_user(cls, user_id)`: Deletes a user by their ID.
  - `update_user(cls, user_id, name, email)`: Updates a user's name and email.
  - `get_number(cls)`: Returns the number of users.

### `UserUtil` Class

- **Purpose**: Offers useful techniques for creating user IDs, passwords, and emails as well as for email and password validation.
- **Methods**:
  - `generate_user_id()`: Generates a new user ID.
  - `generate_password()`: Generates a strong password.
  - `is_strong_password(password)`: Checks if a password is strong.
  - `generate_email(name, surname, domain)`: Generates an email address.
  - `validate_email(email)`: Validates an email address.

## How to Run the Code

1. Verify that Python is installed on your computer.
2. Make a local copy of the repository.
3. Go to the directory for the project.
4. To communicate with the user management system, execute the `main.py` file:
   ```sh
   python main.py
   ```
5. To run the tests, use the following command:
   ```sh
   python -m unittest discover
   ```

## UML Class Diagram

<img width="849" alt="Снимок экрана 2025-02-19 в 00 42 18" src="https://github.com/user-attachments/assets/a135b757-a522-41a0-85f7-fb61a30d1b72" />



## Sample Runs

### Input
```
Enter your name: Argen
Enter your surname: Kulzhanov
Enter your birthday YYYY-MM-DD (like 2000-01-01): 2005-12-07
```

### Output
```
User added successfully!
ID:230121012
Name: Argen
Surname: Kulzhanov
Email: argen.kulzhanov@gmail.com
Password: P@ssw0rd!
Birthday: 2005_12_07

User age: 19

Email validation:  argen.kulzhanov@gmail.com is Valid email
Password strength: P@ssw0rd! is strong
```

### Test Output
```
Launching unittests with arguments python -m unittest /Users/argenkulzhanov/Desktop/work/OOP argen/OOPArgenKulzhanovAssigment4/test.py in /Users/argenkulzhanov/Desktop/work/OOP argen/OOPArgenKulzhanovAssigment4


10)Generated Email: maga.magomedow@gmail.com

8)Generated Password: X%1PAi3l

7)Generated User ID: 259990581

9)Generated password is strong: S%7Gp51=
    Password is strong: Password123!
    Password is weak: password123

11)Generated email: maga.magomedow@gmail.com is Valid email
   Invalid email: maga.magomedow@gmail.com is Not valid email

User Age: Argen 19

User Details: ID:230121012, Name: Argen, Surname: Kulzhanov, Email: argen.kulzhanov@gmail.com, Password: password123, Birthday: 2005-12-07

Added Users:
ID:230121012, Name: Argen, Surname: Kulzhanov, Email: argen.kulzhanov@gmail.com, Password: password123, Birthday: 2005-12-07
ID:230121008, Name: Kirill, Surname: Donetskov, Email: kirill.donetskov@gmil.com, Password: password456, Birthday: 2005-06-12
ID:230121024, Name: Meder, Surname: Rahatbekov, Email: meder.rahatbekov@gmail.com, Password: password789, Birthday: 2003-03-15

5)User: None
Before Update: ID:230121008, Name: Kirill, Surname: Donetskov, Email: kirill.donetskov@gmil.com, Password: password456, Birthday: 2005-06-12

6)Updated User: ID:230121008, Name: Beks, Surname: Donetskov, Email: beks.kulzhanov@gmail.com, Password: password456, Birthday: 2005-06-12

Process finished with exit code 0

test_add_user (__main__.TestUserService) ... ok
test_delete_user (__main__.TestUserService) ... ok
test_find_user (__main__.TestUserService) ... ok
test_update_user (__main__.TestUserService) ... ok
test_generate_email (__main__.TestUseUtil) ... ok
test_generate_password (__main__.TestUseUtil) ... ok
test_generate_user_id (__main__.TestUseUtil) ... ok
test_is_strong_password (__main__.TestUseUtil) ... ok
test_validate_email (__main__.TestUseUtil) ... ok
test_get_age (__main__.TestUser) ... ok
test_get_details (__main__.TestUser) ... ok

----------------------------------------------------------------------
Ran 11 tests in 0.001s

OK
```

A UML class diagram, instructions for executing the code, an outline of the classes and methods, and example runs to illustrate the functionality are all included in this documentation.
