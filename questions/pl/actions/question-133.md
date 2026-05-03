---
question: "Dlaczego warto używać commit SHA zamiast tagu do przypinania akcji?"
documentation: "https://docs.github.com/en/actions/reference/security/secure-use#using-third-party-actions"
---

- [x] Commit SHA są bardziej bezpieczne
> Commit SHA są bardziej bezpieczne, ponieważ obecnie są jedynym sposobem na użycie akcji jako niezmiennego wydania.
- [x] Commit SHA są niezmienne, podczas gdy tagi mogą zostać zmienione
> [Tagi](https://git-scm.com/book/en/v2/Git-Basics-Tagging) wskazują na konkretne commity. Ich referencje mogą zostać zmienione, co nie zawsze jest oczywiste. Luki związane z tagami można ograniczyć poprzez włączenie [niemiennych wydań](https://docs.github.com/en/code-security/concepts/supply-chain-security/immutable-releases), jednak commit SHA zawsze wskazuje na ten sam commit i jest niezmienny.
> Ponowne uruchomienie workflow korzysta z tego samego commit SHA i odniesienia Git, które wywołały pierwotne uruchomienie workflow.
- [ ] Commit SHA są wygodniejsze w użyciu niż tagi
> Mimo że są bardziej bezpieczne, tagi są na ogół łatwiejsze w użyciu.
- [x] Commit SHA gwarantują wskazanie dokładnie tego samego kodu za każdym razem, w przeciwieństwie do tagów
- [ ] Commit SHA są trudniejsze do prześledzenia podczas audytu, co utrudnia osobom o złych zamiarach ustalenie, jak kod akcji wpływa na ogólny proces.
> Commit SHA zawsze wskazują na ten sam commit. Przypinanie akcji do SHA oznacza, że SHA jest wyraźnie referencjonowane, co pozwala znaleźć odpowiedni commit w repozytorium akcji. Te czynniki ułatwiają audyt.
> Referencje tagów mogą być zmieniane, co nie zawsze jest oczywiste. Może to prowadzić do mylących scenariuszy, w których tag wskazuje na nowy commit, ponieważ kod referencjonujący akcję nie wydaje się zmieniony. W związku z tym podczas audytu trzeba ustalić, na jaki commit tag wskazywał i na co obecnie wskazuje.
