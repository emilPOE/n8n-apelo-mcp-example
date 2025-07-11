# 💰 Finance Tools

Tools for managing folios, invoices, payments, and financial transactions.

**Total Tools:** 60

## Finance Accounts

<details>
<summary>`POST` <strong>ExportAccounts</strong></summary>

### 📖 Description
Return transactions filtered by timestamp for a property for a given period.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/accounts/export`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `propertyId` | `str` | ✅ | The property ID |
| `From` | `str` | ✅ | Start date and time for filtering or time range queries. Specify a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `To` | `str` | ✅ | End date and time for filtering or time range queries. Specify a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `accountNumber` | `str` | ❌ | Filter transactions by account number |
| `accountType` | `str` | ❌ | Filter transactions by type |
| `accountingSchema` | `str` | ❌ | Override the default accounting schema |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |
| `languageCode` | `str` | ❌ | The language for the report (2-letter ISO code) |

</details>

<details>
<summary>`POST` <strong>ExportAccountsDaily</strong></summary>

### 📖 Description
Return transactions filtered by date (business day) for a property for a given period.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/accounts/export-daily`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `propertyId` | `str` | ✅ | The property ID |
| `From` | `str` | ✅ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `To` | `str` | ✅ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `accountNumber` | `str` | ❌ | Filter transactions by account number |
| `accountType` | `str` | ❌ | Filter transactions by type |
| `accountingSchema` | `str` | ❌ | Override the default accounting schema |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |
| `languageCode` | `str` | ❌ | The language for the report (2-letter ISO code) |
| `reference` | `str` | ❌ | Filter by reference |

</details>

<details>
<summary>`POST` <strong>ExportAccountsGross</strong></summary>

### 📖 Description
Return gross transactions filtered by date (business day) for a property for a given period.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/accounts/export-gross-daily`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `propertyId` | `str` | ✅ | The property ID |
| `From` | `str` | ✅ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `To` | `str` | ✅ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `accountingSchema` | `str` | ❌ | Override the default accounting schema |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |
| `reference` | `str` | ❌ | Filter by reference |

</details>

<details>
<summary>`POST` <strong>GetAccountAggregate</strong></summary>

### 📖 Description
Aggregate transactions by date (business day) for all accounts and a given period.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/accounts/aggregate-daily`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `propertyId` | `str` | ✅ | The property ID |
| `From` | `str` | ✅ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `To` | `str` | ✅ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `accountNumber` | `str` | ❌ | Filter transactions by account number |
| `accountType` | `str` | ❌ | Filter transactions by type |
| `accountingSchema` | `str` | ❌ | Override the default accounting schema |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |
| `languageCode` | `str` | ❌ | The language for the report (2-letter ISO code) |
| `reference` | `str` | ❌ | Filter by reference |

</details>

<details>
<summary>`POST` <strong>GetAccountAggregatePairs</strong></summary>

### 📖 Description
Aggregate transaction pairs by date (business day) for all accounts and a given period.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/accounts/aggregate-pairs-daily`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `propertyId` | `str` | ✅ | The property ID |
| `From` | `str` | ✅ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `To` | `str` | ✅ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `accountNumber` | `str` | ❌ | Filter transactions by account number |
| `accountType` | `str` | ❌ | Filter transactions by type |
| `accountingSchema` | `str` | ❌ | Override the default accounting schema |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |
| `languageCode` | `str` | ❌ | The language for the report (2-letter ISO code) |
| `reference` | `str` | ❌ | Filter by reference |

</details>

<details>
<summary>`GET` <strong>GetAccountByNumber</strong></summary>

### 📖 Description
Return account information by account number.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/accounts/{number}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |
| `Number` | `str` | ✅ | The number to filter by |
| `AccountingSchema` | `str` | ❌ | Override the default accounting schema |
| `IncludeArchived` | `str` | ❌ | Include archived items in the result |
| `LanguageCode` | `str` | ❌ | The language for the report (2-letter ISO code) |
| `TransactionLimit` | `str` | ❌ | Maximum number of transactions to include |

</details>

<details>
<summary>`POST` <strong>GetAccountsAggregate</strong></summary>

### 📖 Description
Aggregate transactions by timestamp for all accounts and a given period.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/accounts/aggregate`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `propertyId` | `str` | ✅ | The property ID |
| `From` | `str` | ✅ | Start date and time for filtering or time range queries. Specify a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `To` | `str` | ✅ | End date and time for filtering or time range queries. Specify a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `accountNumber` | `str` | ❌ | Filter transactions by account number |
| `accountType` | `str` | ❌ | Filter transactions by type |
| `accountingSchema` | `str` | ❌ | Override the default accounting schema |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |
| `languageCode` | `str` | ❌ | The language for the report (2-letter ISO code) |

