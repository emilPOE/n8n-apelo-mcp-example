# 💵 Rate Plan Tools

Tools for managing rate plans, services, and pricing strategies.

**Total Tools:** 35

## Rateplan Cancellation Policies

<details>
<summary>`POST` <strong>CreateCancellationPolicy</strong></summary>

### 📖 Description
Create a new cancellation policy.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/rateplan/v1/cancellation-policies`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`DELETE` <strong>DeleteCancellationPolicy</strong></summary>

### 📖 Description
Delete a cancellation policy by ID.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/rateplan/v1/cancellation-policies/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>GetCancellationPolicy</strong></summary>

### 📖 Description
Get a cancellation policy by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/rateplan/v1/cancellation-policies/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `Languages` | `str` | ❌ | 'all' or comma separated list of two-letter language codes (ISO Alpha-2) |

</details>

<details>
<summary>`GET` <strong>ListCancellationPolicies</strong></summary>

### 📖 Description
Get a list of cancellation policies.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/rateplan/v1/cancellation-policies`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyId` | `str` | ❌ | The property ID |

</details>

## Rateplan Companies

<details>
<summary>`POST` <strong>CreateCompany</strong></summary>

### 📖 Description
Create a new company.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/rateplan/v1/companies`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`DELETE` <strong>DeleteCompany</strong></summary>

### 📖 Description
Delete a company by ID.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/rateplan/v1/companies/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>GetCompany</strong></summary>

### 📖 Description
Get a company by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/rateplan/v1/companies/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>ListCompanies</strong></summary>

### 📖 Description
Get a list of companies.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/rateplan/v1/companies`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `CorporateCodes` | `str` | ❌ | Return companies that have any of the requested corporate codes |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyId` | `str` | ❌ | The property ID |
| `RatePlanIds` | `str` | ❌ | Return rate plans with any of the specified IDs |
| `TextSearch` | `str` | ❌ | Free text search |

</details>

## Rateplan Corporate Codes

<details>
<summary>`GET` <strong>ListCorporateCodes</strong></summary>

### 📖 Description
Get a list of corporate codes.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/rateplan/v1/corporate-codes/codes`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyId` | `str` | ❌ | The property ID |

</details>

## Rateplan No Show Policies

<details>
<summary>`POST` <strong>CreateNoShowPolicy</strong></summary>

### 📖 Description
Create a new no-show policy.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/rateplan/v1/no-show-policies`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`DELETE` <strong>DeleteNoShowPolicy</strong></summary>

### 📖 Description
Delete a no-show policy by ID.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/rateplan/v1/no-show-policies/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>GetNoShowPolicy</strong></summary>

### 📖 Description
Get a no-show policy by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/rateplan/v1/no-show-policies/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `Languages` | `str` | ❌ | 'all' or comma separated list of two-letter language codes (ISO Alpha-2) |

</details>

<details>
<summary>`GET` <strong>ListNoShowPolicies</strong></summary>

### 📖 Description
Get a list of no-show policies.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/rateplan/v1/no-show-policies`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyId` | `str` | ❌ | The property ID |

</details>

## Rateplan Promo Codes

<details>
<summary>`GET` <strong>ListPromoCodes</strong></summary>

### 📖 Description
Get a list of promo codes.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/rateplan/v1/promo-codes/codes`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyId` | `str` | ❌ | The property ID |

</details>

## Rateplan Rateplans

<details>
<summary>`HEAD` <strong>CheckRatePlanExists</strong></summary>

### 📖 Description
Check if a rate plan exists.

### 🔗 API Endpoint
- **Method:** HEAD
- **Path:** `/rateplan/v1/rate-plans/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>CountRatePlans</strong></summary>

### 📖 Description
Get the count of rate plans matching the specified filters.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/rateplan/v1/rate-plans/$count`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `BaseRatePlanIds` | `str` | ❌ | Return rate plans derived from any of the specified rate plans |
| `CancellationPolicyIds` | `str` | ❌ | Return rate plans with any of the specified cancellation policies |
| `ChannelCodes` | `str` | ❌ | The channel codes used to filter the retrieved data |
| `CompanyIds` | `list[str]` | ❌ | Company IDs the report should be generated for |
| `DerivationLevelFilter` | `str` | ❌ | This will filter rate plans based on their derivation level. |
| `IncludedServiceIds` | `str` | ❌ | Return rate plans that have any of the requested included services |
| `IsDerived` | `str` | ❌ | Return only derived or base rate plans |
| `MinGuaranteeTypes` | `str` | ❌ | Return rate plans with any of the specified min guarantee types |
| `NoShowPolicyIds` | `str` | ❌ | Return rate plans with any of the specified no-show policies |
| `PromoCodes` | `str` | ❌ | Return rate plans that have any of the requested promo codes |
| `PropertyId` | `str` | ❌ | The property ID |
| `RatePlanCodes` | `str` | ❌ | Return rate plans filtered by requested codes |
| `TimeSliceDefinitionIdsDateGeneric` | `str` | ❌ | Time slice definition IDs to filter by |
| `TimeSliceTemplateDateGeneric` | `str` | ❌ | Time slice template to use |
| `UnitGroupIds` | `list[str]` | ❌ | Filter by unit group IDs |
| `UnitGroupTypes` | `str` | ❌ | Filter by unit group types |

</details>

<details>
<summary>`GET` <strong>CountRates</strong></summary>

### 📖 Description
Get the count of rates for a rate plan within a specified time range.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/rateplan/v1/rate-plans/{id}/rates/$count`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `From` | `str` | ✅ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `To` | `str` | ✅ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |

</details>

<details>
<summary>`POST` <strong>CreateRatePlan</strong></summary>

