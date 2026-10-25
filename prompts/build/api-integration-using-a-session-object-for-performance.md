---
title: "API Integration: Using a Session Object for Performance"
slug: api-integration-using-a-session-object-for-performance
stage: Build
category: "LLM & AI Integration"
grade: A
score: 85
difficulty: Beginner
hand_reviewed: false
url: https://buildersprompt.com/prompts/api-integration-using-a-session-object-for-performance
---
# API Integration: Using a Session Object for Performance

Compare the execution speed of standard Python requests versus session-based requests to demonstrate the performance benefits of TCP connection reuse.

## Prompt

As a Python developer making frequent calls to the same API host, you notice that your application can be slow. This is because each `requests.get()` or `requests.post()` call may establish a new TCP connection, which adds overhead.

Your task is to write a Python script that demonstrates the performance benefit of using a `requests.Session` object, which reuses the underlying TCP connection for multiple requests to the same host.

**Scenario:**
- You will make 5 consecutive GET requests to `http://httpbin.org/get`.
- You will do this twice: once without a Session object, and once with a Session object.

**Technical Requirements:**
- Use the 'requests' and 'time' libraries.
- **Part 1 (Without Session):**
    -   Record the start time.
    -   Write a `for` loop that runs 5 times.
    -   Inside the loop, call `requests.get('http://httpbin.org/get')`.
    -   Record the end time and print the total duration.
- **Part 2 (With Session):**
    -   Record the start time.
    -   Create a `requests.Session()` object.
    -   Write a `for` loop that runs 5 times.
    -   Inside the loop, call `session.get('http://httpbin.org/get')`.
    -   Record the end time and print the total duration.
- **Conclusion:** Add a print statement explaining that the duration with the Session object should be shorter because it avoids the overhead of creating a new connection for each request (due to HTTP Keep-Alive).

**Output Format:**
A complete, executable Python script that performs this comparison and prints the timing results.
