# Kanban Task Tracker with Eisenhower Matrix

## Description

This is a client-side Kanban board application designed to help users manage their tasks effectively. It incorporates the Eisenhower Matrix for task prioritization, allowing users to categorize tasks based on urgency and importance. The application features a drag-and-drop interface for moving tasks between status columns ("To Do," "In Progress," "Done"), various filtering and sorting options, and data visualization through charts. All data is stored locally in the user's browser using `localStorage`.

## Key Features

* **Kanban Board:**
    * Three main columns: "To Do," "In Progress," and "Done."
    * Drag-and-drop functionality to move tasks between these columns.
    * Task counters for each column.
* **Eisenhower Matrix Prioritization:**
    * Tasks are assigned a priority based on their urgency and importance:
        * **Do First:** Urgent and Important
        * **Schedule:** Not Urgent but Important
        * **Delegate:** Urgent but Not Important
        * **Delete:** Not Urgent and Not Important
    * Priority is set using "Urgent" and "Important" checkboxes in the task modals, with the resulting action (Do, Schedule, etc.) displayed.
    * Tasks are visually distinguished by priority on the board.
* **Task Management:**
    * Add new tasks with a title, detailed notes, category, tags, due date, and priority.
    * Edit existing tasks.
    * Archive completed tasks (removes them from the main board but keeps them in an accessible archive).
    * Permanently delete tasks (from the board or archive).
* **Dashboard & Views:**
    * **Summary Info:** Displays the current date, total pending tasks.
        * Lists "Today's Tasks" and "Overdue Tasks" for quick visibility.
    * **Task Status by Priority:** Pie charts showing the status distribution (To Do, In Progress, Done) for each Eisenhower priority category.
    * **Category Comparison Chart:** A bar chart showing the total number of non-archived tasks per category.
    * **Filtered Task Views (Accordion):**
        * Filter tasks by user-defined categories.
        * Filter tasks by status (To Do, In Progress, Done).
* **Category Management:**
    * Users can define and manage their own list of categories.
    * Categories can be assigned to tasks via a dropdown in the Add/Edit modals.
    * Option to add new categories directly from the task modals.
* **Controls:**
    * Search tasks by title, description, or tags.
    * Filter tasks on the main board by priority.
    * Sort tasks on the main board by creation date (newest first), due date (ascending/descending).
* **Data Management:**
    * Export all tasks to JSON or CSV format.
    * Import tasks from JSON or CSV files (note: import replaces all current tasks).
    * Manage custom categories (add/delete).
* **Visual Feedback:**
    * Confetti animation when a task is moved to "Done."
    * Visual cues for overdue and due-soon tasks on the task cards.

## Tech Stack

This is a purely client-side application built with:

* **HTML:** For the structure and content.
* **CSS (Tailwind CSS & Custom CSS):** For styling.
    * Tailwind CSS is loaded via CDN.
    * Custom CSS is embedded in `<style>` tags.
* **JavaScript (Vanilla JS):** For all logic, interactivity, and DOM manipulation.
* **External JavaScript Libraries (via CDN):**
    * **Chart.js:** For pie and bar charts.
    * **Canvas Confetti:** For the completion animation.
* **Data Storage:**
    * **Browser `localStorage`:** Used to store tasks and categories locally on the user's machine.

## How to Run / Deploy

1.  **Files:** The entire application is contained within a single `index.html` file (or whatever you name it). This file includes all HTML, CSS, and JavaScript.
2.  **Running Locally:** Simply open the `index.html` file in a modern web browser.
3.  **Deployment (Hosting):**
    * Since it's a static client-side application, it can be hosted on any static web hosting service.
    * Examples: GitHub Pages, Netlify, Vercel, AWS S3 (configured for static website hosting), Firebase Hosting, or any traditional web host that supports serving static files.
    * Upload the `index.html` file to your chosen hosting provider.
    * No backend server or database setup is required for the current functionality.

## Potential Future Enhancements

* Subtasks for breaking down larger tasks.
* Due date reminders/notifications (browser-based).
* User-selectable themes or appearance customization.
* More advanced filtering (e.g., by multiple tags, date ranges).
* Recurring tasks.
* Task activity log/history.
* A dedicated table view for tasks as an alternative to the Kanban board.

