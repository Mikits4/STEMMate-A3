# UI and Accessibility

##  UX/UI and Accessibility

### Version 1 - Initial Design

The purpose of the Version 1 design is to turn the agreed requirements into a simple interface that can be used to build the interactive prototype.

The design is intentionally basic because this is the first prototype version. It focuses on clear navigation, readable information and the main facilitator tasks rather than advanced visual features.

---

## 1. Design Goals

The interface was designed with the following goals:

- Keep the prototype simple and easy to understand.
- Provide clear navigation between the main functions.
- Make activities easy to find and read.
- Make saved activities easy to access when there is no internet.
- Use clear text labels instead of relying only on icons.
- Avoid unnecessary images, animations and other heavy content.
- Keep the interface suitable for shared and lower-specification devices.
- Provide clear feedback when the system is offline or an action fails.

---

## 2. User Flow

### Workflow 1 - Find an Activity

Home  
↓  
Find Activities  
↓  
Select Filters  
↓  
Activity Results  
↓  
Activity Details  

### Workflow 2 - Prepare a Session

Activity Details  
↓  
Create Session Plan  
↓  
Review Session Plan  
↓  
Save Plan  

### Offline Workflow

Activity Details  
↓  
Save Activity for Offline Use  
↓  
Internet Becomes Unavailable  
↓  
Saved Activities  
↓  
Open Saved Activity  

If the user tries to perform an online action while there is no connection:

Online Action  
↓  
Connection Fails  
↓  
Offline / Error Message  
↓  
Open Saved Activities OR Try Again

---

## 3. Screen Designs

Eight main screens were selected for Version 1.

### Screen 1 - Home

The Home screen provides access to the main functions.

Main options:

- Find Activities
- Saved Activities
- Session Plans

The connection status should also be visible as text such as:

**Online**

or

**Offline**

This makes the connection status understandable without depending only on colour.

---

### Screen 2 - Find Activities

The Find Activities screen allows the facilitator to filter activities.

Filters:

- Education Level
- Topic
- Duration

Example:

Education Level: `Upper Primary`

Topic: `Science`

Duration: `30-45 minutes`

Main action:

**Show Activities**

---

### Screen 3 - Activity Results

This screen displays activities that match the selected filters.

Example:

**Water Filtration**  
Science | 30-45 minutes

**Solar Oven**  
Science | 45-60 minutes

**Plant Growth Investigation**  
Science | 30-45 minutes

Selecting an activity opens the Activity Details screen.

---

### Screen 4 - Activity Details

This screen provides the information needed to conduct the activity.

Example:

## Water Filtration

**Level:** Upper Primary  
**Topic:** Science  
**Duration:** 30-45 minutes

### Materials

- Plastic bottle
- Sand
- Gravel
- Cloth
- Container

### Instructions

1. Prepare the bottle.
2. Add the filter materials.
3. Pour the water through the filter.
4. Observe the result.

### Safety

Do not drink the filtered water.

An adult should handle any cutting.

### Inclusion Guidance

Learners can work in small groups and take different roles such as preparing materials, observing and recording results.

Main actions:

**Save for Offline Use**

**Create Session Plan**

---

### Screen 5 - Saved Activities

This screen contains activities that have been saved on the device.

When offline, the screen should display:

**You are offline. Saved activities are still available.**

Example:

**Water Filtration**  
Available offline

**Solar Oven**  
Available offline

This allows facilitators to continue using previously saved content without internet access.

---

### Screen 6 - Create Session Plan

The facilitator can prepare a simple session plan.

Fields:

**Activity**

Water Filtration

**Date**

03/10/2026

**Duration**

45 minutes

**Notes**

The facilitator can enter additional session notes.

Main action:

**Review Plan**

---

### Screen 7 - Review Session Plan

The facilitator reviews the information before saving the plan.

Example:

**Activity:** Water Filtration

**Level:** Upper Primary

**Topic:** Science

**Duration:** 45 minutes

**Notes:** Learners will work in groups.

