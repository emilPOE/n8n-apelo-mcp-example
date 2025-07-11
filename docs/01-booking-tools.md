# 📋 Booking Tools

Tools for managing reservations, bookings, groups, and blocks.

**Total Tools:** 45

## 🔒 Blocks

<details>
<summary>`PUT` <strong>AmendBlock</strong></summary>

### 📖 Description
Modify an existing block's details.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/block-actions/{id}/amend`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

<details>
<summary>`PUT` <strong>CancelBlock</strong></summary>

### 📖 Description
Cancel a block.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/block-actions/{id}/cancel`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`HEAD` <strong>CheckBlockExists</strong></summary>

### 📖 Description
Check if an inventory block exists.

### 🔗 API Endpoint
- **Method:** HEAD
- **Path:** `/booking/v1/blocks/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`PUT` <strong>ConfirmBlock</strong></summary>

### 📖 Description
Confirm a block, making it definitive.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/block-actions/{id}/confirm`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>CountBlocks</strong></summary>

### 📖 Description
Get the count of blocks matching the specified filters.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/blocks/$count`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `From` | `str` | ❌ | Start date and time for filtering or time range queries. Specify a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `GroupId` | `str` | ❌ | Return blocks for the specific group |
| `PropertyIds` | `list[str]` | ❌ | Return market segments with any of the specified property ids. |
| `RatePlanIds` | `str` | ❌ | Return rate plans with any of the specified IDs |
| `Status` | `str` | ❌ | Filter by status |
| `TimeSliceDefinitionIdsDateGeneric` | `str` | ❌ | Time slice definition IDs to filter by |
| `TimeSliceTemplateDateGeneric` | `str` | ❌ | Time slice template to use |
| `To` | `str` | ❌ | End date and time for filtering or time range queries. Specify a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `UnitGroupIds` | `list[str]` | ❌ | Filter by unit group IDs |
| `UnitGroupTypes` | `str` | ❌ | Filter by unit group types |

</details>

<details>
<summary>`POST` <strong>CreateBlock</strong></summary>

### 📖 Description
Create a new inventory block for specific units and dates.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/booking/v1/blocks`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`DELETE` <strong>DeleteBlock</strong></summary>

### 📖 Description
Delete an inventory block.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/booking/v1/blocks/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>GetBlock</strong></summary>

### 📖 Description
Get details of a specific inventory block.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/blocks/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |

</details>

<details>
<summary>`GET` <strong>ListBlocks</strong></summary>

### 📖 Description
Search for inventory blocks with various filters.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/blocks`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `From` | `str` | ❌ | Start date and time for filtering or time range queries. Specify a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `GroupId` | `str` | ❌ | Return blocks for the specific group |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyIds` | `list[str]` | ❌ | Return market segments with any of the specified property ids. |
| `RatePlanIds` | `str` | ❌ | Return rate plans with any of the specified IDs |
| `Status` | `str` | ❌ | Filter by status |
| `TimeSliceDefinitionIdsDateGeneric` | `str` | ❌ | Time slice definition IDs to filter by |
| `TimeSliceTemplateDateGeneric` | `str` | ❌ | Time slice template to use |
| `To` | `str` | ❌ | End date and time for filtering or time range queries. Specify a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `UnitGroupIds` | `list[str]` | ❌ | Filter by unit group IDs |
| `UnitGroupTypes` | `str` | ❌ | Filter by unit group types |

</details>

<details>
<summary>`PUT` <strong>ReleaseBlock</strong></summary>

### 📖 Description
Release a block, making the inventory available again.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/block-actions/{id}/release`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`PUT` <strong>WashBlock</strong></summary>

### 📖 Description
Wash a block (remove unused allocations).

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/block-actions/{id}/wash`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

## 📝 Bookings

<details>
<summary>`POST` <strong>AddReservationToBooking</strong></summary>

### 📖 Description
Add a new reservation to an existing booking.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/booking/v1/bookings/{id}/reservations`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`POST` <strong>CreateBooking</strong></summary>

