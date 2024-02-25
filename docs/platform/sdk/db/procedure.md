# Procedure

## Overview

The provided TypeScript module `Procedure` facilitates the execution of stored procedures in a database. It includes methods for creating and executing stored procedures.

Here's an explanation of the key components:

## ProcedureParameter Interface:

```javascript
export interface ProcedureParameter {
	readonly type: string;
	readonly value: any;
}
```

This interface represents a parameter that can be used in a stored procedure call. It includes the `type` of the parameter (string) and its `value` (any).

## Procedure Class:

The `Procedure`` class provides static methods for creating and executing stored procedures.


### Methods:

#### create

```javascript
create(sql: string, datasourceName?: string): void
```

Creates a stored procedure using an Update operation. (Assumed to be part of the Update class, as Update.execute is used.)

**Parameters:**

* `sql`: The SQL statement for creating the stored procedure.
* `datasourceName`: (Optional) The name of the data source.

#### execute

```javascript
execute(sql: string, parameters: (string | number | ProcedureParameter)[] = [], datasourceName?: string): any[]
```

Executes a stored procedure and returns the result sets.

**Parameters:**

* `sql`: The SQL statement for executing the stored procedure.
* `parameters`: (Optional) An array of parameters to be included in the stored procedure call. Parameters can be of type string, number, or an object conforming to the ProcedureParameter interface.
* `datasourceName`: (Optional) The name of the data source.
* Return Value: An array containing the result sets of the stored procedure execution.

## Example Usage:

### Call Procedure

```javascript
import { Procedure, ProcedureParameter } from 'sdk/db/procedure';

// Example SQL stored procedure call
const sql = 'CALL your_procedure(?, ?)';

// Example parameters
const parameters: (string | number | ProcedureParameter)[] = [
  'value1',
  42,
  { type: 'custom', value: 'custom value' } as ProcedureParameter
];

// Execute the stored procedure
const result = Procedure.execute(sql, parameters, 'yourDataSource');

console.log('Stored Procedure Result:', result);
```

Replace `your_procedure`, `value1`, `42`, `custom value`, `yourDataSource`, and other placeholders with your actual module path, stored procedure name, values, data source
