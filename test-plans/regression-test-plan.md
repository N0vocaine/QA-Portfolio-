# Mobile Regression Test Plan

## Objective
Verify that the mobile application works correctly after a new release, with focus on core flows, content, and cross-platform consistency.

## Context
- Production mobile application
- Multilingual content (EN + SV)
- Platforms: iOS and Android

## Scope
- Settings  
- Main service flows (e.g. booking, navigation)  
- Workout and video content  
- Self-assessment flows  
- Profile and health sections  

## Test Approach

### Functional testing
- Verify main entry points are accessible  
- Validate user can complete key flows  
- Ensure screens load correctly  
- Check that buttons and links are working  

### Content and localization
- Verify English content is displayed correctly  
- Identify mixed-language issues  
- Check for missing or incorrect translations  
- Validate wording clarity and consistency  

### Cross-platform testing
- Compare behavior between iOS and Android  
- Validate consistency of flows and navigation  
- Identify platform-specific issues  

## Test Types
- Smoke testing  
- Functional testing  
- Regression testing  
- Exploratory testing  

## Focus Areas (Risk-Based)
- Language inconsistencies  
- Broken or non-clickable links  
- UI issues (spacing, alignment, layout)  
- Incorrect or unclear wording  
- Loading or partial rendering issues  
- Incorrect state after completing actions  

## Execution
For each scenario:
1. Execute the flow step-by-step  
2. Compare actual vs expected behavior  
3. Validate on both iOS and Android  
4. Mark result as PASS or FAIL  
5. Add notes for any issues or inconsistencies  

## Defect Handling
When a failure is identified:
1. Reproduce the issue  
2. Check if it occurs on one or both platforms  
3. Compare with expected behavior or design  
4. Categorize the issue (functional / UI / content / navigation)  
5. Log a bug report with:
   - steps to reproduce  
   - actual result  
   - expected result  
6. Retest after fix  

## Risks
- Language inconsistencies  
- Broken navigation  
- Incorrect flow routing  
- Missing validation messages  

## Exit Criteria
- No critical issues in core flows  
- Main user journeys can be completed  
- Blocking issues are reported  

## Note
This example is anonymized and created for portfolio purposes.
