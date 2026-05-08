---
question: "Która z poniższych odpowiedzi jest poprawna w odniesieniu do tokenów dostępu instalacji?"
documentation: "https://docs.github.com/en/apps/creating-github-apps/authenticating-with-a-github-app/authenticating-as-a-github-app-installation#using-an-installation-access-token-to-authenticate-as-an-app-installation"
---

- [x] Tokeny dostępu instalacji to krótkoterminowe tokeny idealne do działań automatyzacyjnych, ale wymagają skonfigurowania Github App.
- [x] `GITHUB_TOKEN` jest rodzajem tokenu dostępu instalacji.
> `GITHUB_TOKEN` to token dostępu instalacji GitHub App, który jest automatycznie generowany dla każdego uruchomienia workflow. Zobacz [dokumentację](https://docs.github.com/en/actions/concepts/security/github_token) dla dodatkowych szczegółów.
- [x] Akcja `actions/create-github-app-token` może być wywoływana w obrębie workflow w celu utworzenia tokenu dostępu instalacji, który jest natychmiast gotowy do użycia.
- [ ] Akcja `actions/create-github-app-token` może być wywoływana w obrębie workflow w celu utworzenia tokenu dostępu instalacji, ale token dostępu instalacji może być użyty dopiero w przyszłych uruchomieniach workflow.
> Po utworzeniu token dostępu instalacji może być używany natychmiast. Zobacz [oficjalną stronę tej akcji](https://github.com/actions/create-github-app-token) dla dodatkowych szczegółów.
- [ ] Tokeny dostępu instalacji nie mogą być skonfigurowane do działania w imieniu powiązanej Github App.
> Tokeny dostępu instalacji są często konfigurowane do działania w imieniu powiązanej Github App. Może to pomóc w audytowaniu działań automatyzacyjnych.
