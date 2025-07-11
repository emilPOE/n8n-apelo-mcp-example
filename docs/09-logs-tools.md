# 📝 Logs Tools

Tools for accessing system logs and audit information.

**Total Tools:** 4

## 📝 Bookings

<details>
<summary>`GET` <strong>ListReservationLogs</strong></summary>

### 📖 Description
Get reservation change log entries sorted by timestamp.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/logs/v1/booking/reservation`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `ClientIds` | `str` | ❌ | Filter the log entries by client IDs (which application triggered this event) |
| `DateFilterDateGeneric` | `str` | ❌ | Set a date interval to get the report for. Cannot be more than 1 month. You can provide an array of string expressions which all need to apply. |
| `EventTypes` | `str` | ❌ | Filter the log entries by event types. |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyIds` | `list[str]` | ❌ | Return market segments with any of the specified property ids. |
| `ReservationIds` | `list[str]` | ❌ | Filter by reservation IDs |
| `SubjectIds` | `str` | ❌ | Filter the log entries by subject IDs (the ID of the object this event refers to) |

</details>

## Logs Finance

<details>
<summary>`GET` <strong>ListFolioLogs</strong></summary>

### 📖 Description
Get folio change log entries sorted by timestamp.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/logs/v1/finance/folio`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `ClientIds` | `str` | ❌ | Filter the log entries by client IDs (which application triggered this event) |
| `DateFilterDateGeneric` | `str` | ❌ | Set a date interval to get the report for. Cannot be more than 1 month. You can provide an array of string expressions which all need to apply. |
| `EventTypes` | `str` | ❌ | Filter the log entries by event types. |
| `FolioIds` | `str` | ❌ | Filter by folio IDs |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyIds` | `list[str]` | ❌ | Return market segments with any of the specified property ids. |
| `SubjectIds` | `str` | ❌ | Filter the log entries by subject IDs (the ID of the object this event refers to) |

</details>

<details>
<summary>`GET` <strong>ListNightAuditLogs</strong></summary>

### 📖 Description
Get night audit logs.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/logs/v1/finance/night-audit`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `DateFilterDateGeneric` | `str` | ❌ | Set a date interval to get the report for. Cannot be more than 1 month. You can provide an array of string expressions which all need to apply. |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyIds` | `list[str]` | ❌ | Return market segments with any of the specified property ids. |
| `Statuses` | `str` | ❌ | Filter by statuses |
| `SubjectIds` | `str` | ❌ | Filter the log entries by subject IDs (the ID of the object this event refers to) |

</details>

<details>
<summary>`GET` <strong>ListTransactionExportLogs</strong></summary>

### 📖 Description
Get audit log for accounting exports.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/logs/v1/finance/transactions-export`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `DateFilterDateGeneric` | `str` | ❌ | Set a date interval to get the report for. Cannot be more than 1 month. You can provide an array of string expressions which all need to apply. |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyIds` | `list[str]` | ❌ | Return market segments with any of the specified property ids. |
| `SubjectIds` | `str` | ❌ | Filter the log entries by subject IDs (the ID of the object this event refers to) |
| `Types` | `str` | ❌ | Filter by types |

</details>

