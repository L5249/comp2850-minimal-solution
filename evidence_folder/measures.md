## Objective Metrics (Week 9 Pilot)

---

1. Completion Rate
**Definition**: 
- Proportion of participants who successfully complete each task.

**Calculation**: 
- completion_rate = (# successes) / (# attempts)

**Data source**: 
- Manual observation
- Server logs (outcome=success in metrics.csv)

**Reporting**:
- Percentage per task (e.g., “T2: 5/5 = 100%”)

**Split by**:
- JS-on vs JS-off
- Keyboard-only vs mouse

---

### 2. Time-on-Task

**Definition**: Duration from task start to completion or abandonment.

**Calculation**:
- **Server-timed**: `ms` column in metrics.csv (start to success event)
- **Backup**: Facilitator stopwatch (start when participant reads scenario, stop when they say "done")

**Reporting**:
- **Median** (primary): Middle value, resistant to outliers
- **MAD**: Median absolute deviation for spread
- **Range**: Min-max for context

**Example**:
T1 (Filter): Median: 24s MAD: 6s Range: 12s–58s (n=5)


**Split by**: JS-on vs JS-off (expect no-JS to be slower due to full page reloads)

---

### 3. Error Rate

**Definition**: Proportion of attempts that trigger validation errors.

**Calculation**:
Error rate = (# validation_error events) / (# total attempts)


**Data source**: `metrics.csv` where `step=validation_error`

**Reporting**: Percentage per task + qualitative notes on error type

**Example**:
T3 (Add Task): Error rate: 2/5 = 40% Errors: 1× blank title, 1× exceeded max length


**HCI insight**: High error rates → poor affordances, unclear constraints, or accessibility issues

---

### 4. Validation Error Count

**Definition**: Number of validation errors per participant per task.

**Calculation**: Count rows in `metrics.csv` with `step=validation_error` for given session + task

**Reporting**: Mean errors per task

**Example**:
T2 (Edit): Mean errors per participant: 0.4 (2 errors across 5 participants)



---

## Subjective Metrics

### 5. Confidence Rating

**Definition**: Self-reported confidence that task was completed correctly.

**Scale**: 1 (not at all confident) → 5 (very confident)

**Collection method**: Ask immediately after each task:
> "On a scale of 1 to 5, how confident are you that you completed that task correctly?"

**Reporting**:
- Mean + standard deviation
- Distribution (how many rated 1, 2, 3, 4, 5)

**Example**:
T1 (Filter): Mean confidence: 4.2 ± 0.8 Distribution: 0×1, 0×2, 1×3, 2×4, 2×5


**HCI insight**: Low confidence despite successful completion → interface doesn't provide sufficient feedback

---

## Qualitative Observations

### 8. Facilitator Notes

**Capture**:
- Hesitations ("Participant paused 10s before clicking filter")
- Verbalizations ("I'm not sure if it saved")
- Accessibility issues ("Screen reader didn't announce result count")
- Workarounds ("Used Ctrl+F instead of built-in filter")

**Format**: Timestamped notes in `pilot-notes.md`

**Analysis**: Thematic coding in Week 10 (group similar issues, link to backlog items)

---

## Accessibility-Specific Metrics

### 9. Keyboard-Only Completion

**Definition**: Can task be completed using only keyboard (no mouse)?

**Measurement**: Binary per task (yes/no)

**Reporting**: "T1: Keyboard-accessible, passed y" or "T3: Tab order broken, failed n"

---

## Summary Table

| Metric | Type | Source | Calculation | Reporting |
|--------|------|--------|-------------|-----------|
| Completion rate | Objective | Manual + logs | successes / attempts | % per task |
| Time-on-task | Objective | Server logs | Median + MAD | Seconds |
| Error rate | Objective | Server logs | errors / attempts | % per task |
| Confidence | Subjective | Post-task question | Mean ± SD | 1–5 scale |
| Facilitator notes | Qualitative | Manual observation | Thematic coding | Categories |
| KB-only completion | Accessibility | Manual test | Binary | y/n |

