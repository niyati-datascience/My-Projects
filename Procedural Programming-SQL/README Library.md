# Lbrary Membership

## Overview

This assignment focuses on implementing stored procedures, triggers, and data management tasks in a relational database. The objective is to automate the process of managing overdue fines, updating member status, and performing related operations in a library system.

## Task 1: Update Fine Fees for Overdue Books

In this task, a stored procedure named `UpdateFineFeesForOverdue` is created to calculate and update fine fees for overdue books. The procedure performs the following:
- Identifies books that are overdue.
- Calculates the fine fee based on the number of days overdue.
- Updates the `FineFee` in the `Member` table for members who have overdue books.

## Task 2: Trigger for Automatic Member Status Update

A trigger, `update_member_status_trigger`, is implemented to automatically update a member's status. The trigger works when the `FineFee` of a member reaches
 zero and the member has returned at least one book. When these conditions are met, the member's status is updated to `'REGULAR'`.

## Task 3: Insert Sample Data into Tables

This task involves inserting sample data into the database to simulate real-world library operations. The following tables are populated with data:
- `Member`: Stores information about library members.
- `Book`: Contains details about books available in the library.
- `Borrowedby`: Represents records of books borrowed by members, including borrowing dates.
- `Holding`: Represents records of books that are currently in the library’s possession.

## Task 4: Procedure Execution and Trigger Activation

To execute the stored procedure and update overdue fines, the procedure `UpdateFineFeesForOverdue` is called. The trigger for updating member status 
(`update_member_status_trigger`) is activated automatically when changes are made to the `Member` table, particularly when the fine fee is updated.

---

## Conclusion

This assignment demonstrates the use of stored procedures and triggers to automate fine fee management and member status updates in a library system. 
By automating these tasks, the system ensures consistency, efficiency, and accurate tracking of library operations.


