# 🌤️ OpenWeatherMap API Testing Project

![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Newman](https://img.shields.io/badge/Newman-66B135?style=for-the-badge&logo=postman&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![API Testing](https://img.shields.io/badge/API%20Testing-Automated-blue?style=for-the-badge)

## 📋 Project Overview

Comprehensive API testing suite for **OpenWeatherMap Current Weather API** with **19 test scenarios** covering functional testing, negative testing, and edge case validation. Complete documentation with **Newman CLI automation** for CI/CD integration.

---

## 🎯 Key Highlights

- ✅ **19 Test Scenarios** across 5 functional areas
- ✅ **184 Test Assertions** with comprehensive validation
- ✅ **100% Pass Rate** - All tests passing
- ✅ **2.2 Second** total execution time
- ✅ **33ms Average Response Time** (min: 9ms, max: 216ms)
- ✅ **Documentation** (8 professional documents, 40+ pages)
- ✅ **Newman CLI Integration** for automation
- ✅ **Professional GitHub Repository** ready for portfolio

---

## 📊 Test Coverage

| Category           | Test Cases | Focus Areas                                              |
| ------------------ | ---------- | -------------------------------------------------------- |
| **Happy Path**     | 11         | Valid inputs, all search methods, formats, units         |
| **Error Handling** | 8          | Authentication (401), Not Found (404), Bad Request (400) |
| **Edge Cases**     | -          | Case sensitivity, special characters, spaces in names    |
| **Total**          | **19**     | **Comprehensive coverage**                               |

### Search Methods Tested

- ✅ City Name (with spaces, special characters, case variations)
- ✅ Geographic Coordinates (latitude, longitude)
- ✅ City ID
- ✅ ZIP Code + Country Code

### Features Validated

- ✅ Response Formats: JSON, XML
- ✅ Localization: Spanish language support
- ✅ Temperature Units: Metric (Celsius), Imperial (Fahrenheit), Standard (Kelvin)
- ✅ Error Responses: 400, 401, 404 scenarios
- ✅ Data Types & Structure validation
- ✅ Business Logic & Range validation

---

## 🛠️ Tech Stack

- **API Testing:** Postman v11+
- **Test Automation:** Newman CLI
- **Scripting Language:** JavaScript
- **Documentation Standard:** ISTQB
- **Version Control:** Git/GitHub
- **Reporting:** Newman HTML Extra

---

## 🚀 Quick Start

### Prerequisites

- **Node.js & npm** installed
- **Postman** installed
- **OpenWeatherMap API key** ([Get free key](https://openweathermap.org/api))

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/YOUR_USERNAME/weather-api-testing.git
   cd weather-api-testing
   ```

2. **Install Newman:**

   ```bash
   npm install -g newman newman-reporter-htmlextra
   ```

3. **Set up environment:**
   - Copy `collection/OpenWeatherAPI.postman_environment.TEMPLATE.json`
   - Rename to `OpenWeatherAPI.postman_environment.json`
   - Replace `YOUR_API_KEY_HERE` with your actual API key

### Run Tests in Postman

1. **Import collection:**
   - Open Postman
   - Import `collection/Project 1 - Weather API Testing- OpenWeatherMap.postman_collection`

2. **Import environment:**
   - Import your configured environment file
   - Ensure `apiKey` and `baseUrl` are set

3. **Run collection:**
   - Click "Run" button
   - Execute all 19 test cases
   - View results: 184/184 assertions passed

### Run Tests via Newman CLI

```bash
newman run collection/"Project 1 - Weather API Testing- OpenWeatherMap.postman_collection" \
  -e OpenWeatherAPI.postman_environment.json \
  -r htmlextra,cli \
  --reporter-htmlextra-export reports/newman-report.html
```

**Expected Output:**

```
┌─────────────────────────┬────────────────┬───────────────┐
│                         │       executed │        failed │
├─────────────────────────┼────────────────┼───────────────┤
│              iterations │              1 │             0 │
├─────────────────────────┼────────────────┼───────────────┤
│                requests │             19 │             0 │
├─────────────────────────┼────────────────┼───────────────┤
│            test-scripts │             19 │             0 │
├─────────────────────────┼────────────────┼───────────────┤
│              assertions │            184 │             0 │
└─────────────────────────┴────────────────┴───────────────┘

total run duration: 2.2s
average response time: 33ms
```

---

## 📁 Project Structure

```
weather-api-testing/
├── README.md                          # This file
├── .gitignore                         # Git ignore rules
├── collection/
│   ├── postman_collection             # Postman collection (19 test cases)
│   └── environment.TEMPLATE.json      # Environment template (safe for sharing)
├── documentation/
│   ├── Test_Plan.docx                 # 14-section ISTQB test plan
│   ├── Test_Case_Design.docx          # Detailed test cases (19)
│   ├── Test_Descriptions.docx         # Postman documentation content
│   ├── Test_Data_Reference.docx       # Test data values & ranges
│   ├── Requirements_Traceability_Matrix.docx
│   ├── Test_Environment_Readiness.docx
│   ├── Test_Plan_Approval.docx
│   └── Test_Execution_Summary_Report.docx  # Results & metrics
├── reports/
│   └── newman-report.html             # Newman HTML test report
└── screenshots/
    ├── postman-collection-run-summary.png
    ├── newman-cli-execution.png
    └── newman-html-report.png
```

---

## 📈 Test Results

### Overall Metrics

| Metric                    | Value       | Status  |
| ------------------------- | ----------- | ------- |
| **Total Test Scenarios**  | 19          | ✅      |
| **Total Assertions**      | 184         | ✅      |
| **Tests Passed**          | 184         | ✅      |
| **Tests Failed**          | 0           | ✅      |
| **Pass Rate**             | 100%        | ✅      |
| **Total Execution Time**  | 2.2 seconds | ✅      |
| **Average Response Time** | 33 ms       | ✅      |
| **Min Response Time**     | 9 ms        | ✅      |
| **Max Response Time**     | 216 ms      | ✅      |
| **Performance Threshold** | < 2000ms    | ✅ PASS |

### Results by Test Folder

| Folder                       | Test Cases | Status           |
| ---------------------------- | ---------- | ---------------- |
| Folder 1: City Name          | 8          | ✅ PASS          |
| Folder 2: Coordinates        | 2          | ✅ PASS          |
| Folder 3: City ID            | 2          | ✅ PASS          |
| Folder 4: ZIP Code           | 2          | ✅ PASS          |
| Folder 5: Formats/Parameters | 5          | ✅ PASS          |
| **TOTAL**                    | **19**     | **✅ 100% PASS** |

---

## 📚 Documentation

All ISTQB-compliant documentation available in `/documentation`:

1. **Test Plan** (14 sections)
   - Test objectives, scope, strategy
   - Environment details, responsibilities
   - Schedule, milestones, risks
   - 19 test scenarios breakdown

2. **Test Case Design** (19 detailed test cases)
   - Preconditions, test steps, test data
   - Expected results, assertions
   - Priority levels, status tracking

3. **Requirements Traceability Matrix**
   - Requirements mapped to test cases
   - Coverage verification

4. **Test Data Reference**
   - Valid/invalid test data
   - Temperature ranges for all units
   - Coordinate tolerances

5. **Test Execution Summary Report**
   - Actual test results with metrics
   - Performance analysis
   - Conclusion & recommendations

---

## 🔍 API Endpoints Tested

**Base URL:** `https://api.openweathermap.org/data/2.5`

**Endpoint:** `/weather`

### Test Scenarios by Category

**Folder 1: Current Weather by City Name (8 tests)**

- TC001: Valid city name
- TC002: Invalid city name (404)
- TC003: Missing API key (401)
- TC004: Invalid API key (401)
- TC005: Case insensitive city name
- TC006: City name with spaces
- TC007: City name with special characters
- TC008: Empty city name (400)

**Folder 2: Current Weather by Coordinates (2 tests)**

- TC009: Valid coordinates
- TC010: Invalid coordinates (404/400)

**Folder 3: Current Weather by City ID (2 tests)**

- TC011: Valid city ID
- TC012: Invalid city ID (404)

**Folder 4: Current Weather by ZIP Code (2 tests)**

- TC013: Valid ZIP code
- TC014: Invalid ZIP code (404)

**Folder 5: Response Formats & Parameters (5 tests)**

- TC015: XML response format
- TC016: Spanish language localization
- TC017: Metric units (Celsius)
- TC018: Imperial units (Fahrenheit)
- TC019: Standard units (Kelvin)

---

## 💡 Key Learnings

### Technical Skills Demonstrated

- ✅ Comprehensive API test design
- ✅ JavaScript test scripting in Postman
- ✅ Error handling & negative testing
- ✅ Data validation (types, ranges, structure)
- ✅ Business logic validation
- ✅ Newman CLI automation
- ✅ HTML report generation
- ✅ Git/GitHub version control

### Testing Best Practices Applied

- ✅ ISTQB documentation standards
- ✅ Requirements traceability
- ✅ Comprehensive test coverage (happy path + error scenarios + edge case scenarios)
- ✅ Assertion levels: Status → Structure → Data Types → Business Logic
- ✅ Performance validation
- ✅ CI/CD ready automation

### Challenges Solved

- **Floating-point precision:** Used `.closeTo()` with tolerance for coordinate validation instead of `.equal()` to handle decimal variations in geographic coordinates
- **Optional vs Required fields:** Only validated required fields to prevent random failures. Learned that fields like `visibility` are optional and cause tests to fail unpredictably
- **Case-insensitive validation:** Validated using `.toLowerCase()` for matching names and error messages, making tests more robust and flexible against capitalization changes. Without it, tests would fail if API returned "london" instead of "London", or "api key" instead of "API key".
- **Advanced JavaScript patterns:** Initially struggled with the approach for checking a word from a particular language in API responses. Used `.some()` and arrow functions- more elegant than multiple OR operators.
- **Dynamic temperature ranges:** Temperature validation depends on units parameter - validated appropriate ranges per unit system (Celsius: -50 to 50°C, Fahrenheit: -58 to 122°F, Kelvin: 223 to 323K)
- **Special characters handling:** Validated proper handling of accented characters in city names (São Paulo) by ensuring the API preserves special characters in responses
- **Test organization:** Used folder-level tests for common validations to avoid code duplication across similar test cases.

---

## 🎓 Professional Standards

This project follows industry best practices:

- **ISTQB Guidelines:** Test plan structure, test case design, traceability
- **IEEE 829 Standard:** Documentation templates and formats
- **API Testing Best Practices:** Comprehensive coverage, automation, reporting
- **Version Control:** Clean Git history, proper .gitignore, meaningful commits

---

## 📞 Contact

**Renuka**

- 💼 LinkedIn: www.linkedin.com/in/renukaporje
- 📧 Email: renuka.suresh224@gmail.com
- 🌐 Portfolio:

---

## 🙏 Acknowledgments

- **OpenWeatherMap** for providing the free API
- **Postman** for the excellent testing platform
- **Newman** for CLI automation capabilities

---

**⭐ If you find this project helpful, please consider giving it a star!**
