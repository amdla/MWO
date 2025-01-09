requirementDiagram
    requirement W1 {
        id: 1
        text: "Płacenie za bilet różnymi metodami: kartą, gotówką, telefonem."
    }
    requirement W3 {
        id: 4
        text: "Aktualizowanie zdalne oprogramowania biletomatów"
    }
    element User {
        type: simulation
    }
    element Administrator {
        type: system
    }
    User - satisfies -> W1
    Administrator - satisfies -> W3
