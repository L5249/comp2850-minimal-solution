## Task T1: Filtering Tasks 

**Scenario**:
"There is a large jumbled list of tasks that need filtering to find all tasks that contain the word "treasure". Use filter to search for "treasure" and report how many tasks are left.

**Setup**:
- I will add 20 tasks to the task list and have the word "treasure" in 5 of them.
- Example of tasks: "The treasure is buried here", "It's on the island", "Look under the palm tree to find the treasure".. and 12 more including 3 more contain the word "treasure".

**Success Criteria**:
- Participant can fuse the filter box and types "treasure"
- Participant reports 5 tasks containing "treasure"
- The participant completes the task in under 90 seconds
- There are no validation errors

**Metrics**:
- Time for page to load to the user saying how many tasks are left
- Completion(0= fail 0.5=partial 1=success)
- A count of validation errors
- A confidence rating on how easy it was for the user to complete the task. (1-5)

**Accessibility checks**:
- Is it possible without keyboard completion?
- Does it work with JS disabled?

---

## Task T2: Adding Tasks Twice in a Row

**Scenario**:
- "There is no task in the list at the moment. Add two new tasks in a row: first 'Buy milk', then 'put the washing on'."

**Setup**:
- Task list starts empty.
- Tell participant each task that needs to be added

**Success Criteria**:
- Participant can find and use the add task form.
- They successfully add both tasks to the list
- Both tasks are visible in the task list at the end.
- Task is completed in 90 seconds
- There are no validation errors (e.g. no blank titles submitted).

**Metrics**:

- Time from participant seeing the add task box to both tasks being added
- Completion (0 = fail, 0.5 = partial, 1 = success).
- A count of validation errors.
- A confidence rating on how easy it was for the user to complete the task (1–5).

**Accessibility checks**:
- Is it possible without mouse interaction (keyboard-only completion)?
- Does it work with JS disabled?

---

## Task T3: Editing an Existing Task

**Scenario**:
- "The task before you just added, 'Buy milk' in the list, this is wrong and you must buy 'oat milk'. Edit the task so that it says 'Buy oat milk' and confirm the change."

**Setup**:
- Task list already contains at least one task with the exact title Buy milk.

**Success Criteria**:
- Participant finds the Buy milk task in the list.
- Participant successfully enters the edit section of that task.
- Participant changes the text to Buy oat milk.
- The new updated title is now visible on the card
- The participant completes the task in under 90 seconds.
- There are no validation errors (e.g. not saving a blank title).

**Metrics**:
- Time from page load to the updated task title being visible in the list.
- Completion (0 = fail, 0.5 = partial, 1 = success).
- A count of validation errors.
- A confidence rating on how easy it was for the user to complete the task (1–5).

**Accessibility checks**:
- Is it possible without mouse interaction (keyboard-only completion)?
- Does it work with JS disabled?

--- 

## Task T4: Deleting a Task

**Scenario**:
- "There is a task in the list called 'Delete me'. Remove this task from the list using the delete button."

**Setup**:
- Task list already contains a task with the title Delete me.
- List is populated with a few more tasks so user can see this is specifically the task to remove.

**Success Criteria**:
- Participant finds the Delete me task in the list.
- Participant deletes the task
- The Delete me task disappears from the list after its deleted
- Other tasks remain visible.
- The participant completes the task in under 60 seconds.
- There are no validation errors.

**Metrics**:
- Time from page load to the Delete me task no longer appearing in the list.
- Completion (0 = fail, 0.5 = partial, 1 = success).
- A count of validation errors.
- A confidence rating on how easy it was for the user to complete the task (1–5).

**Accessibility checks**:
- Is it possible without mouse interaction (keyboard-only completion)?
- Does it work with JS disabled?

---

**Suggested Order To Complete**:
- Warmup
- T2
- T1
- T3
- T4 
- Debrief

---

## Notes for Facilitator

- **Do not help** unless participant is completely stuck (>3 min). Note as "facilitated" in observations.
- **Think-aloud optional**: Ask participants to narrate their thoughts if comfortable. Don't force.
- **Keyboard-only**: Offer keyboard-only variant to 1-2 participants for comparison.
- **No-JS**: Test at least 1 participant with JS disabled to verify parity.

---

## Success Definitions

**Completion codes**:
- `1` = Task fully completed, correct outcome
- `0.5` = Partial completion (e.g., found filter but wrong count)
- `0` = Failed or abandoned

**Time bounds**:
- T1: 90s
- T2: 90s
- T3: 90s
- T4: 60s

If participant exceeds time, prompt: "Would you like to continue, or shall we move to the next task?"
