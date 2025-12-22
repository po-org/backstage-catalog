# 🎒 Backstage Catalog

Centralized **Backstage Catalog definitions** for our platform ecosystem.

This repository is the **single source of truth** for all entities registered in Backstage — services, systems, domains, teams, resources, templates, and more.  
If it shows up in Backstage, it lives here.

---

## 📌 What This Repo Is

This repository contains **YAML entity definitions** used by Backstage to:

- Power the **Software Catalog**
- Enable **ownership, discovery, and lifecycle management**
- Standardize how we describe services, systems, and teams
- Provide reusable **Scaffolder templates**

Think of this as the **directory + map** of our internal tech landscape.

---

## 🧱 Repository Structure
```
├── api/ # API entities
├── component/ # Services, libraries, jobs, websites
├── domain/ # Business and technical domains
├── group/ # Teams, squads, org units
├── location/ # Location aggregators
├── resource/ # Databases, queues, buckets, etc.
├── system/ # Systems that group components
├── template/ # Backstage scaffolder templates
├── user/ # Users (if managed via catalog)
└── README.md
```

Each directory contains one or more `*.yaml` files defining Backstage entities.

---

## 🧩 Supported Entity Kinds

This repo currently supports (and expects):

- `Component`
- `API`
- `System`
- `Domain`
- `Resource`
- `Group`
- `User`
- `Location`
- `Template`

All entities should follow Backstage’s official schemas and internal conventions.

---

## 🚀 How This Is Used

1. Backstage is configured to ingest this repo via **Locations**
2. Changes merged to `main` are automatically picked up
3. Entities become visible, searchable, and linkable in Backstage
4. Ownership, dependencies, and lifecycle data stay consistent

---

## ✍️ Adding or Updating Entities

### Add a new entity

1. Create a new YAML file in the appropriate folder
2. Follow existing examples for structure and metadata
3. Ensure:
   - `metadata.name` is unique
   - `spec.owner` is set correctly
   - Relationships are accurate

### Update an existing entity

- Edit the relevant YAML file
- Keep changes focused and intentional
- Avoid breaking references used by other entities

---

## 🧪 Validation & Conventions

While Backstage does schema validation at runtime, contributors should:

- Keep files **small and readable**
- Prefer **one entity per file**
- Use consistent naming and labeling
- Avoid copying entities without updating ownership and IDs

(Automated linting/validation may be added later.)


---


Each top-level folder maps directly to a Backstage entity kind:

