# README: Phonebook Management System

This is a simple Phonebook Management System implemented in C that allows users to store, manage, search, and edit contacts. The program supports various functionalities such as adding, displaying, editing, deleting, and searching contacts by name, number, or gender. It also allows managing a user profile and marking contacts as favorites.

### Features
1. **Add New Contact**: Allows the user to add a new contact with a name and phone number.
2. **Display My Profile**: Displays the pre-configured user profile (Name, Number, Email, Birth Date, Gender).
3. **Display All Contacts**: Displays a list of all contacts in the phonebook with their details.
4. **Display Contacts by Gender**: Displays contacts filtered by a specified gender (Male/Female).
5. **Display Favourite Contacts**: Displays contacts marked as "favourite."
6. **Search Contacts**: Allows searching for a contact either by name or phone number.
7. **Edit Contact**: Allows the user to edit the contact details like number, email, date of birth, gender, or mark a contact as a favorite.
8. **Delete Contact**: Allows the user to delete a contact by its name.
9. **Edit User Profile**: Allows the user to update their profile details (Name, Number, Email, Birth Date, Gender).

### Data Structure
The program uses a linked list to store contact information. Each contact is represented by a node (`contact`), which contains the following fields:
- `name`: Name of the contact (string).
- `num`: Primary phone number (string).
- `num2`: Secondary phone number (string).
- `email`: Email address (string).
- `gender`: Gender of the contact (string).
- `dob`: Date of birth (string, formatted as dd/mm/yyyy).
- `fav`: A flag indicating whether the contact is marked as a favorite (1 for true, 0 for false).
- `next`: Pointer to the next contact node in the linked list.

### Pre-configured Data
The program includes a set of predefined emergency numbers such as:
- Ambulance
- Police
- Fire Brigade
- Gas
- Railway
- Airway
- Service Centre
- etc.

These contacts are inserted automatically into the phonebook when the program starts.

### Compilation and Running
To compile and run the program, follow these steps:

1. Save the code in a file named `phonebook.c`.
2. Open a terminal or command prompt.
3. Navigate to the directory where `phonebook.c` is saved.
4. Run the following command to compile the program:
   ```
   gcc -o phonebook phonebook.c
   ```
5. Run the compiled program:
   ```
   ./phonebook
   ```

### Sample Output
```
======WELCOME TO YOUR PHONE BOOK=====
Press 1: Add new contact
Press 2: Display My Profile
Press 3: Display All Contacts
Press 4: Display specific Gender contact
Press 5: Display favourite contact
Press 6: Search Contact
Press 7: Edit contact
Press 8: Delete contact
Press 9: Edit My Profile
Press 0: Exit

Enter your choice = 1
Enter the name you want to insert = John Doe
Enter the number you want to insert = 1234567890

Contact added successfully!
```

### Functions
1. **`insert(node* head, char tmp_name[25], char tmp_num[11])`**: Inserts a new contact into the phonebook in alphabetical order by name.
2. **`searchName(node* head, char name[25])`**: Searches for a contact by name.
3. **`searchNum(node* head, char num[11])`**: Searches for a contact by number.
4. **`display(node* head)`**: Displays all contacts in the phonebook.
5. **`displayGender(node* head, char gender[7])`**: Displays contacts filtered by gender.
6. **`displayFavourite(node* head)`**: Displays contacts marked as favorites.
7. **`editContact(node* temp)`**: Allows editing of an existing contact's details.
8. **`deleteContact(node* head, char name[25])`**: Deletes a contact by name.
9. **`myprofile()`**: Displays the pre-configured user profile.
10. **`deleteContact()`**: Deletes a contact based on its name.

### Error Handling
- If a contact with the same name already exists, the program will add the new number to the existing contact.
- If a contact name or number does not exist during search or delete operations, the program will display a message indicating that no such contact exists.

### Notes
- The program supports storing two phone numbers per contact.
- The program uses basic C features like strings, linked lists, and file I/O (for user interaction). 
- It uses basic console I/O and doesn't require any special libraries, apart from standard ones (`stdio.h`, `stdlib.h`, `string.h`).

### Future Improvements
- **Persistent Data**: Currently, data is lost when the program is closed. Adding file handling to save and load data would make it more persistent.
- **Search Enhancements**: More advanced search options, such as searching by email or date of birth.
- **Graphical User Interface (GUI)**: Currently, the program uses text-based input and output. Implementing a GUI could make the user experience more intuitive.

### License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Thank you for using the Phonebook Management System!
