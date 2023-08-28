# Group Project: Begin Wireframes & Software Requirements

## Wireframes

![Appointment](/images/Appointment.png)

![Booking](/images/Booking.png)

![HomePage](/images/HomePage.png)

-------

## User Stories

- **Users :** secretary, doctor, patient

### Senario 1

As a new patient who didn't go to the clinic before and want to book an appointment, he will go to the home page through clicin domain, then click on sign up button and put his registering information.

Then a url redirection will happen to the login page. With putting his credentials he will be logged in.


### Senario 2

A registered patient want to book a new appointment, he will go to the application and log in then going to the booking tab then to the dentist tab and he can choose his doctor, when click on the doctor he will see the booked and available dates and time for this doctor then he can choose from the available times and click on book button. 

- a confirmation message will appear on the window.

- He will receive a confirmation message with the date and time of the appointment on his phone.

- The doctor also will recieve a message for this appointment.


### Senario 3

A patient s to see his appointments, he will login to the application and then from the appointments tab he can select from 2 sub tabs (upcoming and history) and then seeing his upcoming or old appointments.


### Senario 4

A patient wnats to edit or delete his appointment, he will login to the application and then from the appointments tab the upcoming tab and then click on delete button then confirm the deletion message .. or edit a specific appointment from edit button then save button.


### Senario 5

A doctor wnats to see his appointments, he will login and from the appointments tab he can select from 2 sub tabs (upcoming and history) and then seeing his upcoming or old appointments.

- he can edit some information in history's appointments . 

- he can search about name of a patient or he can select a specific date.

- he can book a new appointment for a patient  from booking tab.

- Doctors can't do a sign up, only admin can add them.

--------

## Software Requirements

[README for requirements](./requirements.md)

## Domain Modeling

![Domain Modeling](/images/fronend.png)

## Using a Database? Make an Database Schema Diagram

![DatabaseSchema](/images/DatabaseSchema.png)

### database tables:

#### table Insurance fields:

1. Insurance_id PK
2. Insurance_name varchar(255)

- this table contain all the supported Insurance in this dental clinic.

#### table Gender fields:

1. gender_id PK
2. gender varchar(255)

- this table contain the gender of the people (male,female).

#### table Role fields:

1. Role_id PK
2. Role_name varchar(255)

- this table contain the role in this system ex: doctor,patient,...

#### table Account fields:

1. accounts_id PK
2. first_name varchar(255)
3. last_name varchar(255)
4. phone_number varchar(255)
5. email varchar(255)
6. password varchar(255)
7. date_of_birth date
8. role_id FK from Role table
9. Insurance_id FK from Insurance table
10. gender_id FK from Gender table

- this table contain the users info what gender are they what role do they have and do they have insurance and a lot more.

#### table treatment fields:

1. treatments_id PK
2. treatments_name varchar(255)

- this table contain all type of treatment the clinic can offer.

#### table Appointment_Status fields:

1. Appointment_Status_id PK
2. Status varchar(255)

- this table contain all type of status of the appointment the clinic can offer.

#### table appointment fields:

1. appointment_id PK
2. appointment_date date
3. appointment_time time
4. notes varchar(255)
5. payment int4range
6. doctor_id FK from Account table
7. patient_id FK from Account table
8. Appointment_status FK from Appointment_Status table


- this table contain all type of appointment in clinic.

#### table appointment_treatment fields:

1. appointment_treatment_id PK
2. treatments_id date
3. appointment_id time

- this table contain all treatments for a given appointment.