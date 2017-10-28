# assignment_designing_nosql_data_models
I'll have one data model hold the SQL please
Sean Kelly

# Basic
They will need to be able to set their birthday, gender, phone number and location (city, state, country). They should be able to provide text to tell about themselves. They also should be able to enable and disable the visibility of their birthday, gender, phone number, and location.

## Users
* username: string
    * must contain only word characters
* password: string
    * must be at least 8 characters
* birthday:
  * date: date
    * must be at least current date
  * visible: boolean (default: true)

* gender
  * gender: string(in male, female, n/a)
    * must be at least len = 10
  * visible: boolean (default: true)

* phone number: integer
  * visible: boolean (default: true)
    * must be at least len = 10
* location
    * city: string
      * max len = 24
    * state: string
      * in (list of states)
    * country: string
      * in (list of countries)
    * visible: boolean (default: true)

#  Intermediate
1. You're building a restaurant table reserving app that allows users to reserve tables for specified numbers of people. The app will need to show only tables that are available and the times they are available. The app will need to store reservations under a given name with a phone number and number of guests.



You're building a backend for a university that requires students to be able to login. Once logged in, the students can view the exam grades for their classes. They should be able to view results by semester. Each semester should only show the classes in which that student is enrolled that semester.
