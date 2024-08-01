IT Asset Management System

This project is an IT Asset Management System created using Microsoft Access. The system allows users to track IT assets by checking out and checking in assets to employees. It also provides the functionality to produce reports based on checkout date, check-in date, or employee department as filters.
Features

   1. Asset Check-Out: Allows users to check out assets to employees.
   2.  Asset Check-In: Allows users to check in assets and update their status and return condition.
   3.  Reporting: Generates reports based on various filters such as checkout date, check-in date, and employee department.
   4.  Asset Categorization: Categorizes IT assets for easy tracking and management.
   5.  Status Update: Updates the status of assets to reflect whether they are checked out or available.
   6.  Asset history: allows user to see history of an asset by asset tag

Installation

  Clone the Repository:

  bash

    git clone https://github.com/your-username/it-asset-management-system.git

  Open the Database:
      Open the ITAssetManagement.accdb file in Microsoft Access.

Usage
Checking Out an Asset

  1. Open the frmCheckOut form.
  2. Enter the Employee Number and Asset Tag.
  3. Click the Check Out button to complete the check-out process.

Checking In an Asset

  1. Open the frmCheckIn form.
  2. Enter the Asset Number and Employee Number.
  3. Select the Return Condition from the combo box.
  4. Enter the Check-In Date.
  5. Click the Check In button to update the transaction and asset status.

Generating Reports

  1. Open the desired report form (e.g., ReportByCheckoutDate, ReportByCheckInDate, ReportByDepartment).
  2. Select the appropriate filters.
  3. Click the Generate Report button to view the report.

Database Schema
Tables

    asset
        tag (Primary Key): Unique identifier for each asset.
        name: Name of the asset.
        category: Category of the asset.
        currentStatus: Current status of the asset (e.g., available, checked out).
  
    transaction
        transactionID (Primary Key): Unique identifier for each transaction.
        assetTag: Foreign key referencing asset(tag).
        employeeNo: Employee number who checked out the asset.
        checkOutDate: Date the asset was checked out.
        checkInDate: Date the asset was checked in (nullable).
        returnCondition: Condition of the asset upon return (nullable).

Contributing

  Fork the repository.
  Create your feature branch: git checkout -b feature/YourFeature.
  Commit your changes: git commit -m 'Add some feature'.
  Push to the branch: git push origin feature/YourFeature.
    Open a pull request.
