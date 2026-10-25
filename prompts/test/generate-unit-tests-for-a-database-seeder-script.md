---
title: "Generate Unit Tests for a Database Seeder Script"
slug: generate-unit-tests-for-a-database-seeder-script
stage: Test
category: "Testing & QA"
grade: A+
score: 92
difficulty: Advanced
hand_reviewed: false
url: https://buildersprompt.com/prompts/generate-unit-tests-for-a-database-seeder-script
---
# Generate Unit Tests for a Database Seeder Script

Get a complete test file for your database seeder, with setup, teardown, record counts, sample value checks, and idempotency tests.

Variables: language, database_name, seeder_script_code

## Prompt

I have a database seeder script, written in `{{language}}`, that populates our `{{database_name}}` database with initial data. I need to write unit tests to verify that the script correctly inserts the expected data.

**Instructions:**
1.  **Seeder Script:**
    ```{{language}}
    {{seeder_script_code}}
    ```
2.  **Testing Approach:**
    *   Use an in-memory database (e.g., SQLite for testing a SQL database) or a dedicated test database.
    *   The tests should run the seeder script and then query the database to assert that the data was inserted correctly.
    *   The database should be reset to a clean state before each test.
3.  **Test Cases:**
    *   **Data Integrity:** Verify that the correct number of records are inserted into each table.
    *   **Data Correctness:** Check the values of a few sample records to ensure they are correct.
    *   **Idempotency:** Test that running the seeder script multiple times does not create duplicate data or cause errors.
4.  **Output Format:** Provide the complete test file. Include the setup and teardown logic for managing the test database.
