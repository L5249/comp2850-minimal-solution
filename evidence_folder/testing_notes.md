# Testing Notes — Week 7 Lab 1

## HTMX Path
**Date**: [2025-11-17]
**Browser**: Chrome 120.0
**JavaScript**: Enabled

### Test: Inline edit activation
- **Action**: Clicked "Edit" button
- **Result**: ✅ Form appeared instantly (no page reload)
- **Network**: GET /tasks/1/edit (AJAX, 45ms)
- **Screenshot**: `01-view-mode-htmx.png`, `02-edit-mode-htmx.png`

### Test: Validation error
- **Action**: Deleted title, clicked "Save"
- **Result**: ✅ Error shown: "Title is required..."
- **ARIA**: `<p id="error-1" role="alert" aria-live="assertive">` confirmed in DevTools
- **Screenshot**: `03-validation-error-htmx.png`

### Test: Successful save
- **Action**: Entered valid title, clicked "Save"
- **Result**: ✅ View mode restored, status = "Task 'New title' updated successfully."
- **Screenshot**: `04-status-oob-devtools.png`

---

## No-JS Path
**Date**: [2025-11-17]
**Browser**: Chrome 120.0
**JavaScript**: Disabled

### Test: Edit activation
- **Action**: Clicked "Edit" button
- **Result**: ✅ Full page reload, form shown
- **URL**: http://localhost:8080/tasks/1/edit

### Test: Validation error
- **Action**: Deleted title, clicked "Save"
- **Result**: ✅ Redirect to /tasks/1/edit?error=blank, error shown
- **Screenshot**: `05-edit-mode-nojs-error.png`

---

## Keyboard Testing
**Date**: [2025-11-17]
**Input**: Keyboard only (no mouse)

### Test: Tab navigation
- **Path**: Tab → "Edit" → Enter → Title input (autofocus) → Tab → "Save" → Enter
- **Result**: ✅ Focus order logical, all buttons reachable
- **Focus indicators**: ✅ Visible outline on all elements

---

## Issues Found
None. All tests passed.

## WCAG Compliance Check
| Criterion | Status | Evidence |
|-----------|--------|----------|
| 2.1.1 Keyboard (A) | ✅ Pass | All features accessible via Tab/Enter |
| 3.3.1 Error Identification (A) | ✅ Pass | Error message explicit, aria-describedby links input |

