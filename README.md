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

### Setup
Clone the repository and navigate into the project folder:
```bash
git clone [https://github.com/yourusername/gradebook_project.git](https://github.com/yourusername/gradebook_project.git)
cd gradebook_project