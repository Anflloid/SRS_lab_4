@startuml
left to right direction

actor "Адмін" as Admin
actor "Менеджер" as Manager
actor "Користувач" as User

rectangle "TaskMaster" {
  (Реєстрація/вхід) as login
  (Додати користувача) as add_user
  (Створити завдання) as create
  (Оновити статус) as update
  (Переглянути завдання) as view

  Admin --> login
  Admin --> add_user

  Manager --> login
  Manager --> create
  Manager --> view

  User --> login
  User --> update
  User --> view
}

@enduml