</details>

<details>
<summary>`GET` <strong>ListAccountSchema</strong></summary>

### 📖 Description
Return the chart of accounts of the subledger.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/accounts/schema`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |
| `AccountingSchema` | `str` | ❌ | Override the default accounting schema |
| `Depth` | `str` | ❌ | How many hierarchy levels to include (between 1 and 4, default is 1). |
| `IncludeArchived` | `str` | ❌ | Include archived items in the result |
| `LanguageCode` | `str` | ❌ | The language for the report (2-letter ISO code) |

</details>

<details>
<summary>`GET` <strong>ListChildAccounts</strong></summary>

### 📖 Description
Return a list of child accounts.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/accounts/child-accounts`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |
| `Parent` | `str` | ✅ | Filter account list by the parent account's number. |
| `AccountingSchema` | `str` | ❌ | Override the default accounting schema |
| `IncludeArchived` | `str` | ❌ | Include archived items in the result |
| `LanguageCode` | `str` | ❌ | The language for the report (2-letter ISO code) |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |

</details>

## Finance External Accounts

<details>
<summary>`GET` <strong>ListExternalAccounts</strong></summary>

### 📖 Description
Return a list of external accounts.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/external-accounts`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `FolioId` | `str` | ✅ | The folio ID |
| `PropertyId` | `str` | ✅ | The property ID |
| `LanguageCode` | `str` | ❌ | The language for the report (2-letter ISO code) |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `Parent` | `str` | ❌ | Filter account list by the parent account's number. |

</details>

## 📋 Folios

<details>
<summary>`PUT` <strong>BulkMoveCharges</strong></summary>

### 📖 Description
Move multiple charges from one folio to another. Multiple source folios and multiple target folios can be specified.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/finance/v1/folio-actions/bulk-move`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

<details>
<summary>`PUT` <strong>CancelPayment</strong></summary>

### 📖 Description
Cancel a specific payment.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/finance/v1/folios/{folioId}/payments/{paymentId}/cancel`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `paymentId` | `str` | ✅ | The id of the payment. |

</details>

<details>
<summary>`HEAD` <strong>CheckFolioExists</strong></summary>

### 📖 Description
Check if a folio exists.

### 🔗 API Endpoint
- **Method:** HEAD
- **Path:** `/finance/v1/folios/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`PUT` <strong>CloseFolio</strong></summary>

### 📖 Description
Close a folio.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/finance/v1/folio-actions/{folioId}/close`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |

</details>

<details>
<summary>`POST` <strong>CorrectFolio</strong></summary>

### 📖 Description
Corrects a folio by moving some charges. This operation creates a new folio with the charges from the request. The payment, equal to the sum of charges, is also split to this new folio so that both folios will have 0 balance.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folio-actions/{folioId}/correct`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`GET` <strong>CountFolios</strong></summary>

### 📖 Description
Get the count of folios matching the specified filters.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/folios/$count`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `BalanceFilter` | `list[str]` | ❌ | This will filter reservations based on their balance. |
| `BookingIds` | `list[str]` | ❌ | Filter by booking IDs |
| `CheckedOutOnAccountsReceivable` | `str` | ❌ | If set to `true`, only return invoices with an open balance (AR). Otherwise, returns all. |
| `CompanyIds` | `list[str]` | ❌ | Company IDs the report should be generated for |
| `CreatedFrom` | `str` | ❌ | The inclusive start time of the date of creation. Mostly useful for external folios. A date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `CreatedTo` | `str` | ❌ | The exclusive end time of the date of creation. Mostly useful for external folios. A date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `ExcludeClosed` | `str` | ❌ | If set to `true`, closed folios are filtered out from the result collection - DEPRECATED: This field will be removed soon. Please use Status=Open instead. |
| `ExternalFolioCode` | `str` | ❌ | Allows filtering external folios by code. Useful when you use external folios with custom codes. Specifying this parameter will ignore the Type parameter and treat as if it would be set to External. |
| `HasInvoices` | `bool` | ❌ | If set to `true`, only return folios that have invoices |
| `IsEmpty` | `bool` | ❌ | If set to `true`, only return empty folios (no unmoved [transitory] charges, no unmoved payments, no allowances). If set to `false`, only return non-empty folios |
| `OnlyMain` | `bool` | ❌ | If set to `true`, only main folios are returned, otherwise all. |
| `PropertyIds` | `list[str]` | ❌ | Return market segments with any of the specified property ids. |
| `ReservationIds` | `list[str]` | ❌ | Filter by reservation IDs |
| `Status` | `str` | ❌ | Filter by status |
| `TextSearch` | `str` | ❌ | Free text search |
| `Type` | `str` | ❌ | Filter by type |
| `UpdatedFrom` | `str` | ❌ | The inclusive start time of the date of the last update. Mostly useful for external folios. A date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `UpdatedTo` | `str` | ❌ | The exclusive end time of the date of the last update. Mostly useful for external folios. A date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |

</details>

<details>
<summary>`POST` <strong>CreateAccountPayment</strong></summary>

### 📖 Description
Create a payment by charging a stored payment account for the folio.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folios/{folioId}/payments/by-payment-account`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreateAuthPayment</strong></summary>

