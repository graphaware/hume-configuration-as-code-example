# Config As Code Hume Demo

## Setup

- Rename the `.env.template` file to `.env`
- Replace the `<LICENCE_KEY_STRING>` in the `.env` file with your Hume licence key.
- Run `docker-compose up -d`

After running `docker-compose up -d` you will have : 

- Neo4j configured
- Hume pre-configured with the movies KG, roles, a GraphQL Api Key and actions

## Roles

### Admin

Administrator Role

Roles in Hume : `USER`, `ADMINISTRATOR`
Roles in Neo4j : `ADMIN`

### Investigator

Purpose is access to all the data but not admin, also should manage KG

Roles in Hume : `USER`, `INVESTIGATOR`
Roles in Neo4j : `INVESTIGATOR`

### Analyst

Limited access to data, in this example cannot access `Person(born)` property

Roles in Hume : `USER`, `ANALYST`
Roles in Neo4j : `ANALYST`

Denied access to `Person(born)`

## Users

The following users are automatically created : 

Admin : `admin@hume.ga` / `password`
Investigator : `investigator@hume.ga` / `investigator`
Analyst : `analyst@hume.ga` / `analyst`
