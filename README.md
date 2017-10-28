# assignment_designing_nosql_data_models
I'll have one data model hold the SQL please
*Sean Kelly*

# Basic
1. They will need to be able to set their birthday, gender, phone number and location (city, state, country). They should be able to provide text to tell about themselves. They also should be able to enable and disable the visibility of their birthday, gender, phone number, and location.

### Users
* id
  * username: string
      * must contain only word characters
  * password: string
      * must be at least 8 characters
  * profile
    * birthday
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

### available_tables
* table
  * id: integer
  * time: date/time

### reservations
* table_id: integer
* name: string
* guests: integer
* phone: integer
  * must be 10 digits

2. You're building a backend for a university that requires students to be able to login. Once logged in, the students can view the exam grades for their classes. They should be able to view results by semester. Each semester should only show the classes in which that student is enrolled that semester.

### Users
* username: string
    * must contain only word characters
* password: string
    * must be at least 8 characters

### grades
* semester_id: integer
  * start_date: datetime
  * end_date: datetime
  * class: id: integer
    * student_id: integer
      * grades: float

# Advanced
1. Your eCommerce business needs to keep track of products and their prices. The products each belong to a department. The business needs to keep track of revenue as product prices change over time. The business also needs to keep track of receipts of transactions and the number of units each product has in stock.

### product
* id: integer
  * department_id: integer
  * price
    * value: float
    * date: date/time
  * in_stock: integer

### receipts
* id: integer
  * product_id: integer
  * purchase_date: date/time

2. You're building an activity feed for a social media site. The feed must display a chronological list of activities for the current user's friends. These activities could potentially be any action performed on the site including uploading a photo, changing their profile, friending another user, commenting, liking etc... Further, you only want to display activities for users that the current user interacts with frequently.

### users
* user_id: integer
  * friends
    * friend_id: integer
    * interact_coefficient: float

### events
* event_id
  * user_id: id
  * event
    * type: text in(events)
    * content: link
  * timestamp: date/time