### 📖 Description
Create a payment from an existing authorization for the folio.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folios/{folioId}/payments/by-authorization`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreateBulkAllowances</strong></summary>

### 📖 Description
Create allowances for a folio

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folio-actions/{folioId}/bulk-allowances`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreateChargeAllowance</strong></summary>

### 📖 Description
Create an allowance for a charge

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folio-actions/{folioId}/charges/{chargeId}/allowances`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `chargeId` | `str` | ✅ | The charge ID |
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreateFolio</strong></summary>

### 📖 Description
Create additional folios for a reservation or new external folios.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folios`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreateFolioAllowance</strong></summary>

### 📖 Description
Create an allowance for a folio

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folio-actions/{folioId}/allowances`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreateFolioCancellationFee</strong></summary>

### 📖 Description
Add and directly post a cancellation fee to the folio. Additional fees may be added if configured, and fee may be moved if routing instructions are defined.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folio-actions/{folioId}/cancellation-fee`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreateFolioCharge</strong></summary>

### 📖 Description
Add and directly post a charge to the folio. Additional fees may be added if configured for the property.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folio-actions/{folioId}/charges`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreateFolioNoShowFee</strong></summary>

### 📖 Description
Add and directly post a no-show fee to the folio. Additional fees may be added if configured, and fee may be moved if routing instructions are defined.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folio-actions/{folioId}/no-show-fee`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreateFolioPayment</strong></summary>

### 📖 Description
Create a custom payment for the folio.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folios/{folioId}/payments`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreateFolioRefund</strong></summary>

### 📖 Description
Create a refund for the folio.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folios/{folioId}/refunds`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreateFolioTransitoryCharge</strong></summary>

### 📖 Description
Add and directly post a transitory charge to the folio. Additional fees may be added if configured for the property.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folio-actions/{folioId}/transitory-charges`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreatePaymentLink</strong></summary>

### 📖 Description
Create a payment link for the folio that can be sent to the guest.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folios/{folioId}/payments/by-link`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreatePaymentRefund</strong></summary>

### 📖 Description
Create a refund for a specific payment.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folios/{folioId}/payments/{paymentId}/refunds`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `paymentId` | `str` | ✅ | The id of the payment. |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreateTerminalPayment</strong></summary>

### 📖 Description
Create a payment using a card terminal for the folio.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folios/{folioId}/payments/by-terminal`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`DELETE` <strong>DeleteFolio</strong></summary>

### 📖 Description
Delete a folio.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/finance/v1/folios/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>GetFolio</strong></summary>

### 📖 Description
Get detailed information about a specific folio.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/folios/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |

</details>

<details>
<summary>`GET` <strong>GetFolioPayment</strong></summary>

### 📖 Description
Get a specific payment by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/folios/{folioId}/payments/{paymentId}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `FolioId` | `str` | ✅ | The folio ID |
| `PaymentId` | `str` | ✅ | The id of the payment. |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |

</details>

<details>
<summary>`GET` <strong>GetFolioRefund</strong></summary>

### 📖 Description
Get a specific refund by ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/folios/{folioId}/refunds/{refundId}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `FolioId` | `str` | ✅ | The folio ID |
| `RefundId` | `str` | ✅ | The id of the refund. |

</details>

<details>
<summary>`GET` <strong>ListFolioPayments</strong></summary>

### 📖 Description
Get a list of payments for a folio.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/folios/{folioId}/payments`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `FolioId` | `str` | ✅ | The folio ID |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `StatusCodes` | `str` | ❌ | Filter by status codes |

</details>

<details>
<summary>`GET` <strong>ListFolioRefunds</strong></summary>

### 📖 Description
Get a list of refunds for a folio.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/folios/{folioId}/refunds`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `FolioId` | `str` | ✅ | The folio ID |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `StatusCodes` | `str` | ❌ | Filter by status codes |

