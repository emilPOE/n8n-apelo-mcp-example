# 🔧 Operations Tools

Tools for operational management and maintenance tasks.

**Total Tools:** 10

## Operations Maintenances

<details>
<summary>`HEAD` <strong>CheckMaintenanceExists</strong></summary>

### 📖 Description
Check if a maintenance exists by ID.

### 🔗 API Endpoint
- **Method:** HEAD
- **Path:** `/operations/v1/maintenances/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>CountMaintenances</strong></summary>

### 📖 Description
Get the count of maintenance windows.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/operations/v1/maintenances/$count`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `From` | `str` | ❌ | Start date and time for filtering or time range queries. Specify a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `PropertyId` | `str` | ❌ | The property ID |
| `To` | `str` | ❌ | End date and time for filtering or time range queries. Specify a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `Types` | `str` | ❌ | Filter by types |
| `UnitId` | `str` | ❌ | The unit ID |

</details>

<details>
<summary>`POST` <strong>CreateMaintenance</strong></summary>

### 📖 Description
Create a new maintenance window.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/operations/v1/maintenances`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreateMultipleMaintenances</strong></summary>

### 📖 Description
Create multiple maintenance windows.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/operations/v1/maintenances/bulk`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`DELETE` <strong>DeleteMaintenance</strong></summary>

### 📖 Description
Delete a maintenance by ID.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/operations/v1/maintenances/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>GetMaintenance</strong></summary>

### 📖 Description
Get a maintenance by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/operations/v1/maintenances/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |

</details>

<details>
<summary>`GET` <strong>ListMaintenances</strong></summary>

### 📖 Description
Get a list of maintenance windows.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/operations/v1/maintenances`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `From` | `str` | ❌ | Start date and time for filtering or time range queries. Specify a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyId` | `str` | ❌ | The property ID |
| `To` | `str` | ❌ | End date and time for filtering or time range queries. Specify a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `Types` | `str` | ❌ | Filter by types |
| `UnitId` | `str` | ❌ | The unit ID |

</details>

<details>
<summary>`PATCH` <strong>UpdateMaintenance</strong></summary>

### 📖 Description
Update a maintenance using JSON patch operations.

### 🔗 API Endpoint
- **Method:** PATCH
- **Path:** `/operations/v1/maintenances/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

## Operations Night Audit

<details>
<summary>`PUT` <strong>RunNightAudit</strong></summary>

### 📖 Description
Perform the night audit for one property.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/operations/v1/night-audit`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `propertyId` | `str` | ✅ | The property ID |
| `setReservationsToNoShow` | `str` | ❌ | If set to true, all reservations in group will be set to no-show |

</details>

## Operations Units

<details>
<summary>`PUT` <strong>UpdateUnitsCondition</strong></summary>

### 📖 Description
Change the condition of one or more units.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/operations/v1/units-condition`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

