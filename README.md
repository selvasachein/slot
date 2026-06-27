# Ex02 Time Table
## Date:

## AIM
To write a html webpage page to display your slot timetable.

## ALGORITHM
### STEP 1
Create a Django-admin Interface.

### STEP 2
Create an App inside the Django project.

### STEP 2
Create a static folder uder the created App and insert HTML code.

### STEP 3
Create a simple table using ```<table>``` tag in html with the relevant attributes.

### STEP 4
Add rows using ```<tr>``` tag.

### STEP 5
Add your course schedule using ```<td>``` tag.

### STEP 6
Execute the program using runserver command.

## PROGRAM


## OUTPUT


## RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.

## Crash Recovery Policy (SwiftData)

### Objective
Avoid startup crashes when local persistent data is incompatible or corrupted, and provide a user-consented recovery flow.

### Scope
1. Replace startup-time `fatalError`/`assertionFailure` on `ModelContainer` creation failure with recoverable handling.
2. Show a blocking dialog when recovery is possible:
   - Message: `登録データが不整合です。データをクリアしますか？`
   - Actions: `はい` / `キャンセル`
3. On user approval, remove the local store and retry `ModelContainer` initialization.
4. On cancel, keep the app in a safe state with a clear error screen (no partial launch).

### Implementation approach
1. Move persistent container bootstrapping into a dedicated startup coordinator.
2. Surface initialization state to SwiftUI root (`loading`, `ready`, `recoveryRequired`, `failed`).
3. Implement a store reset routine that targets only app-owned persistent files.
4. Reinitialize container after reset and continue normal app launch.

### Operational notes
1. This recovery resets local data; user consent is mandatory.
2. Add structured error logging around initial failure and recovery result for TestFlight diagnostics.
3. Keep migration path as the primary long-term strategy; reset flow is fallback for non-recoverable store states.