### 📖 Description
Create a new booking with one reservation. This is the primary way to make a hotel reservation.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/booking/v1/bookings`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`GET` <strong>GetBooking</strong></summary>

### 📖 Description
Retrieve a specific booking by its ID.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/bookings/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |

</details>

<details>
<summary>`GET` <strong>ListBookings</strong></summary>

### 📖 Description
Search and retrieve bookings with flexible filtering options.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/bookings`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `ChannelCode` | `str` | ❌ | Filter result by the channel code. The result set will contain all bookings having reservations with the specified channel code. |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `ExternalCode` | `str` | ❌ | Filter result by external code |
| `GroupId` | `str` | ❌ | Return blocks for the specific group |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `ReservationId` | `str` | ❌ | The reservation ID |
| `TextSearch` | `str` | ❌ | Free text search |

</details>

## 👥 Groups

<details>
<summary>`POST` <strong>AddReservationToGroup</strong></summary>

### 📖 Description
Add one or more reservations to a group.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/booking/v1/groups/{id}/reservations`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`HEAD` <strong>CheckGroupExists</strong></summary>

### 📖 Description
Check if a group exists.

### 🔗 API Endpoint
- **Method:** HEAD
- **Path:** `/booking/v1/groups/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>CountGroups</strong></summary>

### 📖 Description
Get the count of groups matching the specified filters.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/groups/$count`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `From` | `str` | ❌ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `PropertyIds` | `list[str]` | ❌ | Return market segments with any of the specified property ids. |
| `Status` | `str` | ❌ | Filter by status |
| `TextSearch` | `str` | ❌ | Free text search |
| `To` | `str` | ❌ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |

</details>

<details>
<summary>`POST` <strong>CreateGroup</strong></summary>

### 📖 Description
Create a new group booking.

### 🔗 API Endpoint
- **Method:** POST
- **Path:** `/booking/v1/groups`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |
| `idempotencyKey` | `str` | ❌ | Unique key for safely retrying requests without accidentally performing the same operation twice. We'll always send back the same response for requests made with the same key, and keys can't be reused. |

</details>

<details>
<summary>`DELETE` <strong>DeleteGroup</strong></summary>

### 📖 Description
Delete a group booking.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/booking/v1/groups/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>GetGroup</strong></summary>

### 📖 Description
Get details of a specific group booking.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/groups/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |

</details>

<details>
<summary>`GET` <strong>ListGroups</strong></summary>

### 📖 Description
Search for group bookings with various filters.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/groups`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `From` | `str` | ❌ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyIds` | `list[str]` | ❌ | Return market segments with any of the specified property ids. |
| `Status` | `str` | ❌ | Filter by status |
| `TextSearch` | `str` | ❌ | Free text search |
| `To` | `str` | ❌ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |

</details>

## 💰 Offers

<details>
<summary>`GET` <strong>ListOfferIndex</strong></summary>

### 📖 Description
Get offer index with rates and availability for a date range.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/offer-index`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `RatePlanId` | `str` | ✅ | The rate plan ID |
| `ChannelCode` | `str` | ✅ | Filter result by the channel code. The result set will contain all bookings having reservations with the specified channel code. |
| `From` | `str` | ✅ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `To` | `str` | ✅ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |

</details>

<details>
<summary>`GET` <strong>ListOffers</strong></summary>

