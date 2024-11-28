# Projekt inżynierski – Automatyzacja z użyciem Ansible

## Opis projektu

Projekt realizuje automatyzację zadań związanych z konfiguracją serwerów przy użyciu **Ansible**. Repozytorium zawiera role, playbooki oraz inne pliki niezbędne do zarządzania infrastrukturą.

---

## Struktura projektu

- **Ansible/**
  - **roles/** - Role Ansible (każdy node ma osobną rolę)
    - **node/** - Rola odpowiadająca danemu nodowi
      - **defaults/** - Domyślne zmienne dla roli
      - **tasks/** - Główne zadania wykonywane w ramach roli
      - _..._ - (inne katalogi roli, jeśli wymagane)
  - **inventory** - Plik zawierający listę hostów i grup
  - **vault.yml** - Plik z zaszyfrowanymi informacjami (Ansible Vault)
  - **playbook_<nazwa>.yml** - Główne playbooki uruchamiające role/nody
  - _..._ - Pozostałe pliki i katalogi

---

## Opis kluczowych elementów

- **`roles/`**  
  Zawiera role definiujące konfigurację dla poszczególnych nodów.  
  - `defaults/` – zmienne domyślne dla roli.  
  - `tasks/` – zadania wykonywane w ramach roli.  

- **`inventory`**  
  Lista hostów i grup hostów, na których wykonywane są operacje.

- **`vault.yml`**  
  Plik z wrażliwymi informacjami, zaszyfrowany przy użyciu Ansible Vault.

- **Playbooki**  
  Pliki `playbook_<nazwa>.yml` definiują zadania do wykonania na określonych hostach i grupach, korzystając z ról w `roles/`.

---