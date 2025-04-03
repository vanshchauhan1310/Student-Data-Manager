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

## App.py File Format
The app.py file should follow this structure:
```app.py
import yaml

def load_data(file_path):
    """
    Load data from a YAML file.
    :param file_path: Path to the YAML file.
    :return: Data loaded from the YAML file.
    """
    with open(file_path, 'r') as file:
        data = yaml.safe_load(file)  # Load the data as a Python dictionary
    return data

def display_students(students):
    """
    Display information about all students.
    :param students: List of student dictionaries.
    """
    print("\nAll Students:")
    for student in students:
        print(f"Name: {student['name']}, Age: {student['age']}, Major: {student['major']}, GPA: {student['gpa']}")

def filter_students_by_gpa(students, min_gpa):
    """
    Filter and display students with a GPA above the specified minimum.
    :param students: List of student dictionaries.
    :param min_gpa: Minimum GPA for filtering.
    """
    filtered_students = [s for s in students if s['gpa'] >= min_gpa]
    print(f"\nStudents with GPA >= {min_gpa}:")
    if filtered_students:
        for student in filtered_students:
            print(f"Name: {student['name']}, Age: {student['age']}, Major: {student['major']}, GPA: {student['gpa']}")
    else:
        print("No students found.")

def main():
    # Load the data from the YAML file
    data = load_data('students.yaml')
    students = data['students']
    
    # Display all students
    display_students(students)
    
    # Filter students by GPA
    min_gpa = float(input("\nEnter minimum GPA to filter students: "))
    filter_students_by_gpa(students, min_gpa)

if __name__ == "__main__":
    main()
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
  - name: Charlie
    age: 20
    major: Physics
    gpa: 3.9
  - name: David
    age: 23
    major: Chemistry
    gpa: 3.2
  - name: Eva
    age: 21
    major: Computer Science
    gpa: 3.7
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