### 📖 Description
Create a new rate plan.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/rateplan/v1/rate-plans`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`DELETE` <strong>DeleteRatePlan</strong></summary>

### 📖 Description
Delete a rate plan by ID.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/rateplan/v1/rate-plans/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`DELETE` <strong>DeleteRatePlans</strong></summary>

### 📖 Description
Delete multiple rate plans.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/rateplan/v1/rate-plans`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `RatePlanIds` | `str` | ✅ | Return rate plans with any of the specified IDs |

</details>

<details>
<summary>`GET` <strong>GetRatePlan</strong></summary>

### 📖 Description
Get a rate plan by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/rateplan/v1/rate-plans/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `Languages` | `str` | ❌ | 'all' or comma separated list of two-letter language codes (ISO Alpha-2) |

</details>

<details>
<summary>`GET` <strong>GetRates</strong></summary>

### 📖 Description
Get a list of rates for a rate plan within a specified time range.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/rateplan/v1/rate-plans/{id}/rates`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `From` | `str` | ✅ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `To` | `str` | ✅ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |

</details>

<details>
<summary>`GET` <strong>ListRatePlans</strong></summary>

### 📖 Description
Get a list of rate plans with extensive filtering options.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/rateplan/v1/rate-plans`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `BaseRatePlanIds` | `str` | ❌ | Return rate plans derived from any of the specified rate plans |
| `CancellationPolicyIds` | `str` | ❌ | Return rate plans with any of the specified cancellation policies |
| `ChannelCodes` | `str` | ❌ | The channel codes used to filter the retrieved data |
| `CompanyIds` | `list[str]` | ❌ | Company IDs the report should be generated for |
| `DerivationLevelFilter` | `str` | ❌ | This will filter rate plans based on their derivation level. |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `IncludedServiceIds` | `str` | ❌ | Return rate plans that have any of the requested included services |
| `IsDerived` | `str` | ❌ | Return only derived or base rate plans |
| `MinGuaranteeTypes` | `str` | ❌ | Return rate plans with any of the specified min guarantee types |
| `NoShowPolicyIds` | `str` | ❌ | Return rate plans with any of the specified no-show policies |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PromoCodes` | `str` | ❌ | Return rate plans that have any of the requested promo codes |
| `PropertyId` | `str` | ❌ | The property ID |
| `RatePlanCodes` | `str` | ❌ | Return rate plans filtered by requested codes |
| `TimeSliceDefinitionIdsDateGeneric` | `str` | ❌ | Time slice definition IDs to filter by |
| `TimeSliceTemplateDateGeneric` | `str` | ❌ | Time slice template to use |
| `UnitGroupIds` | `list[str]` | ❌ | Filter by unit group IDs |
| `UnitGroupTypes` | `str` | ❌ | Filter by unit group types |

</details>

<details>
<summary>`PUT` <strong>UpdateRatePlan</strong></summary>

### 📖 Description
Update a rate plan.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/rateplan/v1/rate-plans/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

<details>
<summary>`PUT` <strong>UpdateRates</strong></summary>

### 📖 Description
Initialize and change the rates for a rate plan.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/rateplan/v1/rate-plans/{id}/rates`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

## Rateplan Rates

<details>
<summary>`DELETE` <strong>DeleteRates</strong></summary>

### 📖 Description
Delete all rates for a rate plan within a specified date range.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/rateplan/v1/rates`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `From` | `str` | ✅ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `To` | `str` | ✅ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |

</details>

## Rateplan Services

<details>
<summary>`GET` <strong>CountServices</strong></summary>

### 📖 Description
Get the count of services.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/rateplan/v1/services/$count`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `ChannelCodes` | `str` | ❌ | The channel codes used to filter the retrieved data |
| `OnlySoldAsExtras` | `str` | ❌ | If set to true, return only services that can be sold as extras. Otherwise, it returns both, extras, and include-only. |
| `PropertyId` | `str` | ❌ | The property ID |
| `ServiceTypes` | `str` | ❌ | Filter by service types |
| `TextSearch` | `str` | ❌ | Free text search |

</details>

<details>
<summary>`POST` <strong>CreateService</strong></summary>

### 📖 Description
Create a new service.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/rateplan/v1/services`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`DELETE` <strong>DeleteService</strong></summary>

### 📖 Description
Delete a service by ID.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/rateplan/v1/services/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>GetService</strong></summary>

### 📖 Description
Get a service by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/rateplan/v1/services/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `Languages` | `str` | ❌ | 'all' or comma separated list of two-letter language codes (ISO Alpha-2) |

</details>

<details>
<summary>`GET` <strong>ListServices</strong></summary>

### 📖 Description
Get a list of services.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/rateplan/v1/services`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `ChannelCodes` | `str` | ❌ | The channel codes used to filter the retrieved data |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `OnlySoldAsExtras` | `str` | ❌ | If set to true, return only services that can be sold as extras. Otherwise, it returns both, extras, and include-only. |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyId` | `str` | ❌ | The property ID |
| `ServiceTypes` | `str` | ❌ | Filter by service types |
| `TextSearch` | `str` | ❌ | Free text search |

</details>

## Settings Age Categories

<details>
<summary>`POST` <strong>CreateAgeCategory</strong></summary>

### 📖 Description
Create a new age category.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/settings/v1/age-categories`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`DELETE` <strong>DeleteAgeCategory</strong></summary>

### 📖 Description
Delete an age category by ID.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/settings/v1/age-categories/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>GetAgeCategory</strong></summary>

### 📖 Description
Get an age category by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/age-categories/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `Languages` | `str` | ❌ | 'all' or comma separated list of two-letter language codes (ISO Alpha-2) |

</details>

<details>
<summary>`GET` <strong>ListAgeCategories</strong></summary>

### 📖 Description
Get a list of age categories for a property.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/settings/v1/age-categories`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |

</details>

