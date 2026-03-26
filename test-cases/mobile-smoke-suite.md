# Smoke Tests

## Objective
Quick validation that critical functionality works after a new build, before running full regression testing.

## Scope
- Core user flows  
- Navigation  
- Language / localization  
- Links (Terms, Privacy)  
- Basic UI rendering  
- Cross-platform behavior (iOS & Android)  

---

## Scenarios

### 1. App launch
**Steps:**
1. Open the app  

**Expected:**
- App loads successfully  
- Home screen is displayed  
- No crash or blank screen  

---

### 2. Main navigation
**Steps:**
1. Navigate between main sections (e.g. Home, Settings, Health)  

**Expected:**
- Screens load correctly  
- No broken navigation  
- No unexpected redirects  

---

### 3. Start main flow (care / consultation)
**Steps:**
1. Start a main flow (e.g. booking / consultation)  

**Expected:**
- Flow starts without errors  
- First screen is displayed correctly  

---

### 4. Continue in flow
**Steps:**
1. Answer first question in flow  
2. Tap “Continue”  

**Expected:**
- User can proceed to next step  
- No blocking issues  

---

### 5. Language validation (EN)
**Steps:**
1. Set app language to English  
2. Navigate through a flow  

**Expected:**
- All content is in English  
- No Swedish/mixed language content  

---

### 6. Terms of Use / Privacy Policy
**Steps:**
1. Open Terms of Use  
2. Open Privacy Policy  

**Expected:**
- Links are clickable  
- Correct pages are opened  
- No broken or missing content  

---

### 7. Content rendering
**Steps:**
1. Open different sections (flows, profile, health content)  

**Expected:**
- Text is visible and complete  
- No truncated or missing content  
- UI elements are properly aligned  

---

### 8. Cross-platform check
**Steps:**
1. Execute key flows on iOS and Android  

**Expected:**
- Same behavior on both platforms  
- No major inconsistencies  

---

## Exit Criteria
- No critical issues in core flows  
- App is usable for main user journeys  
- No blocking issues in navigation or flows  

---

## Note
Smoke tests are derived from regression scenarios and focus on validating critical paths before full testing.

This example is anonymized and created for portfolio purposes.
