# Data Access Object (DAO)

## Introduction

The provided code defines a Data Access Object (DAO) module in JavaScript/TypeScript for interfacing with a database. The module is intended to work with a specific Object-Relational Mapping (ORM) configuration.

Here's an overview of the main functionalities:

## DAO Constructor:

```javascript
export function DAO(orm, logCtxName, dataSourceName) { ... }
```

**Parameters:**

* `orm`: The Object-Relational Mapping configuration.
* `logCtxName`: (Optional) Log context name.
* `dataSourceName`: (Optional) Data source name.

## Methods

### execute(sqlBuilder, parameterBindings)

Executes SQL statements (select, insert, update) based on the provided SQL builder and parameter bindings.

**Parameters:**

* `sqlBuilder`: SQL statement builder.
* `parameterBindings`: Parameter bindings for the SQL statement.

### notify(event)

Notifies an event.

**Parameters:**

* `event`: Event to notify.

### createSQLEntity(entity)

Prepares a JSON object for insertion into the database.

### createEntity(resultSetEntry, entityPropertyNames)

Creates an entity as a JSON object from a ResultSet current row.

### validateEntity(entity, skip)

Validates the entity based on mandatory properties.

### insert(_entity)

Inserts an entity or an array of entities into the database.

### update(entity)

Updates an entity in the database.

### remove(...)

Deletes an entity by ID or an array of IDs, or deletes all entities.

### expand(expansionPath, context)

Expands an entity based on the provided expansion path and context.

### find(id, expand, select)

Reads a single entity by ID, parsed into a JSON object. It supports expansion and selection.

### count(settings)

Counts entities based on the provided settings.

### list(settings)

Lists entities based on the provided settings, supporting expansion and selection.

### existsTable()

Checks if the table associated with the ORM definition exists.

### createTable()

Creates the table associated with the ORM definition.

### dropTable(dropIdSequence)

Drops the table associated with the ORM definition, optionally dropping the ID sequence.

## Additional Functions:

### isNotEmptyArray(array)

Checks if an array is not empty.

### create(oDefinition, logCtxName, dataSourceName)

Creates a DAO instance based on the ORM definition.

### dao(oDefinition, logCtxName, dataSourceName)

Alias for the create function.

## Usage Example:

```javascript
import { dao } from 'sdk/db';

//create a DAO from configuration
const myDAO = dao.create({
    table: "CUSTOMERS",
    properties: [{
        name: "id",
        column: "ID",
        type: "BIGINT",
        id: true
    }, {
        name: "orgName",
        column: "ORG_NAME",
        type: "VARCHAR",
        required: true
    }, {
        name: "employeesNumber",
        column: "ORG_EMP_NUM",
        type: "INTEGER",
        required: true
    }, {
        name: "orgDescription",
        column: "ORG_DESCR",
        type: "VARCHAR",
        required: false
    }]
});

//Create CUSTOMERS table
myDAO.createTable();

try {

    //Create a new customer entity
    let customerId = myDAO.insert({
        orgName: "ACME",
        employeesNumber: 1000
    });

    //List all customer entities
    let customersList = customers.list();

    //Get a particular customer entity by its id
    let customer = myDAO.find(customerId);

    //Update a customer entity property
    customer.orgDescription = "ACME is a company";
    myDAO.update(customer);

    //Delete a customer entity
    myDAO.remove(customerId);

} finally {
    //Drop CUSTOMERS table
    myDAO.dropTable();
}
// ... and more
```

Replace placeholder values with your actual module, ORM definition, log context, data source, and entity details.
