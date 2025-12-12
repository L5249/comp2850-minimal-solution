# Evidence Chains — Week 9

---

## Chain 1: No Confirmation After Actions (All Modes)

**Raw data**:  
P1: “I didn’t notice any confirmation.” (add + delete)  
P2 (No-JS): “I wasn’t sure it worked at first.”  
P3 (Keyboard-only): “I didn’t see any pop up or message.”

**Finding**: in each mode, all three participants found that their confidence in the app dropped due to the lack of confirmation.
**Backlog item**: ID 5, "confirmation after action", Severity: Medium, Inclusion risk: Cognitive

**WCAG**: 4.1.3 Status Messages (AA) — Users must receive clear feedback when actions succeed.

**Evidence file**:  
`pilot-notes.md` lines 5–11 (P1), 27–32 (P2), 52–55 (P3)

**Screenshot**: testing_screenshots/week_9/no_confirmation.png

---

## Chain 2: Edit Uncertainty (Especially No-JS)

**Raw data**:  
P2: “Edit kind of doesn’t work in no JS.”  
P3: “Edit feels invisible unless you check manually.”  
findings.md: "participants always needed to check if things had actually saved."

**Finding**: Edit does not work in nojs mode and all uses found it slighlty worrying that when they edited a task that their edit was not saved.

**Backlog item**: ID 11, "Edit does not work in no js", Severity: Medium, Inclusion risk: Cognitive

**WCAG**: 3.3.3 Error Suggestion (AA) — Users should receive clear feedback when changes occur.

**Evidence file**:  
`pilot-notes.md` lines 33–34 (P2), 60–62 (P3)

**Screenshot**: testing_screenshots/week_9/edit_no_conf.png

---

## Chain 3: No-JS Reload Behaviour Causes Confusion

**Raw data**:  
P2: “Without JavaScript it all feels slower and jumpy.”  
P2 needed multiple full-page reloads for filter + edit.  
findings.md: “Filtering felt sluggish without JavaScript.”

**Finding**: All actions caused a reoad, this bugged users and made the page feel slow. and there is no delete confirmation.

**Backlog item**: ID 9 (related to parity + missing JS behaviour), Severity: High, Inclusion risk: Cognitive

**WCAG**: 2.4.3 Focus Order (A) — Reloading disrupts interaction flow  
(also indirectly relates to 4.1.3 Status Messages)

**Evidence file**:  
`wk09/data/pilot-notes.md` lines 27–37  
`wk09/data/findings.md` Task 1 interpretation

**Screenshot**: n/a

---

## Chain 4: Delete Produces Low Confidence (All Modes)

**Raw data**:  
P1: “Delete confirmation is easy to miss.”  
P2: Checked the list twice to confirm deletion.  
P3: “Delete feels risky without undo.”  
findings.md: users always re-check list after deletion.

**Finding**: Ther was no undo option and there was no confirmation after deleting, so they had to double check the list.

**Backlog item**: ID 8, "Delete confirmation missing in no-JS", Severity: Medium, Inclusion risk: Motor, Cognitive

**WCAG**: 3.3.4 Error Prevention (AA) — Important or destructive actions should include confirmation or undo.

**Evidence file**:  
`pilot-notes.md` (P1 + P2 + P3 delete sections)  
`findings.md` Task 4 interpretation

**Screenshot**: n/a

---
