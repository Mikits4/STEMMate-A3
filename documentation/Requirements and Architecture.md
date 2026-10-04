# Requirements and Architecture

## Requirements

The requirements were taken from the work done in A1 and A2 and narrowed down to the parts that are needed for the A3 prototype. The main focus is on helping facilitators find activities, get the information they need, prepare a session and still use saved activities when there is no internet.

### Functional requirements

| ID   | Requirement                                                                                                              | Priority |
| ---- | ------------------------------------------------------------------------------------------------------------------------ | -------- |
| FR01 | The system shall allow facilitators to browse STEM activities.                                                           | Must     |
| FR02 | The system shall allow facilitators to filter activities by level, topic and duration.                                   | Must     |
| FR03 | The system shall provide the instructions, materials, timing, safety information and inclusion guidance for an activity. | Must     |
| FR04 | The system shall allow facilitators to save activities for offline use.                                                  | Must     |
| FR05 | The system shall allow facilitators to create or view a session plan for an activity.                                    | Should   |

### Quality and sustainability requirements

| ID   | Requirement                                                                                                          | Priority |
| ---- | -------------------------------------------------------------------------------------------------------------------- | -------- |
| QR01 | The system shall provide clear navigation and feedback when actions are completed or cannot be completed.            | Must     |
| QR02 | Important information shall not rely on colour alone.                                                                | Must     |
| QR03 | The system shall show when there is no internet connection or when an action has failed.                             | Must     |
| QR04 | The system shall avoid unnecessary large or resource-heavy content for shared and lower-specification devices.       | Should   |
| SR01 | Activity information shall follow the same structure so that new activities can be added and maintained more easily. | Should   |

### Requirement selection

Not all of the requirements from A1 and A2 were carried into A3. The team kept the ones that are most important for the prototype and that match the main problems in the STEMMate case.

Pupil accounts, learner assessment, VR/AR and full LMS features were left out because they are not needed for the A3 prototype.

The requirements also put more focus on offline use and low-resource conditions. This is important because internet access can be unreliable, devices may be shared and some devices may not handle large or complicated content well.

### Traceability

| Requirement | Prototype part                 | Evaluation                                               |
| ----------- | ------------------------------ | -------------------------------------------------------- |
| FR01        | Activity list                  | User can find an activity                                |
| FR02        | Activity filters               | User can narrow down the activities                      |
| FR03        | Activity information           | User can find the information needed to run the activity |
| FR04        | Saved activity                 | User can save and open an activity without internet      |
| FR05        | Session plan                   | User can view or create a session plan                   |
| QR01        | Navigation and feedback        | User understands what happened after an action           |
| QR02        | Text and other non-colour cues | Important information is still clear without colour      |
| QR03        | Offline and error states       | User knows when something has gone wrong                 |
| QR04        | Simple content structure       | Prototype does not depend on unnecessary heavy content   |
| SR01        | Consistent activity data       | Activities can use the same structure                    |

## Architecture

The architecture was kept simple so it supports the prototype without adding parts that are not needed yet. It is split into the interface, the system logic and the activity data.

### Main parts

**Interface**

This is the part the facilitator uses to browse activities, filter them, open activity information, save activities and work with session plans.

**Application logic**

This handles the main actions of the system, such as filtering activities, opening an activity, saving an activity, handling session plans and dealing with offline or failed actions.

**Data**

This contains the activity information, such as the name, level, topic, duration, materials, instructions, safety information and inclusion guidance. Saved activities can also be kept locally for offline use.

### Basic architecture

```text
                Facilitator
                     |
                     v
              +--------------+
              |  Interface   |
              +------+-------+
                     |
                     v
              +--------------+
              | Application  |
              |    Logic     |
              +------+-------+
                     |
                     v
              +--------------+
              |     Data     |
              +------+-------+
                     |
              +------+------+
              |             |
              v             v
          Online data   Saved local data
```

The interface sends requests to the application logic, which gets the required information from the available data. This keeps the main parts separate instead of putting everything into one part of the system.

### Offline and recovery

Offline use is part of the system because STEMMate cannot assume that internet will always be available.

A facilitator can save an activity while connected and then open it later when the connection is unavailable.

The main workflow is:

**Save activity → internet unavailable → open saved activity → connection returns**

The system should also show when something cannot be completed because there is no connection, instead of leaving the user unsure about what happened.

### Architecture decisions

The architecture was kept fairly simple because A3 is a prototype and not a full production system. There is no need to add a large backend structure when the main purpose is to demonstrate the facilitator workflows.

Local saved activities are important because the system needs to keep working when internet access is unavailable. The data structure is also kept consistent so that activities can be added or changed without having to redesign the whole system.

Pupil accounts, learner assessment, VR/AR and full LMS functionality are outside the architecture because they are outside the A3 scope.
