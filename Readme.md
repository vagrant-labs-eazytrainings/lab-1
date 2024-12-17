# 🛩 Lab 1 : Première Machine Virtuelle avec Vagrant

## 🎯 **Objectif**

Dans ce premier laboratoire, l'objectif est de créer une **première machine virtuelle** avec Vagrant et de pratiquer les **commandes de base**. Cela permettra de comprendre comment initialiser, démarrer, arrêter et détruire une VM.

---

## 🧐 **Prérequis**

Assure-toi d'avoir installé les outils suivants :

- **[Vagrant](https://www.vagrantup.com/downloads)**
- **[VirtualBox](https://www.virtualbox.org/)**
- **[Git](https://git-scm.com/)** (optionnel)

---

## 🚀 **Commandes de Base Vagrant**

Voici un résumé des commandes Vagrant essentielles à pratiquer dans ce lab :

| **Commande**                 | **Description**                                            |
|------------------------------|-----------------------------------------------------------|
| `vagrant init`               | Initialise un nouveau projet Vagrant dans un dossier.     |
| `vagrant up`                 | Démarre et provisionne la machine virtuelle.              |
| `vagrant ssh`                | Se connecte à la machine virtuelle via SSH.               |
| `vagrant halt`               | Arrête proprement la machine virtuelle.                   |
| `vagrant destroy`            | Détruit complètement la machine virtuelle.                |
| `vagrant status`             | Affiche l'état actuel des machines virtuelles.            |
| `vagrant reload`             | Redémarre la machine virtuelle (applique les modifications). |
| `vagrant provision`          | Reprovisionne la machine virtuelle (reconfigure).         |
| `vagrant box list`           | Affiche les boxes Vagrant disponibles localement.         |
| `vagrant box add <box>`      | Télécharge et ajoute une nouvelle box Vagrant.            |
| `vagrant box remove <box>`   | Supprime une box Vagrant installée.                       |

---

## 📁 **Structure du Lab 1**

```plaintext
lab-1/
├── README.md                # Documentation du lab
└── Vagrantfile              # Configuration Vagrant pour créer la VM
```

## 🛠️ **Étapes Pratiques**

### 1. **Initialiser le projet**

Dans le dossier **lab-1**, initialise Vagrant :

```bash
vagrant init ubuntu/focal64
```

> Cela créera un fichier `Vagrantfile` avec une configuration par défaut.

---

### 2. **Configurer la VM**

Modifie le `Vagrantfile` comme suit pour une configuration simple :

```ruby
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.hostname = "lab1-vm"
  config.vm.network "private_network", type: "dhcp"
end
```

---

### 3. **Démarrer la machine virtuelle**

Démarre la VM avec la commande :

```bash
vagrant up
```

---

### 4. **Accéder à la machine virtuelle**

Une fois la VM démarrée, connecte-toi avec SSH :

```bash
vagrant ssh
```

---

### 5. **Vérifier le fonctionnement de la VM**

À l'intérieur de la VM, tu peux vérifier son fonctionnement :

- **Afficher l'adresse IP :**
  ```bash
  ip a
  ```

- **Quitter la VM :**
  ```bash
  exit
  ```

---

### 6. **Arrêter la machine virtuelle**

Pour arrêter proprement la machine :

```bash
vagrant halt
```

---

### 7. **Détruire la machine virtuelle**

Si tu veux supprimer complètement la VM :

```bash
vagrant destroy
```

---

## 🔄 **Commandes Résumées**

Voici un rappel rapide des commandes utilisées dans ce laboratoire :

```bash
# Initialisation
vagrant init ubuntu/focal64

# Démarrage et connexion
vagrant up
vagrant ssh

# Arrêt et destruction
vagrant halt
vagrant destroy

# Statut
vagrant status
```

---

## 📋 **Conclusion**

Dans ce Lab 1, tu as appris à :

1. Initialiser un projet Vagrant avec `vagrant init`.
2. Démarrer et accéder à une machine virtuelle avec `vagrant up` et `vagrant ssh`.
3. Arrêter et détruire une VM avec `vagrant halt` et `vagrant destroy`.

Pratique ces commandes pour te familiariser avec l'environnement Vagrant. 🚀

---

### 🎯 **Prochaines étapes**

Passez au **Lab 2**

---

**🚀 Bon apprentissage !**