Actions:

**Edit**

**Save Plan**

---

### Screen 8 - Offline / Error

The offline screen should clearly explain what happened instead of displaying only a technical error.

Example:

# You are Offline

STEMMate cannot connect to the internet right now.

You can still:

- Open activities that were previously saved.
- Read saved activity information.

Internet access is required to search for activities that have not been saved.

Actions:

**Open Saved Activities**

**Try Again**

---

## 4. Accessibility

Accessibility was considered during the initial UI design.

| Area | Design Decision |
|---|---|
| Navigation | Main navigation is kept simple and consistent. |
| Labels | Buttons and inputs use clear text labels. |
| Colour | Important information does not depend on colour alone. |
| Contrast | Dark text is used against light backgrounds. |
| Offline status | The word "Offline" is displayed together with visual indicators. |
| Errors | Error messages explain what happened and what the user can do next. |
| Layout | Screens use simple layouts that can work on smaller displays. |
| Touch targets | Main buttons and activity cards are designed as large selectable areas. |
| Content | Unnecessary animations and large media are avoided. |
| Structure | Activity information follows a consistent structure. |

Keyboard operation, focus order, contrast and resizing will also need to be checked when the interactive prototype is implemented.

---

## 5. Requirements Traceability

The UI was designed from the requirements selected for the A3 prototype.

| Requirement | UI Implementation |
|---|---|
| FR01 | Find Activities and Activity Results |
| FR02 | Education Level, Topic and Duration filters |
| FR03 | Activity Details screen |
| FR04 | Save for Offline Use and Saved Activities |
| FR05 | Create and Review Session Plan |
| QR01 | Simple navigation, feedback and error messages |
| QR02 | Text is used together with colour and icons |
| QR03 | Offline / Error screen |
| QR04 | Simple layouts and limited heavy content |
| SR01 | Activities follow the same information structure |

---

## 6. Design Decision

### Decision

Use simple navigation instead of a large multi-level menu.

### Alternatives Considered

**Alternative 1:**  
Use a larger menu containing additional features such as learner management, assessment, profile, settings and other LMS functions.

**Alternative 2:**  
Use a small navigation structure containing only:

- Home
- Activities
- Saved
- Plans

### Evidence Used

The requirements selected for A3 focus on activity discovery, filtering, activity information, offline saving and session planning.

The requirements also state that the prototype should consider shared and lower-specification devices.

### Selected Option

Alternative 2 was selected.

### Reason

The smaller navigation structure makes the main facilitator tasks easier to find and avoids adding features that are outside the A3 prototype scope.

### Trade-off

Future features are not immediately available from the main interface.

This was accepted because features such as pupil accounts, learner assessment, VR/AR and full LMS functionality were excluded from the A3 scope.

---

## 7. Version 1 Design Style

The first version uses a basic low-fidelity design similar to an early Figma prototype.

Suggested styling:

- Background: light grey or white
- Header: dark blue
- Primary action: orange
- Secondary action: teal
- Main text: dark grey
- Error/offline warning: dark orange/red
- Simple rectangular cards
- Minimal shadows
- Rounded corners kept small
- Clear sans-serif font

The purpose of Version 1 is to test the structure and usability before spending time on detailed visual styling.

---

## 8. Handover

The UI design provides the structure for the students responsible for prototype development.

### Workflow 1

Home → Find Activities → Filters → Results → Activity Details → Save Offline

### Workflow 2

Activity Details → Create Session Plan → Review Session Plan → Save Plan

### Offline / Recovery

Connection unavailable → Offline Message → Open Saved Activities / Try Again

The interactive prototype should keep the same labels and general screen structure so that the requirements can be traced from the documentation to the prototype.

---

## AI Use Declaration

ChatGPT was used to assist with organising and documenting the Version 1 UX/UI design and accessibility considerations.

The final design decisions were checked against the requirements selected for the A3 prototype.

AI was not used to generate participant feedback, testing results, repository history or other evidence that did not occur.
