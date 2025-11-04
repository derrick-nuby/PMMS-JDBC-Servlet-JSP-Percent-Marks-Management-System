# Percent Marks Management System (PMMS)

<div align="center">
  <img src="./images/rectangle_logo_transparent.png" alt="PMMS Logo" width="400"/>
  
  ### A Comprehensive Academic Records Management Platform
  
  [![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)](https://www.java.com/)
  [![Servlet](https://img.shields.io/badge/Servlet-JSP-blue)](https://jakarta.ee/specifications/servlet/)
  [![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://html.spec.whatwg.org/)
  [![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)](https://www.w3.org/Style/CSS/)
</div>

---

## 📋 Table of Contents

- [About](#about)
- [Key Features](#key-features)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage Guide](#usage-guide)
  - [For Students](#for-students)
  - [For Lecturers](#for-lecturers)
  - [For Administrators](#for-administrators)
- [File Format Support](#file-format-support)
- [User Roles](#user-roles)
- [Screenshots](#screenshots)
- [Contributing](#contributing)
- [License](#license)
- [Contact & Support](#contact--support)

---

## 🎯 About

The **Percent Marks Management System (PMMS)** is a Java-based web application powered by Servlets and JSP, designed to streamline academic administration and enhance user experience for students and faculty alike. This comprehensive platform facilitates efficient management of academic records, supporting multiple file formats including Excel and PDF for seamless data handling and reporting.

### Vision

To empower students to take control of their academic journey and inspire educators to engage, evaluate, and guide with precision.

### Mission

Provide a seamless and efficient environment that fosters academic growth, transparency, and collaboration between students, lecturers, and administrators.

---

## ✨ Key Features

### 🎓 Student Features
- **Real-time Grade Access**: View marks and performance across all enrolled modules
- **Mark Appeals**: Submit appeals for grade reviews with detailed justification
- **Academic Dashboard**: Comprehensive view of academic progress and achievements
- **Print Functionality**: Generate and print mark sheets
- **Transcript Generation**: Create academic transcripts in multiple formats
- **Profile Management**: Update and manage personal information

### 👨‍🏫 Lecturer Features
- **Efficient Mark Entry**: Streamlined interface for entering and updating student marks
- **Appeals Management**: Review and respond to student mark appeals
- **Class Performance Overview**: Comprehensive analytics of class performance
- **Multiple Assessment Types**: Support for quizzes, CATs, labs, projects, and exams
- **Batch Operations**: Upload marks for multiple students simultaneously
- **Export Capabilities**: Generate reports in Excel and PDF formats

### 👑 Administrator Features
- **User Management**: Add, edit, and manage students, lecturers, and administrative staff
- **Faculty Management**: Create and organize faculties and departments
- **Subject Management**: Configure subjects, codes, and assigned instructors
- **System Monitoring**: Track system status and user activities
- **Comprehensive Dashboard**: Overview of system-wide statistics and operations
- **Access Control**: Manage user roles and permissions

### 🔒 Security Features
- **Secure Authentication**: Role-based login system
- **Data Privacy**: Industry-standard practices for data protection
- **Session Management**: Secure session handling for all user types
- **Access Control**: Role-based access to different system modules

---

## 🛠️ Technology Stack

### Backend
- **Java**: Core programming language
- **Java Servlets**: Server-side request handling
- **JSP (JavaServer Pages)**: Dynamic web page generation
- **JDBC**: Database connectivity and operations

### Frontend
- **HTML5**: Structure and content
- **CSS3**: Styling and responsive design
- **JavaScript**: Client-side interactivity and validation

### Database
- **JDBC-compatible Database**: (MySQL/PostgreSQL/Oracle)
- Relational database for storing:
  - User information (students, lecturers, admins)
  - Academic records and marks
  - Subject and faculty data
  - Appeal records

### File Processing
- **Apache POI**: Excel file generation and manipulation
- **iText/JasperReports**: PDF document generation
- Support for data import/export in multiple formats

---

## 📁 Project Structure

```
PMMS-JDBC-Servlet-JSP-Percent-Marks-Management-System/
│
├── admin/                      # Administrator module
│   ├── index.html             # Admin dashboard
│   ├── add.html               # Add entities (students, lecturers, subjects)
│   ├── manage.html            # Manage system resources
│   ├── status.html            # System status monitoring
│   ├── admindocs.html         # Admin documentation
│   └── admin.css              # Admin-specific styles
│
├── lecturer/                   # Lecturer module
│   ├── index.html             # Lecturer dashboard
│   ├── marks.html             # Mark entry and management
│   ├── appeals.html           # Review student appeals
│   └── lecturer.css           # Lecturer-specific styles
│
├── student/                    # Student module
│   ├── index.jsp              # Student dashboard
│   ├── marks.jsp              # View marks and grades
│   ├── profile.jsp            # Student profile management
│   └── student.css            # Student-specific styles
│
├── images/                     # Image assets
│   ├── favicon/               # Favicon files
│   ├── team/                  # Team member photos
│   ├── rectangle_logo_transparent.png
│   ├── pmms_logo_square.png
│   └── upload.png
│
├── index.html                  # Main landing page
├── login.html                  # Authentication page
├── about.html                  # About the system
├── guide.html                  # User guide
├── contact.html                # Contact information
├── style.css                   # Global styles
└── README.md                   # This file
```

---

## 🚀 Installation

### Prerequisites

Before you begin, ensure you have the following installed:
- **Java Development Kit (JDK)** 8 or higher
- **Apache Tomcat** 9.0 or higher (or any Java servlet container)
- **MySQL/PostgreSQL** database server
- **Apache Maven** (optional, for dependency management)
- **Git** (for cloning the repository)

### Step-by-Step Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/derrick-nuby/PMMS-JDBC-Servlet-JSP-Percent-Marks-Management-System.git
   cd PMMS-JDBC-Servlet-JSP-Percent-Marks-Management-System
   ```

2. **Database Setup**
   ```sql
   -- Create database
   CREATE DATABASE pmms_db;
   
   -- Use the database
   USE pmms_db;
   
   -- Create required tables for the system
   -- (Database schema documentation will be added in future updates)
   ```

3. **Configure Database Connection**
   - Update the database connection parameters in your servlet configuration
   - Modify `db.properties` or relevant configuration file:
     ```properties
     db.url=jdbc:mysql://localhost:3306/pmms_db
     db.username=your_username
     db.password=your_password
     db.driver=com.mysql.cj.jdbc.Driver
     ```

4. **Deploy to Apache Tomcat**
   
   **Option A: Manual Deployment**
   - Copy the project folder to Tomcat's `webapps` directory
   - Start Tomcat server
   
   **Option B: IDE Deployment**
   - Import project into Eclipse/IntelliJ IDEA
   - Configure Tomcat server in IDE
   - Run the project

5. **Access the Application**
   - Open your web browser
   - Navigate to: `http://localhost:8080/PMMS-JDBC-Servlet-JSP-Percent-Marks-Management-System/`
   - Default admin credentials (if provided in setup):
     - Username: `admin`
     - Password: `admin123`

### Initial Setup

After installation:
1. Log in with administrator credentials
2. Set up faculties and subjects
3. Add lecturers to the system
4. Enroll students
5. Configure academic year settings

---

## 📖 Usage Guide

### For Students

1. **Login**
   - Navigate to the login page
   - Enter your student credentials
   - Access your personal dashboard

2. **View Marks**
   - Click on "Marks" in the navigation menu
   - Browse marks by module/subject
   - View detailed breakdown of:
     - Quizzes
     - Continuous Assessment Tests (CATs)
     - Lab work
     - Projects
     - Examinations

3. **Submit Appeals**
   - Navigate to specific mark entry
   - Click "Appeal" button
   - Provide detailed justification
   - Submit for lecturer review

4. **Generate Reports**
   - Use "Print Marks" to generate mark sheets
   - Use "Generate Transcript" for comprehensive academic records
   - Export to PDF format

5. **Update Profile**
   - Access profile section
   - Update personal information
   - Change password

### For Lecturers

1. **Login**
   - Use lecturer credentials to access the system
   - Access your dashboard

2. **Enter Marks**
   - Navigate to "Marks" section
   - Select subject and assessment type
   - Enter marks for students:
     - Individual entry
     - Batch upload via Excel
   - Save and submit

3. **Review Appeals**
   - Access "Appeals" section
   - Review student appeal requests
   - Provide feedback
   - Approve or reject with comments

4. **View Class Performance**
   - Access analytics dashboard
   - View class statistics
   - Generate performance reports
   - Export data in Excel/PDF format

5. **Manage Assessments**
   - Create new assessments
   - Set grading criteria
   - Configure weightage for different components

### For Administrators

1. **System Management**
   - Access admin dashboard
   - Monitor system status
   - View user statistics

2. **User Management**
   - **Add Students**
     - Navigate to Add → Students
     - Fill in student details
     - Assign to faculty and year
   
   - **Add Lecturers**
     - Navigate to Add → Lecturers
     - Enter lecturer information
     - Assign subjects
   
   - **Manage Users**
     - Edit user information
     - Reset passwords
     - Deactivate/activate accounts

3. **Academic Setup**
   - **Create Faculties**: Add new faculties and departments
   - **Add Subjects**: Configure subject codes and details
   - **Assign Teachers**: Link lecturers to subjects
   - **Set Academic Calendar**: Configure semester dates

4. **System Configuration**
   - Configure system settings
   - Manage permissions
   - Set up backup schedules
   - Monitor system logs

---

## 📊 File Format Support

### Supported Import Formats
- **Excel (.xlsx, .xls)**: Batch mark upload
- **CSV**: Student and lecturer data import
- **Text files**: Configuration imports

### Supported Export Formats
- **PDF**: 
  - Student transcripts
  - Mark sheets
  - Performance reports
  - Official documents
  
- **Excel (.xlsx)**:
  - Mark sheets for analysis
  - Class performance data
  - Student rosters
  - Statistical reports

### Import/Export Features
- **Bulk Operations**: Upload marks for entire classes
- **Data Validation**: Automatic validation of imported data
- **Error Reporting**: Detailed error logs for failed imports
- **Template Downloads**: Pre-formatted templates for data import
- **Customizable Reports**: Configure report layouts and content

---

## 👥 User Roles

### Student
- View personal marks and grades
- Submit mark appeals
- Generate transcripts
- Update profile information
- **Access Level**: Personal data only

### Lecturer
- Enter and update marks
- Review student appeals
- Generate class reports
- View assigned class performance
- **Access Level**: Assigned classes and subjects

### Administrator
- Full system access
- User management (CRUD operations)
- System configuration
- Report generation for all users
- Database maintenance
- **Access Level**: System-wide access

---

## 📸 Screenshots

*Screenshots will be added in future updates to showcase the user interface and key features of the system.*

### Key Interfaces

- **Landing Page**: Welcoming homepage introducing PMMS features
- **Student Dashboard**: Clean, intuitive interface for tracking academic progress
- **Marks View**: Detailed breakdown of marks across modules and assessments
- **Lecturer Dashboard**: Comprehensive tools for managing marks and appeals
- **Admin Panel**: Powerful administrative interface for system management

---

## 🤝 Contributing

We welcome contributions to improve PMMS! Here's how you can help:

### How to Contribute

1. **Fork the Repository**
   ```bash
   # Click the "Fork" button on GitHub
   ```

2. **Create a Feature Branch**
   ```bash
   git checkout -b feature/AmazingFeature
   ```

3. **Make Your Changes**
   - Write clean, documented code
   - Follow existing code style
   - Add comments where necessary

4. **Test Your Changes**
   - Ensure all existing functionality works
   - Test new features thoroughly
   - Check for security vulnerabilities

5. **Commit Your Changes**
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```

6. **Push to Your Branch**
   ```bash
   git push origin feature/AmazingFeature
   ```

7. **Open a Pull Request**
   - Provide a clear description of changes
   - Reference any related issues
   - Wait for review and feedback

### Contribution Guidelines

- **Code Style**: Follow Java coding conventions
- **Documentation**: Update README for significant changes
- **Testing**: Include test cases for new features
- **Security**: Never commit sensitive data or credentials
- **Commits**: Write clear, concise commit messages

### Areas for Contribution

- 🐛 Bug fixes
- ✨ New features
- 📝 Documentation improvements
- 🎨 UI/UX enhancements
- 🔒 Security improvements
- 🌐 Internationalization
- ♿ Accessibility features

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### MIT License Summary

- ✅ Commercial use
- ✅ Modification
- ✅ Distribution
- ✅ Private use
- ❌ Liability
- ❌ Warranty

---

## 📞 Contact & Support

### Team

**Derrick IRADUKUNDA** - Lead Developer
- GitHub: [@derrick-nuby](https://github.com/derrick-nuby)
- Email: [contact@derrick-nuby.dev](mailto:contact@derrick-nuby.dev)

### Support Channels

- **Students**: [support-students@percentsystem.com](mailto:support-students@percentsystem.com)
- **Lecturers**: [support-lecturers@percentsystem.com](mailto:support-lecturers@percentsystem.com)
- **Technical Issues**: [GitHub Issues](https://github.com/derrick-nuby/PMMS-JDBC-Servlet-JSP-Percent-Marks-Management-System/issues)

### Reporting Issues

When reporting issues, please include:
1. **Description**: Clear description of the problem
2. **Steps to Reproduce**: How to recreate the issue
3. **Expected Behavior**: What should happen
4. **Actual Behavior**: What actually happens
5. **Environment**: OS, browser, Java version, etc.
6. **Screenshots**: If applicable

### Feature Requests

Have an idea to improve PMMS? We'd love to hear it!
- Open an issue on GitHub
- Label it as "enhancement"
- Provide detailed description of the feature
- Explain the use case and benefits

---

## 🙏 Acknowledgments

- All contributors who have helped improve this project
- The educational institutions that inspired this system
- The open-source community for excellent tools and libraries
- Students and educators who provide valuable feedback

---

## 📈 Project Status

**Current Version**: 1.0.0
**Status**: Active Development
**Last Updated**: 2024

### Roadmap

- [ ] Mobile responsive design improvements
- [ ] REST API implementation
- [ ] Integration with external LMS systems
- [ ] Advanced analytics and reporting
- [ ] Email notification system
- [ ] Multi-language support
- [ ] Dark mode theme
- [ ] Automated backup system

---

## 🔗 Quick Links

- [Installation Guide](#installation)
- [Usage Guide](#usage-guide)
- [Contributing Guidelines](#contributing)
- [Contact & Support](#contact--support)

---

<div align="center">
  
  ### ⭐ Star this repository if you find it helpful!
  
  **© 2024 Percent Marks Management System. All rights reserved.**
  
  Made with ❤️ for Education
  
</div>
