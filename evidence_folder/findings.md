# Pilot Findings Analysis — Week 9

**Participants**: 3 (2 HTMX, 1 No-JS)  
**Date**: 2025-12-11

---

## Quantitative Summary

### Task 1: Filter Tasks
| Metric | HTMX (n=2) | No-JS (n=1) | Overall |
|--------|------------|-------------|---------|
| Mean time (s) | 12.8 | 49.5 | 25 |
| Success rate | 100% | 100% | 100% |
| Mean errors | 0 | 0 | 0 |
| Mean confidence | 4.0/5 | 3.0/5 | 3.67/5 |

**Interpretation**:  
The filtering worked all round. HTMX worked better becasue the page didn't reload every time.  

---

### Task 2: Add New Task (Twice)
| Metric | HTMX (n=2) | No-JS (n=1) | Overall |
|--------|------------|-------------|---------|
| Mean time (s) | 18 | 27.5 | 21 |
| Success rate | 100% | 100% | 100% |
| Mean errors | 0 | 0 | 0 |
| Mean confidence | 4/5 | 3/5 | 3.67/5 |

**Interpretation**:  
Everyone added tasks successfully, but there was no confirmation message which caused uncertainty.

---

### Task 3: Edit Task
| Metric | HTMX (n=2) | No-JS (n=1) | Overall |
|--------|------------|-------------|---------|
| Mean time (s) | 18.5 | 58 | 29 |
| Success rate | 100% | 100% | 100% |
| Mean errors | 0 | 0 | 0 |
| Mean confidence | 3/5 | 2/5 | 2.5/5 |

**Interpretation**:  
Editing works but participants always needed to check if things had actually saved, due to no message. Also, edit did not work with no-js

---

### Task 4: Delete Task
| Metric | HTMX (n=2) | No-JS (n=1) | Overall |
|--------|------------|-------------|----------|
| Mean time (s) | ~11 | 39 | ~23 |
| Success rate | 100% | 100% | 100% |
| Mean errors | 0 | 0 | 0 |
| Mean confidence | 3/5 | 3/5 | 3/5 |

**Interpretation**:  
Delete always worked, however the participants had to double check the list after becasue there was no confirmation.


---

## Qualitative Themes

### Theme 1: Confirmation Feedback
**Evidence**: All 3 participants mentioned needing confirmation for adding, deleting and editing tasks.

**Quotes**:
(after asking them a question related to the confirmation feedback)
- **P1**: “I didn’t notice anything happen.”
- **P2 (No-JS)**: “I wasn’t sure it worked at first.”
- **P3 (Keyboard-only)**: “I didn’t see any pop up or message.”

**Design implication**:  
Add explicit confirmation messages for add/edit/delete.

---

### Theme 2: Edit Uncertainty
**Evidence**: Confusion across all modes.

**Quotes**:
(both from during study)
- **P2**: “Edit kind of doesn’t work in no JS”
- **P3**: “Edit feels invisible unless you check manually.”

**Design implication**:  
Surface a clear “Task updated” message.

---

### Theme 3: Keyboard Access Strong (but slow)
**Evidence**: Keyboard-only participant succeeded all tasks.

**Quotes**:
- "tab order worked great"

**Design implication**:  


---

## Accessibility Observations

### Keyboard Navigation
- All features reachable  
- Focus visibly indicated  
- Success states not announced  

---

## Prioritised Issues

1. **High** — Missing confirmation messages  
   - Affects all participants  
   - Causes low confidence for add/edit/delete

2. **Medium** — Edit uncertainty  
   - Users unsure changes saved  
   - Particularly bad with no-JS

3. **Medium** — No-JS “jumpy” behaviour  
   - Slow page reload perception  
   - No visible feedback


---

