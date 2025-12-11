- keyboard only : works great, good, logical order
- no-js parity: filtering/paging still works via full page reloads
- History: List doesn't revert
- 

## Trade Off Notes - Week 8

### Full Page renders vs HTMX fragments
- Benefit: No Js support with faster HTMX updates
- Cost: Two rendering paths

### Accessibility Hooks
- live regions mean screen readers work
- focus needs to be managed after HTMX swaps
- announced result reduces cognitive load for reader

### State management decisions
- querey params control filtering and pagination and must stay consistent
- need to watch page size as too many tasks could cause too much navigation or too much cognitive load

### Risks introduced
- _list.peb and _pager.peb must be updated together
- duplicate HTML renderinc increases maintainence
- entering an out of range page could cause errors