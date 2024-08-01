<p align="center">
<img src="https://cwmkt.com.br/wp-content/uploads/2024/04/logo_github.png" width="240" />
<p align="center">Seja bem-vindo ao Guia de Instalação EasyPanel Perfex 🚀</p>
</p>
  
<p align="center"> 
<a href="https://hubconnect.top" target="_blank">👉 Participe da Comunidade HubConnect 👈</a>
</p>

<hr />
<hr />

## Comando para Instalar EasyPanel

```bash
curl -sSL https://get.easypanel.io | sh
```

Adicione nome de Project

![48098522-0c485df00f5cadb0d329061c35fee46c](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/b72c1359-91ca-4bf6-9fb1-32525ba5747b)

Clique na aba Templates

![48098535-90f9b4f370bb8b06cfd7e4acf0ee0f97](https://github.com/cwmkt/easypanelevotypebot/assets/91642837/03c1830c-621c-40b3-94ee-93eb568c8d2e)

Va ate final da pagina

![image](https://github.com/comunidadehubconnect/easypanelwoofedcrm/assets/91642837/828a9e88-45f2-4b6b-98f1-ab4f164d2889)

Adicione codigo abaixo dentro do Schema


```bash
{
  "services": [
    {
      "type": "app",
      "data": {
        "projectName": "perfexcrm",
        "serviceName": "perfexcrm",
        "source": {
          "type": "image",
          "image": "astraonline/perfexcrm:versao3.1.5"
        },
        "domains": [
          {
            "host": "$(EASYPANEL_DOMAIN)",
            "port": 80
          }
        ],
        "env":"MYSQL_ROOT_PASSWORD=a5a1e7d36828bbe4154f",
        "mounts": [
          {
            "type": "volume",
            "name": "perfex_data",
            "mountPath": "/var/www/html/"
          }
        ]
      }
    },
     {
      "type": "mysql",
      "data": {
        "projectName": "mysql-prefex",
        "serviceName": "mysql",
        "password": "a5a1e7d36828bbe4154f"
      }
    }
  ]
}
```

Conclua Pagina Install

![image](https://github.com/user-attachments/assets/a7ed1e7c-0ca9-49a2-9392-32e4a3cce6ea)

Abra arquivo app-config.php

```bash
/etc/easypanel/projects/seuprojeto/perfexcrm/volumes/perfex_data/application/config
```


```bash
app-config.php
```

Acesse pasta perfex_data

```bash
/etc/easypanel/projects/apagar/perfexcrm/volumes/perfex_data
```

Apague a pasta install

Altere linha 20 de http para https

Pronto tudo Funcionando ✅😎

Creditos: Andre Marques
