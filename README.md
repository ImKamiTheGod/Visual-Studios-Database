Database Configuration:

A SQL Server database is assumed to be created with a Customers table having columns like CustomerID, Name, Email, and Phone.
Windows Forms Application Setup:

A Windows Forms Application is created in Visual Studio.
The form includes TextBoxes for customer information, a DataGridView to display data, and buttons for actions (Add, Update, Delete).
DataSet and TableAdapter:

A DataSet named customerDataSet and a TableAdapter for the Customers table (CustomersTableAdapter) are added to the project.
Form Code Initialization:

The MainForm class is defined, and instances of CustomersTableAdapter and BindingSource are declared.
The constructor initializes these instances.
Form Load Event:

In the MainForm_Load event:
Data from the Customers table is loaded into the DataGridView.
A BindingSource is connected to the Customers table.
Add Button Click Event:

In the btnAdd_Click event:
Data validation is performed using the ValidateInput method.
If validation passes, a new customer is inserted into the database using the Insert method of the CustomersTableAdapter.
The DataGridView is refreshed to display the updated data.
Update Button Click Event:

In the btnUpdate_Click event:
Data validation is performed using the ValidateInput method.
If validation passes, the selected customer is updated in the database using the UpdateById method of the CustomersTableAdapter.
The DataGridView is refreshed to display the updated data.
Delete Button Click Event:

In the btnDelete_Click event:
The selected customer is deleted from the database using the DeleteById method of the CustomersTableAdapter.
The DataGridView is refreshed to display the updated data.
Data Validation:

The ValidateInput method performs basic validation, including checking the email format.
Additional validation rules can be added as needed.
Email Validation:

The IsValidEmail method checks the validity of an email address using the System.Net.Mail namespace.
GetSelectedCustomerId Method:

The GetSelectedCustomerId method retrieves the CustomerID of the selected row in the DataGridView.
In summary, this code provides a basic implementation for interacting with a SQL Server database from a Windows Forms Application, allowing users to add, update, and delete customer records. The code includes data validation and ensures the DataGridView reflects the changes made to the database.





