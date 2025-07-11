# 📊 Reports Tools

Tools for generating and retrieving various business reports.

**Total Tools:** 5

## Reports Reports

<details>
<summary>`GET` <strong>ListArrivalsReport</strong></summary>

### 📖 Description
Get a report of arrivals for a property in a specific month.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/reports/v1/reports/arrivals`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |
| `Month` | `int` | ✅ | Requested month for the report. |
| `Year` | `int` | ✅ | Requested year for the report. |

</details>

<details>
<summary>`GET` <strong>ListCompanyInvoicesVatReport</strong></summary>

### 📖 Description
Get a report of company invoices with VAT breakdown information.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/reports/v1/reports/company-invoices-vat`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |
| `CompanyIds` | `list[str]` | ❌ | Company IDs the report should be generated for |
| `DateFilterDateGeneric` | `str` | ❌ | Set a date interval to get the report for. Cannot be more than 1 month. You can provide an array of string expressions which all need to apply. |

</details>

<details>
<summary>`GET` <strong>ListOrderedServicesReport</strong></summary>

### 📖 Description
Get a report of ordered services for a property within a date range.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/reports/v1/reports/ordered-services`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |
| `From` | `str` | ✅ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `ServiceIds` | `str` | ✅ | Filter by service IDs |
| `To` | `str` | ✅ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |

</details>

<details>
<summary>`GET` <strong>ListPropertyPerformanceReport</strong></summary>

### 📖 Description
Get a property performance report including ADR and RevPAR for each business day.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/reports/v1/reports/property-performance`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |
| `From` | `str` | ✅ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `To` | `str` | ✅ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `ChannelCodes` | `str` | ❌ | The channel codes used to filter the retrieved data |
| `CompanyIds` | `list[str]` | ❌ | Company IDs the report should be generated for |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `MarketSegmentIds` | `str` | ❌ | Filter result by market segment IDs |
| `RatePlanIds` | `str` | ❌ | Return rate plans with any of the specified IDs |
| `TimeSliceDefinitionIdsDateGeneric` | `str` | ❌ | Time slice definition IDs to filter by |
| `TravelPurpose` | `str` | ❌ | Filter by travel purpose |
| `UnitGroupIds` | `list[str]` | ❌ | Filter by unit group IDs |
| `UnitGroupTypes` | `str` | ❌ | Filter by unit group types |

</details>

<details>
<summary>`GET` <strong>ListRevenuesReport</strong></summary>

### 📖 Description
Get a revenues report for a property within a specified date range.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/reports/v1/reports/revenues`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |
| `From` | `str` | ✅ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `To` | `str` | ✅ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `LanguageCode` | `str` | ❌ | The language for the report (2-letter ISO code) |

</details>

