---
question: "Manuela está configurando runners autohospedados para su organización, que tiene comunicación con direcciones IP muy restringida. ¿Cómo puede asegurarse de que los runners autohospedados puedan comunicarse con GitHub?"
documentation: "https://docs.github.com/en/enterprise-cloud@latest/organizations/keeping-your-organization-secure/managing-security-settings-for-your-organization/managing-allowed-ip-addresses-for-your-organization#using-github-actions-with-an-ip-allow-list"
---

- [x] Añadiendo la(s) dirección(es) IP de los runners autohospedados a la lista de direcciones IP permitidas de la organización  
> Los runners autohospedados se comunican con GitHub para realizar diversas actividades, como se menciona en la [documentación](https://docs.github.com/en/enterprise-cloud@latest/actions/reference/runners/self-hosted-runners#communication). Para permitir esta comunicación, debes añadir la(s) dirección(es) IP del runner autohospedado a la lista de direcciones IP permitidas.  
- [ ] Añadiendo el sistema operativo de los runners autohospedados a la lista de sistemas operativos permitidos de la organización  
- [ ] Añadiendo el archivo `.ip-exception` al nivel superior de la estructura de directorios del runner autohospedado  
- [ ] Cambiando a runners estándar hospedados por GitHub, ya que los runners autohospedados serán bloqueados si se habilitan listas de direcciones IP permitidas  
- [ ] Seleccionando la casilla 'Allow access from self-hosted runners' en la configuración de la lista de direcciones IP permitidas de la organización  
