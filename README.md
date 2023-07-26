# lab-agile-planning

## About:
This repository serves as a comprehensive lab for exploring and implementing agile planning methodologies in the context of DevOps. It primarily focuses on showcasing the effective utilization of the ZenHub tool for planning purposes. Through this lab, users can gain hands-on experience and insights into how agile principles can be seamlessly integrated with DevOps practices. By leveraging ZenHub's powerful planning features, teams can efficiently manage their workflows, enhance collaboration, and streamline the software development process for improved productivity and outcomes.

## Procedures:
- Install the chrome extension for zenhub, create an account and link account to github account. These will establish the zenhub tab on all repos. Click on the tab to create a zenhub worskspace for the repo.
- Create an issue template from the settings tab of your repo. Titled - User stories. Using this template :
  ```
   **As a** [role]  
   **I need** [function]  
   **So that** [benefit]  
   
   ### Details and Assumptions
   * [document what you know]
   
   ### Acceptance Criteria  
   
   ```gherkin
   Given [some context]
   When [certain action is taken]
   Then [the outcome of action is observed]
   ```
  this will be a guide for user stories for raising issues in your zenhub.
- Next, create issues. Using github issues or the a 'new github issues' tab on the top right of the zenhub board, you can add issues by selecting the user stories template, and adding issues/stories by updating the template. An Example :
  ```
  **As a** [User]  
   **I need** [a service that has a counter]  
   **So that** [i can keep tabs of how many times something was done]  
   
   ### Details and Assumptions
   * [The counter service should have a user-friendly interface for easy interaction.
      The counter should be able to handle positive integer values to represent the count.]
   
   ### Acceptance Criteria  
   
   ```gherkin
   Given I am a User
   When I access the counter service
   Then I should see a counter initialized to zero.
  
   ```gherkin
   Given I have performed a task
   When I increment the counter by one
   Then the counter should reflect the updated count.
  
   ```gherkin
   Given the counter has a non-zero value
   When I reset the counter
   Then the counter should be set back to zero.
  ```
- Sort these issues moving them to the icebox for storing long-term tasks that are not actively being worked on, and the product backlog is for keeping track of all tasks planned for the recent future.
- Always groom and re-order the backlog according to importance or buisness relevance. it's the product owner's responsibility to maintain a groomed backlog and you start refinement by triaging new issues.
- Add labels to relevant issues accordingly by clicking on the issues and clicking labels.
