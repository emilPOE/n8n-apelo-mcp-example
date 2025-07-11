# 🏢 Inventory Tools

Tools for managing properties, units, unit groups, and attributes.

**Total Tools:** 32

## Inventory Groups

<details>
<summary>`HEAD` <strong>CheckUnitGroupExists</strong></summary>

### 📖 Description
Check if a unit group exists by ID.

### 🔗 API Endpoint
- **Method:** HEAD
- **Path:** `/inventory/v1/unit-groups/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>CountUnitGroups</strong></summary>

### 📖 Description
Get the count of unit groups.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/inventory/v1/unit-groups/$count`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ❌ | The property ID |
| `UnitGroupTypes` | `str` | ❌ | Filter by unit group types |

</details>

<details>
<summary>`POST` <strong>CreateUnitGroup</strong></summary>

### 📖 Description
Create a new unit group.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/inventory/v1/unit-groups`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`DELETE` <strong>DeleteUnitGroup</strong></summary>

### 📖 Description
Delete a unit group by ID.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/inventory/v1/unit-groups/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>GetUnitGroup</strong></summary>

### 📖 Description
Get a unit group by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/inventory/v1/unit-groups/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `Languages` | `str` | ❌ | 'all' or comma separated list of two-letter language codes (ISO Alpha-2) |

</details>

<details>
<summary>`GET` <strong>ListUnitGroups</strong></summary>

### 📖 Description
Get a list of unit groups, optionally filtered by property.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/inventory/v1/unit-groups`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyId` | `str` | ❌ | The property ID |
| `UnitGroupTypes` | `str` | ❌ | Filter by unit group types |

</details>

<details>
<summary>`PUT` <strong>UpdateUnitGroup</strong></summary>

### 📖 Description
Update a unit group with new data.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/inventory/v1/unit-groups/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

## 🏢 Properties

<details>
<summary>`PUT` <strong>ArchiveProperty</strong></summary>

### 📖 Description
Archive a property.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/inventory/v1/property-actions/{id}/archive`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`HEAD` <strong>CheckPropertyExists</strong></summary>

### 📖 Description
Check if a property exists by ID.

### 🔗 API Endpoint
- **Method:** HEAD
- **Path:** `/inventory/v1/properties/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`POST` <strong>CloneProperty</strong></summary>

### 📖 Description
Clone an existing property with new settings.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/inventory/v1/property-actions/{id}/clone`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`GET` <strong>CountProperties</strong></summary>

### 📖 Description
Get the total count of properties.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/inventory/v1/properties/$count`

</details>

<details>
<summary>`POST` <strong>CreateProperty</strong></summary>

### 📖 Description
Create a new property.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/inventory/v1/properties`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`GET` <strong>GetProperty</strong></summary>

### 📖 Description
Get a property by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/inventory/v1/properties/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `Languages` | `str` | ❌ | 'all' or comma separated list of two-letter language codes (ISO Alpha-2) |

</details>

<details>
<summary>`GET` <strong>ListProperties</strong></summary>

### 📖 Description
Get a list of properties.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/inventory/v1/properties`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `CountryCode` | `str` | ❌ | Filter by country code |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `IncludeArchived` | `str` | ❌ | Include archived items in the result |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `Status` | `str` | ❌ | Filter by status |

</details>

<details>
<summary>`PUT` <strong>ResetProperty</strong></summary>

### 📖 Description
Reset a test property and delete all transactional data.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/inventory/v1/property-actions/{id}/reset`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`PUT` <strong>SetPropertyLive</strong></summary>

### 📖 Description
Move a property to live status.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/inventory/v1/property-actions/{id}/set-live`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`PATCH` <strong>UpdateProperty</strong></summary>

### 📖 Description
Update a property using JSON patch operations.

### 🔗 API Endpoint
- **Method:** PATCH
- **Path:** `/inventory/v1/properties/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

## 🏠 Units

<details>
<summary>`HEAD` <strong>CheckUnitAttributeExists</strong></summary>

