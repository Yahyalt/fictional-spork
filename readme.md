# Facebook Login Test Automation Project

This project contains automated test cases for Facebook login functionality using Katalon Studio. The test suite covers both positive and negative test scenarios to ensure comprehensive validation of the login process.

## 📋 Project Overview

This Katalon Studio project automates testing of Facebook's login functionality, including:
- Valid login scenarios
- Invalid login scenarios (empty fields, invalid credentials)
- UI element validation
- Error message verification

## 🚀 Prerequisites

Before running this project, ensure you have:

1. **Katalon Studio** (version 7.0 or higher)
   - Download from [Katalon Official Website](https://www.katalon.com/download/)
2. **Java Development Kit (JDK)** 8 or higher
3. **Web Browser** (Chrome, Firefox, Edge)
4. **Internet Connection** (required for Facebook access)

## 📁 Project Structure

```
fictional-spork/
├── Include/
│   └── config/
│       └── log.properties          # Logging configuration
├── Object Repository/
│   └── Page_Facebook log in or sign up/
│       ├── button_Log in.rs        # Login button object
│       ├── input_...rs             # Input field objects
│       ├── profile*.rs             # Profile-related objects
│       └── *.rs                    # Other UI elements
├── Profiles/
│   └── default.glbl               # Default execution profile
├── Reports/                       # Test execution reports
├── Scripts/
│   ├── Negative Case/
│   │   ├── Login with empty email/
│   │   ├── Login with empty password/
│   │   └── login with invalid email but valid password/
│   └── Positive Case/
│       └── Login with valid data/
├── Test Cases/
│   ├── Negative Case/
│   │   ├── Login with empty email.tc
│   │   ├── Login with empty password.tc
│   │   └── login with invalid email but valid password.tc
│   └── Positive Case/
│       └── Login with valid data.tc
├── Test Suites/
│   ├── test suite 03012024.groovy
│   └── test suite 03012024.ts
└── settings/                      # Project configuration files
```

## 🧪 Test Scenarios

### Positive Test Cases
- **Login with valid data**: Tests successful login with correct email and password

### Negative Test Cases
- **Login with empty email**: Validates error handling when email field is empty
- **Login with empty password**: Validates error handling when password field is empty
- **Login with invalid email but valid password**: Tests error handling for invalid email format

## 🔧 Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd fictional-spork
   ```

2. **Open Project in Katalon Studio**
   - Launch Katalon Studio
   - Select "Open Project"
   - Navigate to the project directory and select `fictional-spork.prj`

3. **Configure Browser Settings**
   - Go to Project Settings → Execution → WebUI
   - Configure desired browser preferences
   - Ensure WebDriver is properly configured

4. **Update Test Data (if needed)**
   - Update test credentials in test cases as needed
   - Modify object selectors if Facebook UI changes

## ▶️ Running Tests

### Individual Test Cases
1. Navigate to `Test Cases` folder
2. Right-click on desired test case
3. Select "Run" → Choose browser
4. Monitor execution in the Log Viewer

### Test Suite Execution
1. Navigate to `Test Suites` folder
2. Right-click on `test suite 03012024.ts`
3. Select "Run" → Choose execution profile
4. View results in the generated report

### Command Line Execution
```bash
katalon -projectPath="<project-path>" -testSuiteId="Test Suites/test suite 03012024" -browserType="Chrome" -reportFolder="Reports" -reportFileName="TestReport"
```

## 📊 Test Reports

Test execution reports are automatically generated in the `Reports/` directory:
- **HTML Reports**: Detailed execution results with screenshots
- **CSV Reports**: Tabular format for data analysis
- **JUnit Reports**: XML format for CI/CD integration
- **Execution Logs**: Detailed step-by-step execution information

### Report Structure
```
Reports/
└── [timestamp]/
    ├── [timestamp].html    # Main HTML report
    ├── [timestamp].csv     # CSV data export
    ├── JUnit_Report.xml    # JUnit format
    └── execution0.log      # Detailed logs
```

## ⚙️ Configuration

### Logging Configuration
- Edit `Include/config/log.properties` to modify logging levels
- Available levels: DEBUG, INFO, WARN, ERROR

### Execution Profiles
- Default profile: `Profiles/default.glbl`
- Add custom profiles for different environments

### Object Repository
- All page objects are stored in `Object Repository/Page_Facebook log in or sign up/`
- Update selectors if Facebook UI changes
- Use Spy Object tool to capture new elements

## 🔍 Troubleshooting

### Common Issues
1. **Login Failures**
   - Verify Facebook is accessible
   - Check if test credentials are valid
   - Ensure no CAPTCHA or security checks

2. **Element Not Found**
   - Update object selectors using Object Spy
   - Check for dynamic content loading
   - Verify element visibility and interactability

3. **Browser Issues**
   - Update WebDriver to latest version
   - Clear browser cache and cookies
   - Try different browser if issues persist

### Self-Healing
- Project includes self-healing capabilities
- Broken objects are tracked in `Reports/Self-healing/broken-test-objects.json`
- Review and approve suggested fixes

## 🚨 Important Notes

- **Test Data**: Use test accounts only; avoid personal Facebook credentials
- **Rate Limiting**: Facebook may impose rate limits on automated access
- **UI Changes**: Facebook UI updates may require object repository updates
- **Security**: Never commit real credentials to version control

## 📈 Best Practices

1. **Maintenance**
   - Regularly update object selectors
   - Review and update test data
   - Monitor execution reports for patterns

2. **Execution**
   - Run tests in headless mode for CI/CD
   - Use proper wait strategies for dynamic content
   - Implement screenshot capture for failures

3. **Reporting**
   - Archive old reports periodically
   - Set up automated report distribution
   - Monitor test execution trends

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is for educational and testing purposes only. Ensure compliance with Facebook's Terms of Service when using this automation.

## 📞 Support

For issues or questions:
- Check the troubleshooting section
- Review Katalon documentation
- Contact the test automation team

---

**Last Updated**: January 2024
**Katalon Studio Version**: 7.0+
**Target Application**: Facebook Login Page
