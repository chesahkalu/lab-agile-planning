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
- Always groom and re-order the product backlog according to importance or buisness relevance. it's the product owner's responsibility to maintain a groomed backlog and you start refinement by triaging new 
  issues.
  All these is to get your issues sprint ready. Again, make sure to refine new issues by sorting them as soon as possible.
- Add labels to relevant issues accordingly by clicking on the issues and clicking labels to prepare for sprint meeting.
    * Create new label - 'technical label' on github to flag those stories that provide no visible customer value but must be completed in order to continue development.
    * Add these labels accordingly. Eg- Enhancement labels for issues that would enhance our product.
- Create a sprint: a duration to usually two weeks, to interate and deploy the stories that will be passed to the sprint back-log. This can be created as milestones in both github and zenhub.
- Create a sprint plan: with the meetings and discussions with dev team, you should move a story from the backlog to the sprint backlog, and assign estimates (according to the teams decision are be points 
  used to estimate the difficulty of each story). Also assign one of the sprint durations to the story.
  * The team might have decided that a couple of other stories in the product backlog has less points estimates to fit into this particular activated sprint duration, indicate theese stories by assigning 
    the estimated points and move them to the sprint backlog , assigning them same duration of the first one.
- Sprint planning has been established. Now a couple of stories has been moved to sprint backlog, they must maintain same sprint duration after estimating through the total points that the difficulty of the
  of the stories can be achieved within the sprint duration. This total points should be limited to "Team Velocity"(Velocity is the number of story points that a team can execute in a single sprint). This     could have been determined through various factors such as the team's history, experience and skills.
- Now to execute:
  * team member should take the next item highest on priority on the sprint backlog, inspect the story and if it is one they can work on, assign it to themselves or to someone else.
  * Move the asinged story to in-process and start working on it. Normally by creating a branch of the master on github to work on your code.
  * No one should work on two things at the same time
  * Once you finish working on the story, make a pull request to merge your code into the master branch. Move your story from In Progress to Review/QA for team mates to inspect your work.
  * While waiting for a review, you can start working on another story. Make sure that you have the skills to implement it, assign it to yourself, and move it to In Progress.
  * When your pull request is approved , merged and review complete, Move the story to done.
- Burndown: these is a chart tha shows the story points completed vs. the time left in a sprint. Burndown charts can be used to show progress and forecast the team's probability of achieving the sprint goal 
  By the left corner, on the report option, these chart can be accessed with the current sprint selected.Options at the right top corner of the graph will help teams inspect and monitor their progress, 
  completion status and rate at which they are achieving various task.
- Sprint review: a sprint review is a demonstration of the features that have been implemented during the sprint. Everyone involved with the project is invited to participate, and feedback from stakeholders 
  is critical to help shape the future of the product. Here, the done stories are either accepted or adjusted for new stories for next sprint.
- Sprint retrospective: it measures the health of the process, measures the health of the team,  finds out what works and what doesn't.
- End of sprint:
   * accepted stories that are done should be moved to close.
   * unfinished stories still laying in the product backlog should be dealt with. Don't just move it to the next sprint. We want to adjust the estimate points to take credit for the story points expended so
     that it is reflected in the teams velocity, and create a new story to finish the work in the next sprint. So adjust the estimated points expanded on an unfinished story, move it to close, and create a       new story to address the remaining work giving it the remaining estimated point and move it to the top of the product backlog.
   *  Close the sprint to establish velocity of that sprint, All this will keep velocities accurate for future sprints.
    
