# Project Data Nice

This is the journey for grasping the fundamentals of hows and whys of systems.

## Notes

I've used `uv` for managing packages, it's a good practice to keep it that way
but feel free to use raw python `venv` for running

## Requirements

- Data Lineage
- Data Validation
- Permissions (Role Based)

## Modules

- [Authentication](#authentication)
  - Users
  - Groups
  - Roles
  - API Keys
  - Tokens
- [Authorization](#authorization)
- [Catalog](#catalog)
- [Validation Engine](#validation-engine)
- [Storage](#storage)
  - Files
  - Database Records
  - (Even) Object Storages
- [Lineage](#lineage)
- [Query Engine](#query-engine)

## Authentication

- [ ] TODO

## Authorization

- [ ] TODO

## Catalog

- [ ] TODO
 
## Validation Engine

- [ ] TODO

# Storage

- [ ] TODO

# Lineage

Think of this layer as a (potentially) complex graphing system. for example:

```mermaid
flowchart LR
    file(customers.csv) --> clean(clean customers)
    clean --> features(customer features)
    features --> dashboard(dashboard)
```

But if we want to look as a system feature, we can look at it like

```mermaid
flowchart LR
    asset(Asset) --> transformation(Transformation)
    transformation --> input(Input)
    input --> output(Output)
```

# Query Engine

This is one of my favorite modules, where it's not just about executing 
queries, for our case it's matter of chain of responsibility like

```mermaid
flowchart LR
  check(Check Permission) --> inject(Inject Row Filters)
  inject --> remove(Remove Forbidden Rows)
  remove --> execute(Execute SQL)
  execute --> result(Voila!!!, Data is cooked)
```

## Contribution

You can see anything I come up in [CONTRIBUTION.md](CONTRIBUTION.md)