# Event Logging 

- Event: contrast_mode_changed
- Why log it: to check how often and when high contast mode is actually being used.
- Fields to capture: ts_iso,session_id,previous_mode,new_mode,js_mode

---

- Event: task_action_confirmed
- Why log it: to check if the user actually sees feeback when the action is completed
- Fields to capture: ts_iso,session_id,task_id,action_type,js_mode

---

- Event: task_action_unconfirmed
- Why log it: to check if the user tried to complete an action but it didn't actually work 
- Fields to capture: ts_iso,session_id,task_id,action_type,error_flag,js_mode

---


## Events to Log

### 1. Task Created
**Trigger**: User toggles contrast mode
**Fields**:
- ts_iso: ISO timestamp (e.g., 2025-01-15T14:23:45Z)
- session_id: Anonymous 6-char hex (e.g., P2_b9c1)
- request_id: Unique per toggle event
- event_code: E1_contrast_toggle
- prev_mode: light | dark | high-contrast
- new_mode: light | dark | high-contrast
- device_type: mobile | desktop
- js_mode: js-on | js-off

**Why**: Measuring how often users switch modes, and to compare wo what time of day they do it to see if its within sunlight hours 

### 2. Task action confirmed
**Trigger**: System shows confirmation after adding/editing/deleting a task
**Fields**: 
- ts_iso: ISO timestamp
- session_id: Anonymous per participant
- request_id: Unique per action
- event_code: E3_action_confirmed
- task_id: Internal UUID
- action_type: add | edit | delete
- confirmation_type: toast | aria-live | vibration
- js_mode: js-on | js-off

**Why**: To align with S5, it must always show to reduce the annoying double checking

### 3. Task action unconfirmed
**Trigger**: Task action happens but no confirmation is actually displayed
**Fields**:
- ts_iso: ISO timestamp
- session_id: Anonymous per participant
- request_id: Unique per action
- event_code: E4_action_unconfirmed
- task_id: Internal UUID
- action_type: add | edit | delete
- error_flag: missing_confirmation
- js_mode: js-on | js-off

**Why**: Must be measured becasue failures can increase cognitive load making it let accessible for users with ADHD, memory impairment or anxiety

## Data Storage
- **Format**: CSV (human-readable, easy to analyse in Excel/Google Sheets)
- **Location**: `data/metrics.csv` (local file, not cloud)
- **Schema**:
  ```csv
    ts_iso,session_id,request_id,event_code,prev_mode,new_mode,device_type,js_mode
    ts_iso,session_id,request_id,event_code,task_id,action_type,confirmation_type,js_mode
    ts_iso,session_id,request_id,event_code,task_id,action_type,error_flag,js_mode

## Example Rows 

```csv
    2025-01-15T14:26:30Z,P3_c9a1,req_004,E1_contrast_mode_changed,light,high-contrast,desktop,js-on
    2025-01-15T14:27:12Z,P3_c9a1,req_005,E3_action_confirmed,task_241,add,toast,js-on
    2025-01-15T14:28:01Z,P4_d1f3,req_006,E4_action_unconfirmed,task_089,delete,missing_confirmation,js-off


