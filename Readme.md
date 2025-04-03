# Student Data Manager - YAML & Python

## 📖 Overview
This application reads student information from a YAML file and provides functionality to display and filter student data based on GPA. It serves as a practical example of YAML file handling in Python.

## 🛠 Prerequisites
- Python 3.6+
- PyYAML library

## ⚙ Installation
1. Clone this repository or download the files
2. Install the required package:
   ```bash
   pip install pyyaml
   ```

## 📂 File Structure
```
student_data_manager/
├── app.py            # Main application script
├── students.yaml     # Student data in YAML format
└── README.md         # This documentation
```

## 👨‍💻 Usage
1. Place both app.py and students.yaml in the same directory
2. Run the application:
   ```bash
   python app.py
   ```

## 📝 YAML File Format
The students.yaml file should follow this structure:
```yaml
students:
  - name: Alice
    age: 21
    major: Computer Science
    gpa: 3.8
  - name: Bob
    age: 22
    major: Mathematics
    gpa: 3.5
```

## 💻 Application Features
- Load student data from YAML file
- Display all students with their details
- Filter students by minimum GPA

## 🏃‍♂️ Running the Application
When you execute the program, you'll see:
```
All Students:
Name: Alice, Age: 21, Major: Computer Science, GPA: 3.8
Name: Bob, Age: 22, Major: Mathematics, GPA: 3.5
...
Enter minimum GPA to filter students: 3.6
```

## 🚀 Expected Output
```
Students with GPA >= 3.6:
Name: Alice, Age: 21, Major: Computer Science, GPA: 3.8
...
```

## 🛠 Code Structure
- `load_data(file_path)` - Loads YAML data into Python dictionary
- `display_students(students)` - Prints all student information
- `filter_students_by_gpa(students, min_gpa)` - Filters students by GPA threshold
- `main()` - Orchestrates the program flow

## 📚 Learning Resources
- [PyYAML Documentation](https://pyyaml.org/wiki/PyYAMLDocumentation)
- [YAML Syntax Guide](https://yaml.org/spec/1.2.2/)

## 🤝 Contributing
Contributions are welcome! Please fork the repository and submit a pull request.

## 📄 License
MIT License
