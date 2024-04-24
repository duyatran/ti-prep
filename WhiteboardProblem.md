### Get Employees by Department (Arrays Practice)
You are working on a Node.js application that manages a list of employees in a company. The employee data is represented as an array of arrays, where each inner array contains information about an employee. The inner array follows the format `[name, position, department]`.

Your task is to implement a function that retrieves all the employees in a specific department from the employee data array.

Write a function called `getEmployeesByDepartment` that takes two parameters: `employees` (the array of employee data) and `department` (the department name). The function should return an array of employees who belong to the specified department.

Here are the requirements for the function:

1. The employees array contains multiple inner arrays, where each inner array represents an employee and contains three elements: `name`, `position`, `and` department. For example: `['John Doe', 'Software Engineer', 'Engineering']`.
2. The function should search through the `employees` array and extract all the employees who belong to the specified department.
3. The function should return an array of employee names who belong to the specified department.
4. If there are no employees in the specified department, the function should return an empty array.
5. The function should not modify the original employees array.
6. Your task is to implement the `getEmployeesByDepartment` function according to the requirements.

Here is an example data-set,

```
const employees = [
  ['John Doe',     'Software Engineer', 'Engineering'],
  ['Jane Smith',   'Product Manager',   'Product'],
  ['Mike Johnson', 'Sales Executive',   'Sales'],
  ['Emily Brown',  'HR Coordinator',    'Human Resources'],
  ['David Lee',    'Quality Assurance', 'Engineering']
];
```

// Alternative approach: `Arrays.map`
function getEmployeesByDepartment(employees, departmentName) {
  // TODO: edge cases
  const resultEmployees = [];
  if (!employees) {
    return resultEmployees;
  }

  for (const employee of employees) {
    const employeeDepartment = employee[2];

    if (employeeDepartment === departmentName) {
      const employeeName = employee[0];
      resultEmployees.push(employeeName);
    }
  }

  return resultEmployees;
}

const engineeringEmployees = getEmployeesByDepartment(employees, 'Engineering');
console.log('Engineering Employees:', engineeringEmployees);
// Output: ['John Doe', 'David Lee']


- Ask questions to interviewers
  - (Examples of inputs and outputs)
  - Inputs: `employees`, `department` (string)
  - Output: an array of employees who belong to the specified department
  - Format
  - Edge cases: [], undefined, null

- Discuss the problem and potential approaches with interviewer
  - Think aloud
  - Say "we" not "I"
  - Start with whatever approach comes to your mind

- Solving the problem
  - Start with input/outputs
  - pseudo-code

- Test your code
```
const engineeringEmployees = getEmployeesByDepartment(employees, 'Engineering');
console.log('Engineering Employees:', engineeringEmployees);
// Output: ['John Doe', 'David Lee']

const salesEmployees = getEmployeesByDepartment(employees, 'Sales');
console.log('Sales Employees:', salesEmployees);
// Output: ['Mike Johnson']

const marketingEmployees = getEmployeesByDepartment(employees, 'Marketing');
console.log('Marketing Employees:', marketingEmployees);
// Output: []
```


