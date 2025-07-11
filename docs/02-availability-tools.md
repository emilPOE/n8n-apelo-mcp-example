# 📅 Availability Tools

Tools for checking and managing unit and service availability.

**Total Tools:** 5

## Availability Groups

<details>
<summary>`GET` <strong>GetAvailableUnitGroups</strong></summary>

### 📖 Description
Get a list of all available unit groups in a property for a specific time period.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/availability/v1/unit-groups`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |
| `From` | `str` | ✅ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `To` | `str` | ✅ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `Adults` | `int` | ❌ | Number of adults |
| `ChildrenAges` | `list[int]` | ❌ | Ages of children |
| `OnlySellable` | `str` | ❌ | When set to 'true', only the unit groups sold by the specified time slice template and time slice definition ids are returned, otherwise all unit groups are returned |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `TimeSliceDefinitionIdsDateGeneric` | `str` | ❌ | Time slice definition IDs to filter by |
| `TimeSliceTemplateDateGeneric` | `str` | ❌ | Time slice template to use |
| `UnitGroupIds` | `list[str]` | ❌ | Filter by unit group IDs |
| `UnitGroupTypes` | `str` | ❌ | Filter by unit group types |

</details>

<details>
<summary>`PATCH` <strong>UpdateUnitGroupAvailability</strong></summary>

### 📖 Description
Modify the availability settings for a unit group using JSON patch operations.

### 🔗 API Endpoint
- **Method:** PATCH
- **Path:** `/availability/v1/unit-groups/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `From` | `str` | ✅ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `timeSliceTemplateDateGeneric` | `str` | ✅ | Time slice template to use |
| `To` | `str` | ✅ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |

</details>

## Availability Reservations

<details>
<summary>`GET` <strong>GetAvailableUnitsForReservation</strong></summary>

### 📖 Description
Get a list of all available units for a specific reservation.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/availability/v1/reservations/{id}/units`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `From` | `str` | ❌ | Start date and time for filtering or time range queries. Specify a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `IncludeOutOfService` | `str` | ❌ | Should units that are set OutOfService in the defined time period be returned as available. |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `To` | `str` | ❌ | End date and time for filtering or time range queries. Specify a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `UnitAttributeIds` | `str` | ❌ | Filter by unit attribute IDs |
| `UnitCondition` | `str` | ❌ | Filter by unit condition |
| `UnitGroupId` | `str` | ❌ | The unit group ID |

</details>

## Availability Services

<details>
<summary>`GET` <strong>GetAvailableServices</strong></summary>

### 📖 Description
Get a list of all available services in a property for a specific time period.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/availability/v1/services`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |
| `From` | `str` | ✅ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `To` | `str` | ✅ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `ChannelCodes` | `str` | ❌ | The channel codes used to filter the retrieved data |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `TimeSliceDefinitionIdsDateGeneric` | `str` | ❌ | Time slice definition IDs to filter by |
| `TimeSliceTemplateDateGeneric` | `str` | ❌ | Time slice template to use |

</details>

## Availability Units

<details>
<summary>`GET` <strong>GetAvailableUnits</strong></summary>

### 📖 Description
Get a list of all available units in a property for a specific time period.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/availability/v1/units`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |
| `From` | `str` | ✅ | Start date and time for filtering or time range queries. Specify a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `To` | `str` | ✅ | End date and time for filtering or time range queries. Specify a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `IncludeOutOfService` | `str` | ❌ | Should units that are set OutOfService in the defined time period be returned as available. |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `UnitAttributeIds` | `str` | ❌ | Filter by unit attribute IDs |
| `UnitCondition` | `str` | ❌ | Filter by unit condition |
| `UnitGroupId` | `str` | ❌ | The unit group ID |

</details>