</details>

<details>
<summary>`GET` <strong>ListFolios</strong></summary>

### 📖 Description
Search for folios with various filtering options.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/folios`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `BalanceFilter` | `list[str]` | ❌ | This will filter reservations based on their balance. |
| `BookingIds` | `list[str]` | ❌ | Filter by booking IDs |
| `CheckedOutOnAccountsReceivable` | `str` | ❌ | If set to `true`, only return invoices with an open balance (AR). Otherwise, returns all. |
| `CompanyIds` | `list[str]` | ❌ | Company IDs the report should be generated for |
| `CreatedFrom` | `str` | ❌ | The inclusive start time of the date of creation. Mostly useful for external folios. A date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `CreatedTo` | `str` | ❌ | The exclusive end time of the date of creation. Mostly useful for external folios. A date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `ExcludeClosed` | `str` | ❌ | If set to `true`, closed folios are filtered out from the result collection - DEPRECATED: This field will be removed soon. Please use Status=Open instead. |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `ExternalFolioCode` | `str` | ❌ | Allows filtering external folios by code. Useful when you use external folios with custom codes. Specifying this parameter will ignore the Type parameter and treat as if it would be set to External. |
| `HasInvoices` | `bool` | ❌ | If set to `true`, only return folios that have invoices |
| `IsEmpty` | `bool` | ❌ | If set to `true`, only return empty folios (no unmoved [transitory] charges, no unmoved payments, no allowances). If set to `false`, only return non-empty folios |
| `OnlyMain` | `bool` | ❌ | If set to `true`, only main folios are returned, otherwise all. |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyIds` | `list[str]` | ❌ | Return market segments with any of the specified property ids. |
| `ReservationIds` | `list[str]` | ❌ | Filter by reservation IDs |
| `Status` | `str` | ❌ | Filter by status |
| `TextSearch` | `str` | ❌ | Free text search |
| `Type` | `str` | ❌ | Filter by type |
| `UpdatedFrom` | `str` | ❌ | The inclusive start time of the date of the last update. Mostly useful for external folios. A date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `UpdatedTo` | `str` | ❌ | The exclusive end time of the date of the last update. Mostly useful for external folios. A date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |

</details>

<details>
<summary>`PUT` <strong>MoveAllFolioCharges</strong></summary>

### 📖 Description
Move all charges and transitory charges from one folio to another.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/finance/v1/folio-actions/{folioId}/move-all-charges`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

<details>
<summary>`PUT` <strong>MoveFolioCharges</strong></summary>

### 📖 Description
Move multiple charges, allowances and transitory charges from one folio to another.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/finance/v1/folio-actions/{folioId}/move-charges`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

<details>
<summary>`PUT` <strong>MoveFolioPayments</strong></summary>

### 📖 Description
Move multiple payments from one guest/booking folio to another.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/finance/v1/folio-actions/{folioId}/move-payments`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

<details>
<summary>`PUT` <strong>PostFolioCharges</strong></summary>

### 📖 Description
Posts all unposted charges for the whole length of stay.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/finance/v1/folio-actions/{folioId}/post-charges`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |

</details>

<details>
<summary>`PUT` <strong>ReopenFolio</strong></summary>

### 📖 Description
Reopens a folio.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/finance/v1/folio-actions/{folioId}/reopen`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |

</details>

<details>
<summary>`POST` <strong>SplitFolioCharge</strong></summary>

### 📖 Description
Splits a charge into two using the percent or amount provided Creates an allowance and two new charges.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folio-actions/{folioId}/charges/{chargeId}/split`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `chargeId` | `str` | ✅ | The charge ID |
| `folioId` | `str` | ✅ | The folio ID |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>SplitFolioPayment</strong></summary>

### 📖 Description
Splits a payment into two using the percent or amount provided Creates a refund and two new payments.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/folio-actions/{folioId}/payments/{paymentId}/split`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `folioId` | `str` | ✅ | The folio ID |
| `paymentId` | `str` | ✅ | The id of the payment. |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`PATCH` <strong>UpdateFolio</strong></summary>

### 📖 Description
Update specific properties of a folio using JSON Patch operations.

### 🔗 API Endpoint
- **Method:** PATCH
- **Path:** `/finance/v1/folios/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

## Finance Global Accounts

<details>
<summary>`GET` <strong>ListGlobalAccounts</strong></summary>

