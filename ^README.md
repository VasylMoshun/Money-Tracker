classDiagram
User <--> SpendHistory
SpendHistory *-- Category
SpendHistory *-- Source
Source .. Cash
Source .. CreditCard

    class Source
    Source : -Double balance
    SpendHistory: -User user

    class SpendHistory
    SpendHistory: -Double amount
    SpendHistory: -String description
    SpendHistory: -Date date
    SpendHistory: -Source source
    SpendHistory: -Category category


     class User
    User : -Lond id
    User : -String name
    User : -String surname
    User : -String mail
    User : -String password
    User: List SpendHistory

    class Category
    Category: -Long id
    Category: -String name
    Category: List SpendHistory
