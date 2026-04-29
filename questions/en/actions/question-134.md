---
question: "How do you use Github Script in workflows?"
documentation: "https://docs.github.com/en/actions/reference/security/secure-use#using-third-party-actions"
---

- [x] Via the `actions/github-script` action
> To use Github Script, you must call upon [`actions/github-script`] (https://github.com/actions/github-script) 
- [ ] By enabling its configuration in the Actions settings of a repository
> There are no settings relating to Github Script in the Actions settings of a repository.
- [ ] By enabling its configuration in the Actions settings of an organization
> While you may have to enable settings like 'Allow actions created by Github' in an organization's Action settings to use official Github Actions, this is not only related to Github Script. 
- [ ] Write the contents of a script block to the `GITHUB_SCRIPT` environmental variable
> `GITHUB_SCRIPT` is not a default Github Actions environmental variable. A list of default environmental variables can be found in the [documentation](https://docs.github.com/en/actions/reference/workflows-and-actions/variables)
- [ ] In a JavaScript Action, set the `using` key to `'github-script'`
> JavaScript Actions must have their `using` key set to `node*` where * is a supported version of Node.js.  Generally, JavaScript Actions do not have a huge need for Github Script.