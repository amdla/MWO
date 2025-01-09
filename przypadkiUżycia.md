```mermaid
requirementDiagram
    requirement ticketSelection {
        text: "Szybki wybór rodzaju biletu"
        }
    requirement languageSelection {
        text: "Wybór języka biletomatu"
        }
    requirement transactionVerification {
        text: "Sprawdzenie poprawności transakcji"
        }

    requirement configTickets {
        text: "Konfiguracja dostępnych biletów, promocji i taryf w systemie centralnym"
    }

    element User {
        type: simulation
    }

        element Administrator {
        type: simulation
    }

    User - satisfies -> ticketSelection
    User - satisfies -> languageSelection
    User - satisfies -> transactionVerification
    Administrator - satisfies -> configTickets