### 📖 Description
Search for available room and rate offers for a specific stay.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/offers`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `PropertyId` | `str` | ✅ | The property ID |
| `Adults` | `int` | ✅ | Number of adults |
| `Arrival` | `str` | ✅ | Date and optional time of arrival. Specify either a pure date or a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `Departure` | `str` | ✅ | Date and optional time of departure. Cannot be more than 5 years after arrival. Specify either a pure date or a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `ChannelCode` | `str` | ❌ | Filter result by the channel code. The result set will contain all bookings having reservations with the specified channel code. |
| `ChildrenAges` | `list[int]` | ❌ | Ages of children |
| `CorporateCode` | `str` | ❌ | The code associated with a corporate rate |
| `IncludeUnavailable` | `bool` | ❌ | Return also offers that are currently not publicly bookable as restrictions are violated. By default only available offers are returned |
| `PromoCode` | `str` | ❌ | The promo code associated with a special offer |
| `TimeSliceDefinitionIdsDateGeneric` | `str` | ❌ | Time slice definition IDs to filter by |
| `TimeSliceTemplateDateGeneric` | `str` | ❌ | Time slice template to use |
| `UnitGroupIds` | `list[str]` | ❌ | Filter by unit group IDs |
| `UnitGroupTypes` | `str` | ❌ | Filter by unit group types |

</details>

<details>
<summary>`GET` <strong>ListRatePlanOffers</strong></summary>

### 📖 Description
Get offers for a specific rate plan.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/rate-plan-offers`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `RatePlanId` | `str` | ✅ | The rate plan ID |
| `Adults` | `int` | ✅ | Number of adults |
| `Arrival` | `str` | ✅ | Date and optional time of arrival. Specify either a pure date or a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `Departure` | `str` | ✅ | Date and optional time of departure. Cannot be more than 5 years after arrival. Specify either a pure date or a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `ChannelCode` | `str` | ❌ | Filter result by the channel code. The result set will contain all bookings having reservations with the specified channel code. |
| `ChildrenAges` | `list[int]` | ❌ | Ages of children |
| `IncludeUnavailable` | `bool` | ❌ | Return also offers that are currently not publicly bookable as restrictions are violated. By default only available offers are returned |
| `OverridePrices` | `str` | ❌ | Desired prices for each timeslice |

</details>

<details>
<summary>`GET` <strong>ListServiceOffers</strong></summary>

### 📖 Description
Get available service offers for a specific stay.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/service-offers`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `RatePlanId` | `str` | ✅ | The rate plan ID |
| `Adults` | `int` | ✅ | Number of adults |
| `Arrival` | `str` | ✅ | Date and optional time of arrival. Specify either a pure date or a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `Departure` | `str` | ✅ | Date and optional time of departure. Cannot be more than 5 years after arrival. Specify either a pure date or a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `ChannelCode` | `str` | ❌ | Filter result by the channel code. The result set will contain all bookings having reservations with the specified channel code. |
| `ChildrenAges` | `list[int]` | ❌ | Ages of children |
| `IncludeUnavailable` | `bool` | ❌ | Return also offers that are currently not publicly bookable as restrictions are violated. By default only available offers are returned |
| `OnlyDefaultDatesDateGeneric` | `str` | ❌ | Depending on the postNextDay setting of a service it will by default be posted before or after midnight. |

</details>

## 🏨 Reservations

<details>
<summary>`PUT` <strong>AddCityTax</strong></summary>

### 📖 Description
Add city tax to a reservation.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/reservation-actions/{id}/add-city-tax`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`PUT` <strong>AmendReservation</strong></summary>

### 📖 Description
Modify the stay details of a reservation.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/reservation-actions/{id}/amend`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

<details>
<summary>`PUT` <strong>AssignSpecificUnit</strong></summary>

### 📖 Description
Assign a specific unit to a reservation.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/reservation-actions/{id}/assign-unit/{unitId}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `unitId` | `str` | ✅ | The unit ID |
| `From` | `str` | ❌ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `To` | `str` | ❌ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |

</details>

<details>
<summary>`PUT` <strong>AssignUnit</strong></summary>

### 📖 Description
Automatically assign a suitable unit to a reservation.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/reservation-actions/{id}/assign-unit`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `unitConditions` | `str` | ❌ | The optional unit conditions for unit that you want to auto assign for. |

</details>

<details>
<summary>`PUT` <strong>BookService</strong></summary>

### 📖 Description
Book a service for a reservation.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/reservation-actions/{id}/book-service`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `bodyJsonData` | `object` | ✅ | The request body data as JSON string |

</details>

<details>
<summary>`PUT` <strong>CancelReservation</strong></summary>

### 📖 Description
Cancel a reservation.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/reservation-actions/{id}/cancel`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`PUT` <strong>CheckIn</strong></summary>

