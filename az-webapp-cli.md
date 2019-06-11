# Azure CLI

## Objectifs

Cet atelier montre comment utiliser la Command-Line Interface Azure pour créer un Resource Groupe et un application web dans App Service à l’aide de [Cloud Shell](https://docs.microsoft.com/azure/cloud-shell/overview).

Vous pouvez réaliser cet atelier dans Cloud Shell ou localement avec [Azure CLI](https://docs.microsoft.com/fr-fr/cli/azure/install-azure-cli).

## Scénario

Dans cet atelier vous apprendrez à:

- Créer un groupe de ressources

- Créer un plan App Service en spécifiant des paramètres

- Créer une Web App en spécifiant des paramètres

- Supprimer le groupe de ressources

## Créer un resource group

La commande `az group create` est une commande qui créé un groupe de ressource dans la souscription courante.

Dans Cloud Shell, éxécutez la commande suivante pour créer un resource-group temporaire:

```azurecli-interactive
az group create -n deleteme-rg --location westeurope
```

## Créer un plan App Service

La commande `az appservice plan create` est une commande qui créé un plan d'app service dans le resource group spécifié.

Dans Cloud Shell, éxécutez la commande suivante:

```azurecli-interactive
az appservice plan create -n deleteme-plan -g deleteme-rg -l westeurope --sku B1
```

## Créer une web app

La commande `az webapp create` est une commande qui créé une application App Service dans le resource group spécifié.

Dans Cloud Shell, éxécutez la commande suivante:

```azurecli-interactive
az appservice plan create -n deleteme-plan -g deleteme-rg -l westeurope --sku B1
```

## Accéder à l’application

Pour accéder à l’application déployée à l’aide de votre navigateur web, vous devrez vous rendre à l'adresse `https://<app_name>.azurewebsites.net` dans laquelle vous remplacerez <app_name> par le nom de votre application.

**Félicitations !** Vous avez créé votre première application via la CLI Azure.

## Supprimer des ressources

Au cours des étapes précédentes, vous avez créé des ressources Azure au sein d’un groupe de ressources. Si vous ne pensez pas avoir besoin de ces ressources à l’avenir, supprimez le groupe de ressources dans Cloud Shell.

```azurecli-interactive
az group delete --name deleteme-rg
```

L’exécution de cette commande peut prendre une minute.
