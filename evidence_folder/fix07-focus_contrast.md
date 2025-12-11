# Fix 09: Delete Button Contrast (WCAG 1.4.3)

**Backlog ID**: 7
**WCAG Criterion**: 1.4.3 Contrast (Minimum, Level AA)
**Priority**: 9 (highest)

---

## Problem Statement
#0172AD on #181C25 = 3.25:1 contrast ratio
**Fails**: WCAG AA requires 4.5:1 for normal text.

**Evidence**:
- WebAIM Contrast Checker: 3.25:1 (Fail AA)
- Screenshot: `contrast-before.png`

---

## Target State
Contrast ratio ≥ 4.5:1 (AA) or ≥ 7:1 (AAA).

---

## Solution
Change colour to have a much larger contrast


---

## Implementation

### Before (Current CSS)
No code 

## After 
in base.peb 

:focus {
    outline: 3px solid #000;     
    outline-offset: 4px;
    }