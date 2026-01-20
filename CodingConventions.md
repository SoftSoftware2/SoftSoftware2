# Code Conventions – Fleetly

> **Objectiu**: Definir unes normes clares i consensuades perquè tot l’equip desenvolupi codi **llegible, mantenible, escalable i segur**.
>
---

## 1. Informació general del projecte
- **Nom del projecte**: Fleetly
- **Tecnologies principals** (frontend, backend, BD, etc.): 
    - **Frontend**: VUE
    - **Backend**: Laravel
    - **SGBD**: PostgreSQL, Pgadmin.
    
- **Versió del llenguatge**:
- **Responsables de les convencions**: Jordi Arnau, Francesc Quintó i Iker Vericat.
- **Data d’última revisió**: 20/01/2026

---

## 2. Principis generals
- **Prioritat**: llegibilitat i optimització
- **Enfocament** (clean code, domain-driven, component-based, etc.)
- **Regles generals aplicables a tot el projecte**:
    - Llenguatge en inglès
    - Pocs comentaris
    - Comentaris breus
    - Treballar en la metodologia SCRUM.

---

## 3. Estructura del projecte
- Estructura:
  - Frontend: 
    - Ha de tindre el seu propi repositori
    - Utilitzarem una arquitectura modular. 
    - Funció principal: Mostrar les vistes formatades i capturar les dades de l'usuari  
  - Backend: 
    - Ha de tindre el seu propi repositori
    - Utilitzarem una arquitectura modular.
    - Funció: Gestionar la comunicació, processar dades i validar usuaris.
- Fitxers obligatoris (README, .env.example, etc.)

---

## 4. Convencions de nomenclatura
### 4.1 Fitxers i carpetes
- Estil:
    - Noms arxius: PascalCase
    - Nom variables: camelCase
    - Nom funcions: camelCase
    - Nom constants: SCREAMING_SNAKE_CASE
    - Rutes: kebab-case
    - Carpetes: snake_case
    - Taules i Noms DB: snake_case
- Prefixos / sufixos permesos:
    - FrontEnd:    
        - Composables: use -> useAuth.ts
        - Views: Page -> LoginPage.vue
        - Interfaces: .interfaces. -> users.interfaces.ts 
    - BackEnd:
        - Controllers: Controller -> AuthController.php

### 4.2 Variables
- Idioma: anglès
- Semàntica: noms descriptius (evitar x, y) excepte iteradors.
- Booleans: Han de portar prefix (is, has, can..)
### 4.3 Funcions i mètodes
- Verb + acció. Exemple (getVehicleLocation(), storeCoordinate(), calculateDistance())
- Longitud màxima recomanada: 20-30 linies

### 4.4 Classes i components
- Patró de noms: PascalCase
- Singular

### 4.5 Constants
- Format: SCREAMING_SNAKE_CASE
- Ubicació
    - Laravel: (Model o /config)
    - VUE: fitxer dedicat @/constants/index.js / objecte "const"

---

## 5. Estil de codi
- Indentació (espais o tabuladors): 
- Mida de la indentació: 4 espais per a PHP (Laravel), 2 espais per a VUE i fitxers de configuració.
- Ús de línies en blanc: 
    - Una línia en blanc obligatòria entre cada mètode o funció dins d'una classe.
    - Final de fitxer: Una linia en blanc

---

## 6. Comentaris i documentació
- Comentaris breus únicament per entendre fragments de codi complexos
- Format de comentaris
    - PHP i Typescript:
        /**
        * Calcula la distància total recorreguda per un vehicle.
        */
- Documentació en fitxers .md en un repositori a part.

---

## 7. Gestió de versions (Git)
### 7.1 Branca principal
- Nom de la branca principal: Main

### 7.2 Estratègia de branques
- Feature branches
    - feature/FT-1
- Hotfix
    - hotfix/problema_a_arreglar


### 7.3 Commits
- Format del missatge de commit: "Add/fix/bug: cualsevol cosa"
- Idioma dels commits: Anglès
- Exemples de bons commits: Breus

### 7.4 Pull Requests / Merge Requests
- Requisits mínims
    - Titol descriptiu
    - Descripció clara
    - Codi lliure de warnings
- Reviews obligatòries
    - Compliment de les coding conventions
- Regles abans de fer merge
    - Passar els tests CI
    - Resolució de conflictes

---

## 10. Seguretat
- Gestió de secrets i variables d’entorn
- Protecció contra atacs comuns (XSS, CSRF, SQL Injection, etc.)
- Autenticació i autorització
- Bones pràctiques de seguretat

---

## 11. Rendiment i optimització
- Bones pràctiques de rendiment
- Lazy loading
- Optimització d’imatges i assets
- Caching

---

> **Nota final**: Aquest document és viu i s’ha d’anar actualitzant segons l’evolució del projecte i de l’equip.