### 📖 Description
Check in a guest for their reservation.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/reservation-actions/{id}/checkin`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `withCityTax` | `str` | ❌ | Define if city tax should be added for this reservation or not. The default is 'true'. |

</details>

<details>
<summary>`PUT` <strong>CheckOut</strong></summary>

### 📖 Description
Check out a guest from their reservation.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/reservation-actions/{id}/checkout`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>CountReservations</strong></summary>

### 📖 Description
Get the count of reservations matching the specified filters.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/reservations/$count`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `AllFoliosHaveInvoice` | `str` | ❌ | If set to `true`, returns only reservations, in which all folios are closed and have an invoice. If set to `false`, returns only reservations, in which some of the folios are open or don't have an invoice. |
| `BalanceFilter` | `list[str]` | ❌ | This will filter reservations based on their balance. |
| `BlockIds` | `str` | ❌ | Filter result by requested blocks |
| `BookingId` | `str` | ❌ | Filter result by booking id |
| `ChannelCode` | `str` | ❌ | Filter result by the channel code. The result set will contain all bookings having reservations with the specified channel code. |
| `CompanyIds` | `list[str]` | ❌ | Company IDs the report should be generated for |
| `DateFilterDateGeneric` | `str` | ❌ | Set a date interval to get the report for. Cannot be more than 1 month. You can provide an array of string expressions which all need to apply. |
| `ExternalCode` | `str` | ❌ | Filter result by external code |
| `From` | `str` | ❌ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `MarketSegmentIds` | `str` | ❌ | Filter result by market segment IDs |
| `PropertyIds` | `list[str]` | ❌ | Return market segments with any of the specified property ids. |
| `RatePlanIds` | `str` | ❌ | Return rate plans with any of the specified IDs |
| `Sources` | `str` | ❌ | Filter by sources |
| `Status` | `str` | ❌ | Filter by status |
| `TextSearch` | `str` | ❌ | Free text search |
| `To` | `str` | ❌ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `UnitGroupIds` | `list[str]` | ❌ | Filter by unit group IDs |
| `UnitGroupTypes` | `str` | ❌ | Filter by unit group types |
| `UnitIds` | `list[str]` | ❌ | Filter by unit IDs |
| `ValidationMessageCategory` | `str` | ❌ | Filter result by validation message category |

</details>

<details>
<summary>`GET` <strong>GetReservation</strong></summary>

### 📖 Description
Get details of a specific reservation.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/reservations/{id}`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |

</details>

<details>
<summary>`GET` <strong>GetReservationOffers</strong></summary>

### 📖 Description
Get available offers for modifying a reservation.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/reservations/{id}/offers`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `Adults` | `int` | ❌ | Number of adults |
| `Arrival` | `str` | ❌ | Date and optional time of arrival. Specify either a pure date or a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `ChannelCode` | `str` | ❌ | Filter result by the channel code. The result set will contain all bookings having reservations with the specified channel code. |
| `ChildrenAges` | `list[int]` | ❌ | Ages of children |
| `Departure` | `str` | ❌ | Date and optional time of departure. Cannot be more than 5 years after arrival. Specify either a pure date or a date and time (without fractional second part) in UTC or with UTC offset as defined in ISO8601:2004 |
| `IncludeUnavailable` | `bool` | ❌ | Return also offers that are currently not publicly bookable as restrictions are violated. By default only available offers are returned |
| `PromoCode` | `str` | ❌ | The promo code associated with a special offer |
| `Requote` | `str` | ❌ | Whether the offers should be re-quoted based on current prices, or only additions like change of number of adults should be calculated. Defaults to 'false' |
| `UnitGroupIds` | `list[str]` | ❌ | Filter by unit group IDs |

</details>

<details>
<summary>`GET` <strong>GetReservationServiceOffers</strong></summary>

### 📖 Description
Get available service offers for a reservation.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/reservations/{id}/service-offers`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `ChannelCode` | `str` | ❌ | Filter result by the channel code. The result set will contain all bookings having reservations with the specified channel code. |
| `IncludeUnavailable` | `bool` | ❌ | Return also offers that are currently not publicly bookable as restrictions are violated. By default only available offers are returned |
| `OnlyDefaultDatesDateGeneric` | `str` | ❌ | Depending on the postNextDay setting of a service it will by default be posted before or after midnight. |

