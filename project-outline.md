# Hospital Management System

## Notes

A patient checks into the hospital. Patient describes reason for being at the hospital.

Triage enters info about the patient and the reason they are there.

Triage gets vital signs.

Triage sets patients severity.

Patient gets called to room.

Patient gets seen by nurse and doctor.

Patient has labs done (usually).

Patient may stay at hospital.

If patient stays they get a room in the hospital.

The room is on a floor, the floor usually depends on the severity of the patient.

Possibly floor departments (ICU, Cardiac, Special Watch, etc...).

Hospital departments for different things done to the patient.

Hospital need to know patient medications, allergies, if they have any religious needs/preferences.

Hospital needs to know patient medical history.

Maybe add patient emergency contact.

Need to keep track of the current nurse/doctor is. Who took vitals at what time.

Based on severity, the patient may stay as a in-patient.

Might have to figure out structure for departments.

Does patient need physical therapy/rehabilitation services.

Doctor has to be able to add orders for the patient such as medications, labs, npo, etc...

Patient needs extra table to track other data such as if they need therapy as mentioned above, is patient npo, risk of falling, etc...

## Tables

- **patients**

  - patient id
  - first name
  - last name
  - dob
  - reason for visit
  - date & time of visit
  - \* hospital stay
  - \* date & time of discharge

Maybe make a table for in-patient hospitals along with hospitalization/discharge date & time.

- **doctors**

  - doctor id
  - first name
  - last name
  - specialization

- **nurses**

  - nurse id
  - first name
  - last name
  - \* floor
  - patients

- **departments**

  - department id
  - name
  - \* floor
  - \* workers

- **labs**

  - \* **TBD**

- **patient vital signs**

  - blood pressure
  - temperature
  - weight
  - height
  - oxygen levels (o2)

- **ER rooms**

  - room id
  - room number
  - is vacant
  - cleaned
  - patient

- **hospital rooms**
  - room id
  - room number
  - is vacant
  - ready
  - patient

Maybe put er rooms and hospital rooms in one table and have them available through department id (e.g., ER department, hospital department).

- **medications**

  - medication id
  - name

- **patient medications**
  - medication id
  - patient id
  - name
  - dosage
  - time givin
  - next dose
