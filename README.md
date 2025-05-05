## ClassCard Manager - Tasks

## Home Page

**Allow Only STI Students to Register**
- [ ] Require STI email address during registration (e.g., ends with @sti.edu.ph).
- [ ] Validate that the email ends with @sti.edu.ph before creating the account.
- [ ] Optionally verify the email via a confirmation link. Optionally verify the email via a confirmation link. 
- [ ] Block or redirect users with non-STI emails.
- [ ] (Optional) Keep a list of valid STI student IDs and check against it.

## Admin

**Soft Deletion of Accounts**
- [ ] Add a status column to the users table (e.g., active, deleted, dropped, etc.).
- [ ] When an admin deletes or deactivates a student:
- Update the status to deleted or dropped, do not remove the record.
- Record timestamp of deletion and reason if necessary.
- [ ] Filter out inactive users from the login and dashboard logic.

**Admin > Manage Schedules**
- [ ] Create a schedule management interface for assigning subjects and times to teachers.
- [ ] Allow CRUD operations (Create, Read, Update, Delete) for each schedule entry.
- [ ] Ensure schedules include: Teacher Name, Subject, Class, Day, and Time Slot.

## Teacher

**Assigned Class > Manage Class**
- [ ] Remove the student selection functionality in the teacher dashboard.
- Teachers should no longer have the ability to select or manage students for their classes.
- [ ] Display only relevant students in the teacher's dashboard.
- Ensure that only students assigned to the teacher by the admin are visible in the teacher's dashboard.

**Admin Dashboard Changes**
- [ ] Move the "Remove Student" functionality to the admin dashboard.
- Admins should be able to:
  - Remove or drop students (soft deletion) from classes.
  - Mark students as inactive, removed, or dropped without deleting their records.
- Admin should be able to manage which students are assigned to which classes.

**Manage Assignment > Create Assignment**
- [ ] Allow assignment type selection (e.g., multiple choice, quiz, essay, etc.).
- Provide a dropdown or radio buttons for the teacher/admin to select the type of assignment they are creating.
- [ ] Add time to the due date, not just the date.
- Implement a date and time picker for the due date, so teachers can specify both the date and exact time the assignment is due.
- [ ] Add a "Max Grade" field when creating an assignment.
- Teachers should be able to set a maximum possible grade (e.g., 100, 50, etc.).
- [ ] Enforce grade limit during grading. Enforce grade limit during grading.
- Prevent assigning a grade higher than the set max grade.

**Assignment History (Teacher & Student)**
- [ ] Display all submitted assignments under a specific assignment.
- Both teacher and student dashboards should show a history of submissions.
- [ ] Include grades for each submission.
- For students: show their own grade and submission status.
- For teachers: show a list of all students who submitted, with their corresponding grades.

**Grade Submissions**
- [ ] Hide graded submissions from the teacher’s "Grade Submissions" list after grading.
- [ ] Move graded submissions to a separate "Student Grades" section for record-keeping.
- [ ] Allow teachers to view graded submissions if needed (e.g., under a "Graded" tab or filter).

**Manage Attendance**
- [ ] Add a "Late" status alongside Present and Absent.
- [ ] Rename "Note" field to "Reason" for clarity and consistency.

**Student Grades**
- [ ] Create a dynamic table listing all students.
- [ ] Add columns for each assignment showing:
- Submission status (Submitted / Not Submitted / Late).
- Grade (if available).
- [ ] Add a final column to display the total or average grade per student.
- [ ] (Optional) option to export records (e.g., CSV or PDF)

**Teacher > View Schedules**
- [ ] Display a read-only view of the teacher’s assigned subject schedules.
- [ ] Group schedules by day and class for easy readability.

## Student

**Student > My Assignments**
- [ ] After submission, hide the assignment from the active assignment list.
- [ ] Move the submitted assignment to the Assignment History section for review and tracking.

