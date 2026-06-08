---
question: "Organizacja posiada kilka repozytoriów, które współdzielą specjalne środowisko Node.js hostowane w prywatnej sieci. Kolejnym celem organizacji jest konfiguracja oprogramowania blokującego dostęp do węzłów w tej sieci. Które z poniższych rozwiązań najlepiej odpowiada potrzebom organizacji w zakresie wykonywania przepływów pracy?"
documentation: "https://docs.github.com/en/actions/concepts/runners/self-hosted-runners"
---

- [x] Self-hosted runners skonfigurowane na poziomie organizacji
- [ ] Jeden self-hosted runner na repozytorium, skonfigurowany na poziomie repozytorium
> Byłoby to powielanie i skomplikowane w zarządzaniu. Repozytoria mogą odwoływać się do tego samego runnera na poziomie organizacji, co jest odpowiednim podejściem w tej sytuacji.
- [ ] GitHub-hosted runners, gdzie wszystkie przepływy pracy wykorzystują `actions/setup-node`
> GitHub-hosted runners są [efemeryczne](https://docs.github.com/en/actions/concepts/runners/github-hosted-runners#overview-of-github-hosted-runners), co oznacza, że nowa instancja runnera jest konfigurowana przy każdym uruchomieniu przepływu pracy. To nie współgra z oprogramowaniem blokującym dostęp do węzłów, które pozwala działać wyłącznie na określonym urządzeniu/VM. Ponadto, chociaż GitHub-hosted runners mogą być skonfigurowane do uzyskiwania dostępu do prywatnych sieci, nie jest to funkcjonalność dostępna od razu.
- [ ] GitHub-hosted runners skonfigurowane na poziomie organizacji
> GitHub-hosted runners nie mogą być tak skonfigurowane.
- [ ] GitHub-hosted runners, używając `runs-on: [node<version>]` (`<version>` oznacza wymaganą wersję Node) we wszystkich przepływach pracy.
> `[node<version>]` nie wskazuje na żadnego GitHub-hosted runnera.
