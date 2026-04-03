# Gradebook CLI


- Seed sample data:

```bash
python -m scripts.seed
```

> A lightweight, JSON-powered command-line interface (CLI) for managing students, courses, enrollments, and academic performance with ease. 🚀

---

## ✨ Features

* **👨‍🎓 Student Management:** Easily add and track students in the system.
* **📚 Course Catalog:** Create and manage course codes and titles.
* **🔗 Enrollment System:** Bridge students and courses securely.
* **📝 Grade Tracking:** Record individual floating-point grades (0-100).
* **🗂️ Local Persistence:** Lightweight, automated JSON storage—no database required!

---

## 🛠️ Tech Stack

* **Language:** Python 3
* **Libraries:** `argparse`, `logging`, `json`, `pathlib`, `unittest`
* **Storage:** Local JSON file (`data/gradebook.json`)

---

* **Separation of Concerns:** The logic is split into three distinct layers:
    * `models.py`: Defines the data structures (Student, Course, Enrollment).
    * `service.py`: Contains the "Business Logic" (calculating averages, validating grades).
    * `storage.py`: Handles all File I/O operations to ensure data integrity.
* **Logging over Printing:** Instead of simple print statements for errors, the project uses a dedicated `app.log` file. This is a best practice for production-grade software to track issues over time.

### ⚠️ Current Limitations

* **No Concurrency Support:** Since the app uses a flat JSON file, it does not support multiple users writing to the file at the exact same millisecond. This is intended for single-user CLI usage.
* **Grade Validation:** Grades are strictly capped between `0.0` and `100.0`. The system will reject any input outside this range to prevent skewed GPA data.
* **Case Sensitivity:** Course codes (e.g., `CS101` vs `cs101`) are currently case-sensitive. Users must ensure they use the exact code defined during course creation.
* **Manual Enrollment Required:** To maintain data relational integrity, a student must be explicitly enrolled in a course using the `enroll` command before any grades can be assigned to them.

### Setup
Clone the repository and navigate into the project folder:
```bash
git clone [https://github.com/yourusername/gradebook_project.git](https://github.com/yourusername/gradebook_project.git)
cd gradebook_project
