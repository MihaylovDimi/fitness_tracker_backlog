# FitnessTracker MVP: Practice Backlog

## Definition of Done

A user story is only "Done" when every point below is true.

1. All unit tests pass.
2. Code is refactored (Boy Scout Rule applied): it is left cleaner than it was found.
3. Every acceptance criterion of the story has been checked and met.
4. Documentation (README and design rationale) is updated to reflect the change.
5. The change has been reviewed by another developer and merged into `main`.

## User Stories

### User Story 1: Log a Run
**Story:** As a runner, I want to log a run with its distance and duration, so that I can keep a record of my training.
**Acceptance Criteria:**
* A run with a distance in kilometres and a duration in minutes is saved.
* A distance of zero or below is rejected with a clear error message.
* A saved run appears in the run history with the date it was logged.

### User Story 2: Set a Weekly Goal
**Story:** As a runner, I want to set a weekly distance goal, so that I stay motivated to train regularly.
**Acceptance Criteria:**
* A goal can be set as a positive number of kilometres.
* Setting a new goal for the same week replaces the previous one.
* The current goal is shown on the home screen.

### User Story 3: View Weekly Progress
**Story:** As a runner, I want to see my total distance this week compared with my goal, so that I know whether I am on track.
**Acceptance Criteria:**
* The total distance of all runs from Monday to Sunday of the current week is shown.
* Progress is shown as a percentage of the weekly goal.
* A week with no runs shows 0 km and 0%, not an error.
* When the total reaches the goal, the goal is marked as achieved.
