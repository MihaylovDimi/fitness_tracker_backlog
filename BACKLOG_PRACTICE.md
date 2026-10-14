# FitnessTracker MVP: Practice Backlog

## Definition of Done

A user story is only "Done" when every point below is true.

1. All unit tests pass.
2. Code is refactored (Boy Scout Rule applied): it is left cleaner than it was found.
3. Every acceptance criterion of the story has been checked and met.
4. Documentation (README and design rationale) is updated to reflect the change.
5. The change has been reviewed by another developer and merged into `main`.

## User Stories

Ordered by priority (Product Owner).

### User Story 1: Log a Run
**Story:** As a runner, I want to log a run with its distance and duration, so that I can keep a record of my training.
**Estimate:** 3 Story Points.
**Acceptance Criteria:**
* A run with a distance in kilometres and a duration in minutes is saved.
* A distance of zero or below is rejected with a clear error message.
* A saved run appears in the run history with the date it was logged.

### User Story 2: Set a Weekly Goal
**Story:** As a runner, I want to set a weekly distance goal, so that I stay motivated to train regularly.
**Estimate:** 2 Story Points.
**Acceptance Criteria:**
* A goal can be set as a positive number of kilometres.
* Setting a new goal for the same week replaces the previous one.
* The current goal is shown on the home screen.

### User Story 3: View Weekly Progress
**Story:** As a runner, I want to see my total distance this week compared with my goal, so that I know whether I am on track.
**Estimate:** 5 Story Points.
**Acceptance Criteria:**
* The total distance of all runs from Monday to Sunday of the current week is shown.
* Progress is shown as a percentage of the weekly goal.
* A week with no runs shows 0 km and 0%, not an error.
* When the total reaches the goal, the goal is marked as achieved.

## Estimation Rationale

Story points measure relative complexity, not time.

* **Set a Weekly Goal (2)** is the smallest: it stores one number and replaces it when a new one is set.
* **Log a Run (3)** is bigger: it saves several fields, validates input and must show the run in a history list.
* **View Weekly Progress (5)** is the biggest: it depends on both other stories, has to calculate totals across a week and must handle edge cases such as an empty week.

**Priority:** Log a Run comes first because nothing else works without run data. Set a Weekly Goal comes second, and View Weekly Progress last, because it depends on both.

## Optional Challenge: Splitting the Largest Story

View Weekly Progress (5 points) can be split into two smaller, independent stories:

### User Story 3a: See Weekly Distance Total
**Story:** As a runner, I want to see the total distance I have run this week, so that I can see how much training I have done.
**Estimate:** 2 Story Points.

### User Story 3b: See Goal Achievement
**Story:** As a runner, I want to see what percentage of my weekly goal I have reached, so that I know how much is left.
**Estimate:** 3 Story Points.

Splitting the story helps the team keep a sustainable pace. Each part is small enough to finish within a few days, so the team delivers working software sooner and gets feedback earlier, instead of carrying one large, risky item across the whole sprint.
