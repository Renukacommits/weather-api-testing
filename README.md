# 🌤️ OpenWeatherMap API Testing Project

![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Newman](https://img.shields.io/badge/Newman-66B135?style=for-the-badge&logo=postman&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![API Testing](https://img.shields.io/badge/API%20Testing-Automated-blue?style=for-the-badge)

## 📌 Project Overview

API testing suite for **OpenWeatherMap Current Weather API**, focused on **functional testing, negative testing, and edge case validation**. This project demonstrates **practical API testing skills**, structured test design, and robust JavaScript assertions suitable for real-world QA work.

---

## 🎯 What This Project Demonstrates

- API test design based on requirements and risk
- Functional + negative + edge case testing
- JavaScript assertions in Postman
- Automated execution using Newman CLI
- Clear validation of response structure, data, and business rules

---

## 📊 Test Coverage Summary

### API Endpoint Tested

- **Base URL:** `https://api.openweathermap.org/data/2.5`
- **Endpoint:** `/weather`

| Category           | Test Cases | Focus Areas                                              |
| ------------------ | ---------- | -------------------------------------------------------- |
| **Happy Path**     | 9          | Valid inputs, all search methods, formats, units         |
| **Error Handling** | 7          | Authentication (401), Not Found (404), Bad Request (400) |
| **Edge Cases**     | 3          | Case sensitivity, special characters, spaces in names    |
| **Total**          | **19**     | **Comprehensive coverage**                               |

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
- **Version Control:** Git/GitHub
- **Reporting:** Newman HTML Extra

---

## 🚀 How to run the tests

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

### Run Tests via Newman CLI

```bash
newman run collection/"Project 1 - Weather API Testing- OpenWeatherMap.postman_collection" \
  -e OpenWeatherAPI.postman_environment.json \
  -r htmlextra,cli \
  --reporter-htmlextra-export reports/newman-report.html
```

## 📁 Project Structure

```
weather-api-testing/
├── collection/        # Postman collection (API test cases)
├── environment/       # Environment template (API key configurable)
├── documentation/     # Test plan, test cases, traceability, execution summary
├── reports/           # Newman HTML reports
├── screenshots/
└── README.md
```

---

## 🔍 Key Testing Decisions & Learnings

- Validated required fields only to avoid flaky tests caused by optional API fields
- Used tolerance-based assertions for floating-point values (coordinates, temperatures)
- Applied case-insensitive validation for city names and error messages
- Implemented unit-specific temperature range checks
- Reduced duplication using folder-level assertions in Postman
- Focused on risk-based coverage instead of exhaustive enumeration

---

## 📌 Why This Project Matters

This project reflects how API testing is done in practice:

- Clear scope definition
- Meaningful negative testing
- Maintainable assertions
- Automation-ready execution
- Documentation that supports, not overwhelms

## Technical Skills Demonstrated

- ✅ Risk-based API test design
- ✅ JavaScript test scripting in Postman
- ✅ Newman CLI automation
- ✅ HTML report generation
- ✅ Git/GitHub version control

---

## 📞 Contact

**Renuka**

- 💼 LinkedIn: www.linkedin.com/in/renukaporje
- 📧 Email: renuka.suresh224@gmail.com
- 🌐 Portfolio:

---

## Acknowledgments

- **OpenWeatherMap** for providing the free API
- **Postman** for the excellent testing platform
- **Newman** for CLI automation capabilities

---

**⭐ If you find this project helpful, please consider giving it a star!**
