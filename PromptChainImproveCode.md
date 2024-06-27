# AI-Assisted Code Refinement

### Description
This prompt chain will review a piece of code (it it tailored now to C# code, but with little adjustment it can also work with other languages), reflect on it's review and rewrite the code. It is inspired by this awesome prompt chain (https://github.com/PickleBoxer/dev-chatgpt-prompts?tab=readme-ov-file#-a-multi-prompt-approach-prompt-chaining)

### Step 1: Review the code
```
Conduct a thorough review of the provided code, focusing on identifying logical concerns and potential issues. Your task is to analyze the code critically and provide a comprehensive list of recommendations for improvement without rewriting the code. Please adhere to the following guidelines:

   - Examine the overall logic and flow of the code.
   - Identify any potential logical errors, edge cases, or boundary conditions that may not be properly handled.
   - Check for off-by-one errors, infinite loops, or incorrect conditional statements.
   - Evaluate the efficiency of the implemented algorithms.
   - Identify any areas where time or space complexity could be improved.
   - Suggest alternative approaches if a more efficient algorithm exists for the problem at hand.
   - Assess the robustness of error handling mechanisms.
   - Identify potential null reference exceptions or unhandled exceptions.
   - Check if all possible input scenarios are properly handled.
   - If applicable, review the code for potential race conditions or deadlocks.
   - Ensure proper synchronization mechanisms are in place for shared resources.
   - Identify any potential security vulnerabilities, such as SQL injection, cross-site scripting (XSS), or improper input validation.
   - Check for any hardcoded sensitive information like passwords or API keys.
   - Look for potential performance bottlenecks or resource-intensive operations.
   - Identify areas where caching or lazy loading could be beneficial.
   - Consider how well the code would scale with increased data or user load.
   - Identify any potential scalability issues in the current implementation.
   - Assess how easily the code can be unit tested.
   - Suggest ways to improve testability without rewriting the code.
   - Identify any repeated code that could be refactored into reusable functions or methods.
   - Suggest opportunities for improving code modularity and reusability.
   - While not rewriting the code, suggest improvements for variable, method, or class names that could enhance readability.
   - Identify areas where additional comments might be beneficial for understanding complex logic.

Please provide your recommendations in a clear, prioritized list format. For each recommendation:
- Briefly describe the concern or issue.
- Explain why it's important to address.
- Suggest a high-level approach to resolve the issue without providing specific code rewrites.

The code:
[insert code here]
```

### Step 2: Self-review
```
Conduct a comprehensive self-review of your previous recommendations. Your task is to critically analyze your initial assessment, identifying potential oversights, biases, or areas for improvement. Please adhere to the following guidelines:

   - Identify any assumptions you made in your initial review that may have influenced your recommendations.
   - Consider how these assumptions might have led to overlooked issues or incorrect conclusions.
   - Reflect on whether you fully understood the context of the code and its intended purpose.
   - Assess if any recommendations were made without considering the broader system architecture or project constraints.
   - Examine your recommendations for potential cognitive biases (e.g., confirmation bias, anchoring bias).
   - Consider how your personal experiences or preferences might have influenced your initial review.
   - Compare your recommendations against current industry best practices and standards.
   - Identify any areas where your suggestions might deviate from widely accepted best practices in software development.
   - Consider any recent technological advancements or updates in the programming language or framework used.
   - Assess if any of your recommendations are outdated or could be improved based on new features or methodologies.
   - Reevaluate your assessment of performance and scalability concerns.
   - Consider if you overlooked any potential bottlenecks or scalability issues in the original code.
   - Reflect on whether you adequately addressed all potential security vulnerabilities.
   - Identify any security best practices that might have been overlooked in your initial review.
   - Reassess your recommendations regarding code structure and organization.
   - Consider if your suggestions truly enhance the long-term maintainability and readability of the code.
   - Evaluate whether your recommendations adequately addressed testability and quality assurance concerns.
   - Identify any overlooked opportunities for improving test coverage or implementing better testing strategies.
   - Consider alternative approaches or solutions that you might have overlooked in your initial review.
   - Assess whether any of your recommendations could be replaced with more effective or efficient alternatives.
   - Reevaluate the prioritization of your recommendations.
   - Consider if you accurately assessed the potential impact and effort required for each suggestion.
   - Reflect on whether you covered all aspects of the code in your initial review.
   - Identify any areas or components of the code that might have been overlooked or not given sufficient attention.

For each point of self-criticism or newly identified issue:
- Clearly state what was overlooked, incorrectly assessed, or could be improved in your initial review.
- Explain the reasoning behind your self-criticism, referencing relevant software development principles or best practices.
- Suggest how your initial recommendation could be modified or what new recommendation should be added to address the identified shortcoming.

Remember, the goal of this self-review is not to completely rewrite your initial recommendations or the original code, but to demonstrate critical thinking, self-awareness, and a commitment to continuous improvement in software development practices.

Please provide your self-review based on these guidelines, focusing on constructive self-criticism and actionable insights for improvement.
```

### Step 3: Rewrite the code (optinally, you can split this up further if it is very complex code or if there are many recommendations)
```
Rewrite the provided code based on your previous review and recommendations. Your task is to implement the suggested improvements while adhering to best practices in code refactoring and software development. Please follow these guidelines:

  - Begin with the most critical issues identified in your review, such as logical errors, security vulnerabilities, or performance bottlenecks.
  - Implement changes that provide the most significant impact on code quality, readability, and maintainability.
  - Ensure that the rewritten code preserves the original functionality unless explicitly recommended otherwise in your review.
  - Use meaningful and consistent naming conventions for variables, methods, and classes.
  - Break down complex methods into smaller, more manageable functions.
  - Add or improve comments and documentation where necessary, focusing on explaining 'why' rather than 'what'.
  - Implement any performance optimizations suggested in your review.
  - Enhance error handling mechanisms as per your recommendations.
  - Address any edge cases or boundary conditions identified in the review.
  - Leverage modern features of the programming language (e.g., C# 12.0 features if applicable) to enhance code quality and efficiency.
  - Eliminate any redundant code through appropriate abstraction or the use of design patterns.
  - Ensure the rewritten code follows the project's or industry-standard coding conventions.

  Respond with the rewritten code in one continuous code block, only output the rewritten code without any further comments and remarks.
```
