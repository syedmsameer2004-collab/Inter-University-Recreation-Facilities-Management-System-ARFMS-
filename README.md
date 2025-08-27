1. Run Your SQL Scripts (In Order)
Execute these scripts in SSMS or your SQL client:
1. scripts/01_create_database_schema.sql - Creates ARFMS database and all tables
2. scripts/02_insert_sample_data.sql - Adds sample data for testing
3. scripts/03_alter_supply_requests_add_rejected.sql - Adds rejected status option

2. Update Connection String
File: Data/DatabaseConnection.cs

// Your connection string should point to ARFMS database
private static string connectionString = "Server=.\\SQLEXPRESS;Database=ARFMS;Integrated Security=true;";

3. Verify Database Creation
After running 01_create_database_schema.sql , you should have:
ARFMS database with 10 main tables
Sample users with different roles (Manager, Student, MaintenanceStaff)
Facility types and facilities ready for booking
Complete schema matching your C# models
Your SQL script already handles everything - database creation, table structure, relationships, and constraints. Just run the scripts in order and update the connection
string to match your SQL Server instance!
