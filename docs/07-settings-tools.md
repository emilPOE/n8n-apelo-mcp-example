# ⚙️ Settings Tools

Tools for configuring property settings, policies, and system preferences.

**Total Tools:** 28

## Settings Capture Policies

<details>
<summary>`GET` <strong>GetCapturePolicy</strong></summary>

### 📖 Description
Get a specific capture policy by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/capture-policies/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>ListCapturePolicies</strong></summary>

### 📖 Description
Get a list of capture policies.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/capture-policies`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyId` | `str` | ❌ | The property ID |

</details>

## Settings City Tax

<details>
<summary>`POST` <strong>CreateCityTax</strong></summary>

### 📖 Description
Create a new city tax configuration.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/settings/v1/city-tax`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`DELETE` <strong>DeleteCityTax</strong></summary>

### 📖 Description
Delete a city tax configuration by ID.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/settings/v1/city-tax/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>GetCityTax</strong></summary>

### 📖 Description
Get a specific city tax configuration by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/city-tax/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `Languages` | `str` | ❌ | 'all' or comma separated list of two-letter language codes (ISO Alpha-2) |

</details>

<details>
<summary>`GET` <strong>ListCityTaxes</strong></summary>

### 📖 Description
Get a list of city tax configurations.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/city-tax`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ❌ | The property ID |

</details>

## Settings Features

<details>
<summary>`GET` <strong>GetFeatureSettings</strong></summary>

### 📖 Description
Get feature settings for a property.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/features/{propertyId}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |

</details>

## Settings Invoices

<details>
<summary>`GET` <strong>ListInvoiceAddresses</strong></summary>

### 📖 Description
Get invoice addresses for properties.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/invoice-address`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyIds` | `list[str]` | ❌ | Return market segments with any of the specified property ids. |

</details>

<details>
<summary>`PUT` <strong>UpdateInvoiceAddresses</strong></summary>

### 📖 Description
Update or update invoice addresses for one or more properties.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/settings/v1/invoice-address`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `propertyIds` | `list[str]` | ✅ | Return market segments with any of the specified property ids. |

</details>

## Settings Languages

<details>
<summary>`GET` <strong>ListLanguageSettings</strong></summary>

### 📖 Description
Get the language settings for the account.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/languages`

</details>

<details>
<summary>`PUT` <strong>UpdateLanguageSettings</strong></summary>

### 📖 Description
Update the language settings for the account.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/settings/v1/languages`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

## Settings Market Segments

<details>
<summary>`HEAD` <strong>CheckMarketSegmentExists</strong></summary>

### 📖 Description
Check if a market segment exists.

### 🔗 API Endpoint
- **Method:** HEAD
- **Path:** `/settings/v1/market-segments/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>CountMarketSegments</strong></summary>

### 📖 Description
Get the count of market segments.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/market-segments/$count`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyIds` | `list[str]` | ❌ | Return market segments with any of the specified property ids. |

</details>

<details>
<summary>`POST` <strong>CreateMarketSegment</strong></summary>

### 📖 Description
Create a new market segment.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/settings/v1/market-segments`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`DELETE` <strong>DeleteMarketSegment</strong></summary>

### 📖 Description
Delete a market segment by ID.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/settings/v1/market-segments/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>GetMarketSegment</strong></summary>

### 📖 Description
Get a specific market segment by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/market-segments/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>ListMarketSegments</strong></summary>

### 📖 Description
Get a list of market segments, filtered by the specified parameters.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/market-segments`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyIds` | `list[str]` | ❌ | Return market segments with any of the specified property ids. |

</details>

## Settings Properties

<details>
<summary>`POST` <strong>CreateTimeSliceDefinition</strong></summary>

### 📖 Description
Create a new time slice definition for a property.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/settings/v1/properties/{propertyId}/time-slice-definitions`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `propertyId` | `str` | ✅ | The property ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`DELETE` <strong>DeleteTimeSliceDefinition</strong></summary>

### 📖 Description
Delete a specific time slice definition.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/settings/v1/properties/{propertyId}/time-slice-definitions/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `PropertyId` | `str` | ✅ | The property ID |

</details>

<details>
<summary>`GET` <strong>GetPropertySettings</strong></summary>

### 📖 Description
Get property settings by property ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/properties/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>GetTimeSliceDefinition</strong></summary>

### 📖 Description
Get a specific time slice definition by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/properties/{propertyId}/time-slice-definitions/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `PropertyId` | `str` | ✅ | The property ID |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |

</details>

<details>
<summary>`GET` <strong>ListTimeSliceDefinitions</strong></summary>

### 📖 Description
Get a list of time slice definitions for a property.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/properties/{propertyId}/time-slice-definitions`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |

</details>

## Settings Sub Accounts

<details>
<summary>`HEAD` <strong>CheckSubAccountExists</strong></summary>

### 📖 Description
Check if a sub-account exists.

### 🔗 API Endpoint
- **Method:** HEAD
- **Path:** `/settings/v1/sub-accounts/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>CountSubAccounts</strong></summary>

### 📖 Description
Get the count of sub-accounts for a property.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/sub-accounts/$count`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |

</details>

<details>
<summary>`POST` <strong>CreateSubAccount</strong></summary>

### 📖 Description
Create a new custom sub-account.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/settings/v1/sub-accounts`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`DELETE` <strong>DeleteSubAccount</strong></summary>

### 📖 Description
Delete a custom sub-account by ID.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/settings/v1/sub-accounts/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>GetSubAccount</strong></summary>

### 📖 Description
Get a specific sub-account by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/sub-accounts/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>ListSubAccounts</strong></summary>

### 📖 Description
Get a list of sub-accounts for a property.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/sub-accounts`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |

</details>