### 📖 Description
Return a list of global accounts.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/global-accounts`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |
| `Parent` | `str` | ✅ | Filter account list by the parent account's number. |
| `AccountingSchema` | `str` | ❌ | Override the default accounting schema |
| `IncludeArchived` | `str` | ❌ | Include archived items in the result |
| `LanguageCode` | `str` | ❌ | The language for the report (2-letter ISO code) |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |

</details>

## Finance Guest Accounts

<details>
<summary>`GET` <strong>ListGuestAccounts</strong></summary>

### 📖 Description
Return a list of guest accounts.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/guest-accounts`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |
| `ReservationId` | `str` | ✅ | The reservation ID |
| `LanguageCode` | `str` | ❌ | The language for the report (2-letter ISO code) |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `Parent` | `str` | ❌ | Filter account list by the parent account's number. |

</details>

## 🧾 Invoices

<details>
<summary>`PUT` <strong>CancelInvoice</strong></summary>

### 📖 Description
Cancel an invoice with a specified reason code.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/finance/v1/invoice-actions/{id}/cancel`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

<details>
<summary>`POST` <strong>CreateInvoice</strong></summary>

### 📖 Description
Create an invoice for a specific folio.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/finance/v1/invoices`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`GET` <strong>GetInvoice</strong></summary>

### 📖 Description
Get detailed information about a specific invoice.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/invoices/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |

</details>

<details>
<summary>`GET` <strong>GetInvoicePdf</strong></summary>

### 📖 Description
Get the PDF file for a specific invoice.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/invoices/{id}/pdf`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>ListInvoicePreview</strong></summary>

### 📖 Description
Get an invoice preview for a specific folio.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/invoices/preview`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `FolioId` | `str` | ✅ | The folio ID |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |

</details>

<details>
<summary>`GET` <strong>ListInvoicePreviewPdf</strong></summary>

### 📖 Description
Get a preview invoice PDF for a specific folio.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/invoices/preview-pdf`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `FolioId` | `str` | ✅ | The folio ID |
| `LanguageCode` | `str` | ✅ | The language for the report (2-letter ISO code) |

</details>

<details>
<summary>`GET` <strong>ListInvoices</strong></summary>

### 📖 Description
Search for invoices with various filtering options.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/invoices`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `BookingIds` | `list[str]` | ❌ | Filter by booking IDs |
| `CheckedOutOnAccountsReceivable` | `str` | ❌ | If set to `true`, only return invoices with an open balance (AR). Otherwise, returns all. |
| `CompanyIds` | `list[str]` | ❌ | Company IDs the report should be generated for |
| `DateFilterDateGeneric` | `str` | ❌ | Set a date interval to get the report for. Cannot be more than 1 month. You can provide an array of string expressions which all need to apply. |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `FolioIds` | `str` | ❌ | Filter by folio IDs |
| `NameSearch` | `str` | ❌ | Find invoices for a recipient name or company. Provide at least three characters. |
| `Number` | `str` | ❌ | The number to filter by |
| `OutstandingPaymentFilter` | `str` | ❌ | Filter for the outstanding balance for invoices. You can provide an array of string expressions which all need to apply. |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PaymentSettled` | `str` | ❌ | If set to `true`, returns only invoices having no outstanding payments or marked as settled. |
| `PropertyIds` | `list[str]` | ❌ | Return market segments with any of the specified property ids. |
| `RecipientType` | `str` | ❌ | Filter invoices by recipient type |
| `ReservationIds` | `list[str]` | ❌ | Filter by reservation IDs |
| `Status` | `str` | ❌ | Filter by status |

</details>

<details>
<summary>`PUT` <strong>PayInvoice</strong></summary>

### 📖 Description
Mark an invoice as paid with the specified payment method and receipt.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/finance/v1/invoice-actions/{id}/pay`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

## Finance Types

<details>
<summary>`GET` <strong>ListCurrencies</strong></summary>

### 📖 Description
Get a list of all supported currencies.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/types/currencies`

</details>

<details>
<summary>`GET` <strong>ListPaymentMethods</strong></summary>

### 📖 Description
Get a list of all supported payment methods.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/types/payment-methods`

</details>

<details>
<summary>`GET` <strong>ListServiceTypes</strong></summary>

### 📖 Description
Get a list of all supported service types.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/types/service-types`

</details>

<details>
<summary>`GET` <strong>ListVatTypes</strong></summary>

### 📖 Description
No description available.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/finance/v1/types/vat`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `AtDate` | `str` | ❌ | Specific date for which data should be retrieved. Specify a pure date in YYYY-MM-DD format |

</details>

