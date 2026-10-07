## 📋 Spec-Driven Development (SDD) Pull Request Gate

### 1. Specification & Context
- **Related Spec / Issue**: Fixes/Implements #
- **SDD Stage**: [ ] Specify  [ ] Plan  [ ] Tasks  [ ] Implement  [ ] Converge

### 2. Constitution & Invariants Checklist
- [ ] **Architecture**: Separation of concerns maintained (Controller -> Service -> Repository).
- [ ] **Test-Backed Change**: 100% green tests covering new code and edge cases.
- [ ] **Zero Secrets**: No tokens, API keys, or hardcoded credentials.
- [ ] **Idempotency**: Mutating requests are idempotent and concurrency-safe.
- [ ] **Minimal Diff**: Zero unnecessary refactoring or scope creep.

### 3. Convergence Verification
- **Automated Tests Passed**: `mvn test` / `pytest` / `npm test` ✅
- **Static Analysis / Lint**: Clean ✅
- **Spec Convergence**: [ ] Converged (Exit 0)
