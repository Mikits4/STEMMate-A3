# Requirements and Architecture

## Requirements

The requirements from A1 and A2 were reviewed and narrowed down to the main functions needed for the A3 prototype. The focus is on helping facilitators find activities, get the information they need, prepare a session and use saved activities when there is no internet.

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

Not all of the requirements from A1 and A2 were carried into A3. The selected requirements cover the main facilitator workflows and the low-resource conditions in the STEMMate case.

Pupil accounts, learner assessment, VR/AR and full LMS features were left out of the A3 scope.

The requirements also cover offline use, accessibility, shared devices and limited device performance. These affect how activities are stored, accessed and presented.

### Traceability

| Requirement | Prototype part           | Evaluation                                               |
| ----------- | ------------------------ | -------------------------------------------------------- |
| FR01        | Activity list            | User can find an activity                                |
| FR02        | Activity filters         | User can narrow down the activities                      |
| FR03        | Activity information     | User can find the information needed to run the activity |
| FR04        | Saved activity           | User can save and open an activity without internet      |
| FR05        | Session plan             | User can view or create a session plan                   |
| QR01        | Navigation and feedback  | User understands what happened after an action           |
| QR02        | Text and non-colour cues | Important information is still clear without colour      |
| QR03        | Offline and error states | User knows when something has gone wrong                 |
| QR04        | Activity content         | Activities do not depend on unnecessary heavy content    |
| SR01        | Activity data structure  | Activities use the same structure                        |

## Architecture

The system is divided into the interface, application logic and activity data.

### Main parts

**Interface**

The facilitator can browse activities, filter them, open activity information, save activities and work with session plans.

**Application logic**

This handles filtering activities, opening activities, saving activities, managing session plans and handling offline or failed actions.

**Data**

This contains the activity name, level, topic, duration, materials, instructions, safety information and inclusion guidance. Saved activities are also stored locally for offline use.

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

The interface sends requests to the application logic, which gets the required information from the available data.

### Offline and recovery

A facilitator can save an activity while connected and open it later when the connection is unavailable.

The workflow is:

**Save activity → internet unavailable → open saved activity → connection returns**

The system also shows when an action cannot be completed because there is no connection.

### Architecture decisions

Local saved activities are used so that previously saved content is still available without internet. Activity information uses a consistent structure so that different activities can contain the same types of information.

Pupil accounts, learner assessment, VR/AR and full LMS functionality are outside the A3 architecture.
