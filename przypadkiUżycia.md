```mermaid
requirementDiagram
    requirement ticketPayment {
        text: "Płacenie za bilet różnymi metodami: kartą, gotówką, telefonem."
    }
    requirement ticketUpdate {
        text: "Aktualizowanie zdalne oprogramowania biletomatów"
    }
    requirement ticketSelection {
        text: "Wybór oferty"
        }
    requirement languageSelection {
        text: "Wybór języka biletomatu"
        }
    requirement transactionVerification {
        text: "Zakup biletu"
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
    Administrator - satisfies -> configTickets
    Administrator - satisfies -> ticketUpdate
    transactionVerification - traces -> ticketPayment
    ticketSelection - traces -> transactionVerification