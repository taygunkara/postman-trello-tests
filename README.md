# Trello API Automation Project

<a href="https://rest-assured.io/"><img src="https://miro.medium.com/v2/1*QOx_tPV5wJnhTzAGhfIiLA.png" width="350" alt="Postman"/></a>


Welcome to the Trello API Automation Project! This project showcases automated testing for Trello's API using Postman and Newman. This repository includes various scripts and tests that ensure the robustness and reliability of Trello's API endpoints.


## Table of Contents
- [Overview](#overview)
- [Project Structure](#project-structure)
- [Setup Instructions](#setup-instructions)
- [Dependencies](#dependencies)
- [Usage](#usage)
- [Running Tests with Newman](#running-tests-with-newman)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

This project contains a Postman collection and environment settings designed to test Trello's API functionalities. It includes comprehensive test cases for creating, updating, and managing Trello boards, lists, cards, checklists, and labels.

### Key Features
- Automated tests for Trello API endpoints
- Environment management for different API configurations
- Randomized data generation for test cases
- Comprehensive response validations and assertions

## Project Structure

The repository is organized as follows:

```
postman-trello-tests/ 
├── workspace-globals.json 
├── trello-environment.json 
├── trello-collection.json 
├── newman/ 
│ ├── trello.xml 
├── result.png 
├── README.md
├── LICENSE
```

- `workspace-globals.json`: Global variables for Postman, including API keys and tokens.
- `trello-environment.json`: Environment-specific variables for Trello API endpoints.
- `trello-collection.json`: Postman collection containing all the API requests and tests.
- `newman/trello.xml`: Newman report in JUnit format.
- `result.png`: Sample result screenshot from the terminal.

## Setup Instructions

To get started with this project, follow these steps:

1. **Clone the repository**:  
    ```bash
    git clone https://github.com/taygunkara/postman-trello-tests.git
    cd postman-trello-tests
    ```

2. **Install Postman** (optional but recommended):  
    Download and install Postman from the [official website](https://www.postman.com/downloads/).

3. **Import the Collection and Environment** (if using Postman):  
    - Open Postman.
    - Click on the `Import` button.
    - Select `trello-collection.json` to import the collection.
    - Select `trello-environment.json` to import the environment.

4. **Configure Environment Variables**:  
    - Ensure that the `trelloKey` and `trelloToken` variables in `workspace-globals.json` are correctly set with your Trello API key and token.
    - Update any other environment variables as necessary.

## Dependencies

To run the tests using Newman, ensure you have the following dependencies installed:

- [Node.js](https://nodejs.org/) (which includes npm)
- Newman

Install Newman globally using npm:

```bash
npm install -g newman
```

## Usage

Once the setup is complete, you can run the tests:

1. **Select the Environment** (if using Postman):
    - In Postman, select the `Trello Environment` from the environment dropdown.
2. **Run the Collection** (if using Postman):
    - Go to the `Collections` tab.
    - Click on the `Trello APIs` collection.
    - Click on the `Run` button to execute all the test cases.
3. **Review the Results**:
    - Postman will display the test results, indicating the success or failure of each test case.

## Running Tests with Newman

You can also run the tests using Newman, which is a command-line collection runner for Postman. This allows you to run Postman collections directly from the command line.

1. **Navigate to the Project Directory**:

```bash
cd postman-trello-tests
```

2. **Run the Collection with Newman**:

```bash
newman run trello-collection.json \
  -e trello-environment.json \
  -g workspace-globals.json \
  -r cli,junit \
  --reporter-junit-export "newman/trello.xml"
```

3. **Review the Results**:
	- Newman will display the test results in the command line, showing detailed information about each request and response.
	- A JUnit report will be generated in the `newman` directory as `trello.xml`.

## Contributing
Contributions are welcome! If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
For any inquiries or further information, please contact me at:
- [Email](mailto:kara.taygun@gmail.com)
- [LinkedIn](https://www.linkedin.com/in/taygunkara/) 
