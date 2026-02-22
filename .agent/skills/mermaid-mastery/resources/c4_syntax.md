# C4 Diagram Syntax

## Context
```mermaid
C4Context
  title System Context diagram for Internet Banking System
  Person(customerA, "Banking Customer A", "A customer of the bank, with personal bank accounts.")
  System(SystemAA, "Internet Banking System", "Allows customers to view information about their bank accounts, and make payments.")

  System_Ext(mail_system, "E-mail system", "The internal Microsoft Exchange e-mail system.")
  System_Ext(mainframe, "Mainframe Banking System", "Stores all of the core banking information about customers, accounts, transactions, etc.")

  Rel(customerA, SystemAA, "Uses")
  Rel(SystemAA, mail_system, "Sends e-mails", "SMTP")
  Rel(SystemAA, mainframe, "Uses")
  Rel(mail_system, customerA, "Sends e-mails to")
```

## Types
- `Person(alias, label, desc)`
- `System(alias, label, desc)`
- `System_Ext(alias, label, desc)`
- `Container(alias, label, technology, desc)`
- `Component(alias, label, technology, desc)`
- `Rel(from, to, label, technology)`
