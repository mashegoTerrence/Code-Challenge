# Code-Challenge
**Workflow Management System - Simple Dynamic View Compilation**

In this code challenge, you will be tasked with building a simplified version of a Workflow Management System that can dynamically compile views by retrieving data from JSON structures. The goal is to create a basic system that demonstrates the core functionalities of dynamic view compilation without overwhelming complexity.

**Scenario:**

Imagine you are working with a company that offers a platform for data analysis. The platform allows users to define their own data workflows, where they can specify the data they want to retrieve and display from simple JSON structures.

**Requirements:**

**1. Dynamic View Compilation:** Implement a mechanism to compile dynamic views based on user-defined configurations. Users should be able to specify the data they want to retrieve and display from the complex JSON structures.

**2. Support for Nested Data:** The system should handle deeply nested JSON structures with multiple levels of nesting.

**3. Array Handling:** Extend the solution to support arrays within the JSON structure. Allow users to retrieve values from arrays using dynamic indexing, such as providing the index path (e.g., "data.persons[2].name").

**4.Wildcard Retrieval:** Implement the ability to retrieve all occurrences of a certain key in the JSON structure using wildcards (e.g., "data.*.name" retrieves all "name" values at any level under "data").

**5.Error Handling and Validation:** Implement robust error handling for cases like invalid paths, non-existent keys, or any other potential errors. Provide meaningful error messages to guide users in resolving issues.

**6.Performance Optimization:** Optimize the view compilation algorithm to handle large and deeply nested JSON structures efficiently. Consider ways to reduce redundant traversals and enhance overall performance.

**User-Defined Configurations Example:**
As a user of the Workflow Management System, you can define your view configurations using a simplified JSON-based syntax. Let's look at an example of how you can set up a view configuration:

```json
{
 "sales":{
      "products":[
       
        {
          "date": "2023-01-05",
          "product": "Widget A",
          "product_name":"Product A",
          "quantity": 100,
          "total_price": 500
        },
        {
          "date": "2023-01-06",
          "product": "Widget B",
          "product_name":"Product B",
          "quantity": 150,
          "total_price": 750
        }
      ],
    "total_value":41515

    },
  "view_fields": [
    {
      "field_name": "date",
      "path": "sales.date",
      "data_type": "string"
    },
    {
      "field_name": "product",
      "path": "sales.products[2].product_name",
      "data_type": "string"
    },
    {
    "field_name": "total price",
      "path": "sales.accounts.total_value",
      "data_type": "number"
    },
    {
      "field_name": "All products",
      "path": "sales.*.product_name",
      "data_type": "number"
    }
  ]
}

```

In this example, the user defines a view called “Sales_Report” with data directly provided in the “data_source” object. The view_fields array contains four fields to be retrieved: "date," "product," “quantity,” “total_price” and “all products” The "path” attribute in each field specifies the JSON path to extract the corresponding data. The "data_type" attribute indicates the expected data type for each field.

Your task is to implement the Workflow Management System that can interpret these user-defined configurations and dynamically compile the desired views from the JSON data.
# Guidelines:

1. Implement the Dynamic View Compilation system using TypeScript.
2. Focus on the core functionalities of dynamic view compilation.
4. Prioritize code readability and maintainability, adhering to TypeScript best practices.
5. Be creative in your approach to solving complex problems.
6. Provide clear and detailed documentation explaining how to use the Dynamic View Compilation system and any other relevant information.

