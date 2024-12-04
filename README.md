# CRM App with Django, Python, and MySQL

## Overview

This project is a simple Customer Relationship Management (CRM) application built with **Django**, **Python**, and **MySQL**. The CRM system allows you to manage customer data, including the ability to:

- Register users
- Log in and log out
- Add, view, update, and delete customer records

The project leverages MySQL for the database management and Django for the web framework.

## Features

- **User Authentication**: 
  - Register, log in, and log out functionality.
  - Password encryption and secure login system.
  
- **Customer Record Management**:
  - Add new customer records with details like name, contact info, and address.
  - View customer records in a simple table format.
  - Update customer information.
  - Delete customer records.

## Requirements

Before you get started, ensure that you have the following installed:

- **Python** 3.8+ 
- **Django** 4.0+ 
- **MySQL** Database
- **MySQL Client** for Python
- **pip** (Python's package installer)

## Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/yourusername/crm-app.git
   cd crm-app
   ```

2. **Create a virtual environment** (optional but recommended):

   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows use: venv\Scripts\activate
   ```

3. **Install required dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Set up MySQL Database**:
   
   - Install MySQL server if you haven't already.
   - Create a new database for the CRM app.
   
     ```sql
     CREATE DATABASE crm_db;
     ```

5. **Update database settings**:
   
   In the `settings.py` file, configure the database settings under the `DATABASES` section. Replace the placeholder values with your MySQL username, password, and database name.

   ```python
   DATABASES = {
       'default': {
           'ENGINE': 'django.db.backends.mysql',
           'NAME': 'crm_db',
           'USER': 'your_username',
           'PASSWORD': 'your_password',
           'HOST': 'localhost',
           'PORT': '3306',
       }
   }
   ```

6. **Migrate the database**:

   Run the following command to create the necessary tables in your MySQL database:

   ```bash
   python manage.py migrate
   ```

7. **Create a superuser** (optional, for admin access):

   You can create an admin user to access the Django admin panel:

   ```bash
   python manage.py createsuperuser
   ```

8. **Run the development server**:

   Now you can start the Django development server:

   ```bash
   python manage.py runserver
   ```

   Visit `http://127.0.0.1:8000` in your browser to access the app.

## Usage

### Authentication:

- **Register**: Use the registration form to create a new account.
- **Login**: After registration, you can log in with your credentials.
- **Logout**: Use the logout option to exit your session.

### Customer Records:

- **Add Customer**: After logging in, you can add new customer records by filling out the form with details such as name, email, phone number, and address.
- **View Records**: View all customer records in a table with options to update or delete.
- **Update Records**: You can edit customer information by selecting the "Edit" button next to a record.
- **Delete Records**: You can delete customer records by clicking the "Delete" button next to each customer.


## Testing

To run the unit tests, use the following command:

```bash
python manage.py test
```

## Contributing

Feel free to fork the project, submit issues, and create pull requests. Contributions are welcome!

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature-name`).
6. Create a new Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

### Acknowledgments

- Django documentation (https://www.djangoproject.com/)
- MySQL documentation (https://dev.mysql.com/doc/)
