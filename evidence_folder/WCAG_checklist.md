# WCAG 2.2 AA Checklist — Week 7

**Date**: [2025-11-17]
**Scope**: Task manager (add, edit, delete flows)
**Tester**: Lewis Wiles

---

## Perceivable (Principle 1)

### 1.1 Text Alternatives
| Criterion | Level | Status | Evidence | Notes |
|-----------|-------|--------|----------|-------|
| 1.1.1 Non-text Content | A | N/A | The page includes no images | If needed, images will be added later |

### 1.3 Adaptable
| Criterion | Level | Status | Evidence | Notes |
|-----------|-------|--------|----------|-------|
| 1.3.1 Info and Relationships | A | Pass | `<label for="search-query">Filter by title</label>` | Semantic HTML |
| 1.3.2 Meaningful Sequence | A | Pass | Tab order: moves down the page in order| Logical reading order, not a jumbled mess |

### 1.4 Distinguishable
| Criterion | Level | Status | Evidence | Notes |
|-----------|-------|--------|----------|-------|
| 1.4.3 Contrast (Minimum) | AA |  Fail | Delete button #0172AD = 3.25:1 | Needs 4.5:1 (AA) |
| 1.4.11 Non-text Contrast | AA | Fail | Focus outline 3px solid #0F5177 | Not enough contrast |

---

## Operable (Principle 2)

### 2.1 Keyboard Accessible
| Criterion | Level | Status | Evidence | Notes |
|-----------|-------|--------|----------|-------|
| 2.1.1 Keyboard | A | Pass | All features accessible via tabbing, features that can ba clicked acan be done with enter | Tested: add, edit, delete, cancel |
| 2.1.2 No Keyboard Trap | A | Pass | No traps detected | Can Tab out of all forms |

### 2.4 Navigable
| Criterion | Level | Status | Evidence | Notes |
|-----------|-------|--------|----------|-------|
| 2.4.1 Bypass Blocks | A | Pass | Skip link appears on first tab onto the page, jumps to #main | Tested with keyboard |
| 2.4.3 Focus Order | A | Pass | Tab order: Edit → Title → Save → Cancel | Logical sequence |
| 2.4.7 Focus Visible | AA | fail | Pico.css default outline visible, but faint, the colour is blue on blue so needs changing | Consider custom outline (3px solid) |

---

## Understandable (Principle 3)

### 3.2 Predictable
| Criterion | Level | Status | Evidence | Notes |
|-----------|-------|--------|----------|-------|
| 3.2.1 On Focus | A | Pass | No context change on focus | Only explicit button clicks trigger actions |
| 3.2.2 On Input | A | Pass | No auto-submit on input change | Form submits only on button click(mouse or enter) |

### 3.3 Input Assistance
| Criterion | Level | Status | Evidence | Notes |
|-----------|-------|--------|----------|-------|
| 3.3.1 Error Identification | A | Pass | Error: "Title is required. Please enter at least one character." | Specific, actionable |
| 3.3.2 Labels or Instructions | A | Pass | All inputs have `<label>` + hint text | `aria-describedby` links to hint |
| 3.3.3 Error Suggestion | AA | Pass | Error message includes correction hint | "Please enter at least one character" |

---

## Robust (Principle 4)

### 4.1 Compatible
| Criterion | Level | Status | Evidence | Notes |
|-----------|-------|--------|----------|-------|
| 4.1.2 Name, Role, Value | A | Pass | All buttons have accessible names | `aria-label="Edit task: Buy milk"` |


---

## Summary
- **Total criteria evaluated**: 16
- **Pass**: 14
- **Fail**: 2 (1.4.3 Contrast) (2.4.7 focus visible)
- **Partial**:0
- **N/A**: 1

---

## High-Priority Failures
1. **1.4.3 Contrast (Minimum, AA)**: Delete button text fails 4.5:1 ratio
   - **Action**: Change Pico.css button color or add custom CSS

2. **2.4.7 Focus Visible (AA)**: Default outline may be too close to actuall button colour
   - **Action**: Add custom `:focus` styles with way more contrast/larger size

---


