# Group Project: Begin Wireframes & Software Requirements

## Wireframes

![Appointment](/images/Appointment.png)

![Booking](/images/Booking.png)

![HomePage](/images/HomePage.png)

## User Stories

### for malek

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