</details>

<details>
<summary>`GET` <strong>GetReservationServices</strong></summary>

### 📖 Description
Get all services currently booked for a reservation.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/reservations/{id}/services`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`GET` <strong>ListReservations</strong></summary>

### 📖 Description
Search for reservations with various filters.

### 🔗 API Endpoint
- **Method:** GET
- **Path:** `/booking/v1/reservations`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `AllFoliosHaveInvoice` | `str` | ❌ | If set to `true`, returns only reservations, in which all folios are closed and have an invoice. If set to `false`, returns only reservations, in which some of the folios are open or don't have an invoice. |
| `BalanceFilter` | `list[str]` | ❌ | This will filter reservations based on their balance. |
| `BlockIds` | `str` | ❌ | Filter result by requested blocks |
| `BookingId` | `str` | ❌ | Filter result by booking id |
| `ChannelCode` | `str` | ❌ | Filter result by the channel code. The result set will contain all bookings having reservations with the specified channel code. |
| `CompanyIds` | `list[str]` | ❌ | Company IDs the report should be generated for |
| `DateFilterDateGeneric` | `str` | ❌ | Set a date interval to get the report for. Cannot be more than 1 month. You can provide an array of string expressions which all need to apply. |
| `ExpandGenericExpand` | `str` | ❌ | List of all embedded resources that should be expanded in the response |
| `ExternalCode` | `str` | ❌ | Filter result by external code |
| `From` | `str` | ❌ | Start date (inclusive) for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `MarketSegmentIds` | `str` | ❌ | Filter result by market segment IDs |
| `PageNumber` | `int` | ❌ | Page number, 1-based. Default value is 1 (if this is not set or not positive). Results in 204 if there are no items on that page. |
| `PageSize` | `int` | ❌ | Page size. If this is not set or not positive, the pageNumber is ignored and all items are returned. |
| `PropertyIds` | `list[str]` | ❌ | Return market segments with any of the specified property ids. |
| `RatePlanIds` | `str` | ❌ | Return rate plans with any of the specified IDs |
| `Sort` | `str` | ❌ | Sort order for results |
| `Sources` | `str` | ❌ | Filter by sources |
| `Status` | `str` | ❌ | Filter by status |
| `TextSearch` | `str` | ❌ | Free text search |
| `To` | `str` | ❌ | End date for filtering or time range queries. Specify a pure date in YYYY-MM-DD format |
| `UnitGroupIds` | `list[str]` | ❌ | Filter by unit group IDs |
| `UnitGroupTypes` | `str` | ❌ | Filter by unit group types |
| `UnitIds` | `list[str]` | ❌ | Filter by unit IDs |
| `ValidationMessageCategory` | `str` | ❌ | Filter result by validation message category |

</details>

<details>
<summary>`PUT` <strong>MarkNoShow</strong></summary>

### 📖 Description
Mark a reservation as a no-show.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/reservation-actions/{id}/noshow`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`PUT` <strong>RemoveCityTax</strong></summary>

### 📖 Description
Remove city tax from a reservation.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/reservation-actions/{id}/remove-city-tax`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`DELETE` <strong>RemoveServiceFromReservation</strong></summary>

### 📖 Description
Remove a specific service from a reservation.

### 🔗 API Endpoint
- **Method:** DELETE
- **Path:** `/booking/v1/reservations/{id}/services`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |
| `ServiceId` | `str` | ✅ | The service ID |

</details>

<details>
<summary>`PUT` <strong>RevertCheckIn</strong></summary>

### 📖 Description
Reverse a previous check-in operation.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/reservation-actions/{id}/revert-checkin`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

<details>
<summary>`PUT` <strong>UnassignUnits</strong></summary>

### 📖 Description
Remove all unit assignments from a reservation.

### 🔗 API Endpoint
- **Method:** PUT
- **Path:** `/booking/v1/reservation-actions/{id}/unassign-units`

### 📋 Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|--------------|
| `Id` | `str` | ✅ | The ID of the resource |

</details>