### 📖 Description
Check if a unit attribute exists by ID.

### 🔗 API Endpoint
- **Method:** HEAD
- **Path:** `/inventory/v1/unit-attributes/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`HEAD` <strong>CheckUnitExists</strong></summary>

### 📖 Description
Check if a unit exists by ID.

### 🔗 API Endpoint
- **Method:** HEAD
- **Path:** `/inventory/v1/units/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>CountUnits</strong></summary>

### 📖 Description
Get the count of units matching the specified filters.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/inventory/v1/units/$count`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Condition` | `str` | ❌ | Return units with a specific condition |
| `IsOccupied` | `bool` | ❌ | Return only occupied or vacant units |
| `MaintenanceType` | `str` | ❌ | Return units with the specific maintenance type |
| `PropertyId` | `str` | ❌ | The property ID |
| `TextSearch` | `str` | ❌ | Free text search |
| `UnitAttributeIds` | `str` | ❌ | Filter by unit attribute IDs |
| `UnitGroupId` | `str` | ❌ | The unit group ID |
| `UnitGroupIds` | `list[str]` | ❌ | Filter by unit group IDs |

</details>

<details>
<summary>`POST` <strong>CreateMultipleUnits</strong></summary>

### 📖 Description
Create multiple units in a single request.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/inventory/v1/units/bulk`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreateUnit</strong></summary>

### 📖 Description
Update a new unit.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/inventory/v1/units`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreateUnitAttribute</strong></summary>

### 📖 Description
Update a new unit attribute.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/inventory/v1/unit-attributes`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`DELETE` <strong>DeleteUnit</strong></summary>

### 📖 Description
Delete a unit by ID.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/inventory/v1/units/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`DELETE` <strong>DeleteUnitAttribute</strong></summary>

### 📖 Description
Delete a unit attribute by ID.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/inventory/v1/unit-attributes/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>GetUnit</strong></summary>

### 📖 Description
Get a unit by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/inventory/v1/units/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `Languages` | `str` | ❌ | 'all' or comma separated list of two-letter language codes (ISO Alpha-2) |

</details>

<details>
<summary>`GET` <strong>GetUnitAttribute</strong></summary>

### 📖 Description
Get a unit attribute by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/inventory/v1/unit-attributes/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>ListUnitAttributes</strong></summary>

### 📖 Description
Get a list of unit attributes.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/inventory/v1/unit-attributes`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |

</details>

<details>
<summary>`GET` <strong>ListUnits</strong></summary>

### 📖 Description
Get a list of units with various filtering options.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/inventory/v1/units`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Condition` | `str` | ❌ | Return units with a specific condition |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `IsOccupied` | `bool` | ❌ | Return only occupied or vacant units |
| `MaintenanceType` | `str` | ❌ | Return units with the specific maintenance type |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyId` | `str` | ❌ | The property ID |
| `TextSearch` | `str` | ❌ | Free text search |
| `UnitAttributeIds` | `str` | ❌ | Filter by unit attribute IDs |
| `UnitGroupId` | `str` | ❌ | The unit group ID |
| `UnitGroupIds` | `list[str]` | ❌ | Filter by unit group IDs |

</details>

<details>
<summary>`PATCH` <strong>UpdateMultipleUnits</strong></summary>

### 📖 Description
Update multiple units with the same patch operations.

### 🔗 API Endpoint
- **Method:** PATCH
- **Path:** `/inventory/v1/units`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `unitIds` | `list[str]` | ✅ | Filter by unit IDs |

</details>

<details>
<summary>`PATCH` <strong>UpdateUnit</strong></summary>

### 📖 Description
Update a unit using JSON patch operations.

### 🔗 API Endpoint
- **Method:** PATCH
- **Path:** `/inventory/v1/units/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

<details>
<summary>`PATCH` <strong>UpdateUnitAttribute</strong></summary>

### 📖 Description
Update a unit attribute using JSON patch operations.

### 🔗 API Endpoint
- **Method:** PATCH
- **Path:** `/inventory/v1/unit-attributes/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

