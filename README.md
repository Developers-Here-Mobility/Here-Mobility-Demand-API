# Protocol Documentation
<a name="top"/>

## Table of Contents

- [marketplace/public/grpc/demand_handler/v2/gen-doc/demand_c2s_messages.proto](#marketplace/public/grpc/demand_handler/v2/gen-doc/demand_c2s_messages.proto)
    - [CancelRideRequest](#demand.v2.c2s.CancelRideRequest)
    - [CreatePublicTransportRideRequest](#demand.v2.c2s.CreatePublicTransportRideRequest)
    - [CreateRideRequest](#demand.v2.c2s.CreateRideRequest)
    - [GetRideListRequest](#demand.v2.c2s.GetRideListRequest)
    - [GetRideLocationRequest](#demand.v2.c2s.GetRideLocationRequest)
    - [GetRideRequest](#demand.v2.c2s.GetRideRequest)
    - [RideOffersRequest](#demand.v2.c2s.RideOffersRequest)





- [marketplace/public/grpc/demand_handler/v2/gen-doc/demand_c2s_service.proto](#marketplace/public/grpc/demand_handler/v2/gen-doc/demand_c2s_service.proto)



    - [C2SDemandApi](#demand.v2.c2s.C2SDemandApi)


- [marketplace/public/grpc/demand_handler/v2/gen-doc/demand_common_entities.proto](#marketplace/public/grpc/demand_handler/v2/gen-doc/demand_common_entities.proto)
    - [BookingConstraints](#demand.v2.common.BookingConstraints)
    - [CancellationInfo](#demand.v2.common.CancellationInfo)
    - [DriverDetails](#demand.v2.common.DriverDetails)
    - [PassengerDetails](#demand.v2.common.PassengerDetails)
    - [PublicTransportRouteLeg](#demand.v2.common.PublicTransportRouteLeg)
    - [Ride](#demand.v2.common.Ride)
    - [RideLocation](#demand.v2.common.RideLocation)
    - [RideOffer](#demand.v2.common.RideOffer)
    - [RideOffersResponse](#demand.v2.common.RideOffersResponse)
    - [RidePreferences](#demand.v2.common.RidePreferences)
    - [RideQuery](#demand.v2.common.RideQuery)
    - [RideQueryResponse](#demand.v2.common.RideQueryResponse)
    - [RideStatusLog](#demand.v2.common.RideStatusLog)
    - [RideStatusUpdate](#demand.v2.common.RideStatusUpdate)
    - [RideTrackingDetails](#demand.v2.common.RideTrackingDetails)
    - [Route](#demand.v2.common.Route)
    - [Supplier](#demand.v2.common.Supplier)
    - [TransitOptions](#demand.v2.common.TransitOptions)
    - [Vehicle](#demand.v2.common.Vehicle)

    - [CancellationInfo.Party](#demand.v2.common.CancellationInfo.Party)
    - [CancellationInfo.Status](#demand.v2.common.CancellationInfo.Status)
    - [PublicTransportRouteLeg.PublicTransportMode](#demand.v2.common.PublicTransportRouteLeg.PublicTransportMode)
    - [RideOffer.CancellationPolicy](#demand.v2.common.RideOffer.CancellationPolicy)
    - [RideOffer.SortType](#demand.v2.common.RideOffer.SortType)
    - [RideOffer.TransitType](#demand.v2.common.RideOffer.TransitType)
    - [RideQuery.RideStatusFilter](#demand.v2.common.RideQuery.RideStatusFilter)
    - [RideQuery.SortType](#demand.v2.common.RideQuery.SortType)
    - [RideStatusUpdate.Status](#demand.v2.common.RideStatusUpdate.Status)
    - [Vehicle.VehicleType](#demand.v2.common.Vehicle.VehicleType)




- [marketplace/public/grpc/demand_handler/v2/gen-doc/demand_common_types.proto](#marketplace/public/grpc/demand_handler/v2/gen-doc/demand_common_types.proto)
    - [Address](#demand.v2.common.Address)
    - [Empty](#demand.v2.common.Empty)
    - [Location](#demand.v2.common.Location)
    - [Point](#demand.v2.common.Point)
    - [Price](#demand.v2.common.Price)
    - [PriceEstimate](#demand.v2.common.PriceEstimate)
    - [PriceRange](#demand.v2.common.PriceRange)
    - [TimeRange](#demand.v2.common.TimeRange)





- [marketplace/public/grpc/demand_handler/v2/gen-doc/demand_s2s_messages.proto](#marketplace/public/grpc/demand_handler/v2/gen-doc/demand_s2s_messages.proto)
    - [CancelRideRequest](#demand.v2.s2s.CancelRideRequest)
    - [CancelTrackedRideRequest](#demand.v2.s2s.CancelTrackedRideRequest)
    - [CreatePublicTransportRideRequest](#demand.v2.s2s.CreatePublicTransportRideRequest)
    - [CreateRideRequest](#demand.v2.s2s.CreateRideRequest)
    - [GetOfferTrackingDetailsRequest](#demand.v2.s2s.GetOfferTrackingDetailsRequest)
    - [GetRecentRidesRequest](#demand.v2.s2s.GetRecentRidesRequest)
    - [GetRideListByUserRequest](#demand.v2.s2s.GetRideListByUserRequest)
    - [GetRideListRequest](#demand.v2.s2s.GetRideListRequest)
    - [GetRideLocationRequest](#demand.v2.s2s.GetRideLocationRequest)
    - [GetRideRequest](#demand.v2.s2s.GetRideRequest)
    - [GetRideTrackingDetailsRequest](#demand.v2.s2s.GetRideTrackingDetailsRequest)
    - [RideOffersRequest](#demand.v2.s2s.RideOffersRequest)





- [marketplace/public/grpc/demand_handler/v2/gen-doc/demand_s2s_service.proto](#marketplace/public/grpc/demand_handler/v2/gen-doc/demand_s2s_service.proto)



    - [S2SDemandApi](#demand.v2.s2s.S2SDemandApi)


- [Scalar Value Types](#scalar-value-types)



<a name="marketplace/public/grpc/demand_handler/v2/gen-doc/demand_c2s_messages.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/demand_handler/v2/gen-doc/demand_c2s_messages.proto



<a name="demand.v2.c2s.CancelRideRequest"/>

### CancelRideRequest
A request to cancel a ride


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| ride_id | [string](#string) |  | Mandatory. The unique ride ID. |
| cancel_reason | [string](#string) |  | Optional. Free text. The reason for the cancellation. |






<a name="demand.v2.c2s.CreatePublicTransportRideRequest"/>

### CreatePublicTransportRideRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| offer_id | [string](#string) |  | Mandatory. An offer ID that was returned by GetRideOffers(). |
| passenger | [demand.v2.common.PassengerDetails](#demand.v2.common.PassengerDetails) |  | Mandatory. The passenger details at the time of booking. |
| preferences | [demand.v2.common.RidePreferences](#demand.v2.common.RidePreferences) |  | Optional. Preferences for the ride. NOTE: this field is not yet supported. |






<a name="demand.v2.c2s.CreateRideRequest"/>

### CreateRideRequest
A request to create a new ride by offer ID


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| offer_id | [string](#string) |  | Mandatory. An offer ID that was returned by GetRideOffers(). |
| passenger | [demand.v2.common.PassengerDetails](#demand.v2.common.PassengerDetails) |  | Mandatory. The passenger details at the time of booking. |
| subscribe_to_messages | [google.protobuf.BoolValue](#google.protobuf.BoolValue) |  | DEPRECATED. Please use the RidePreferences object to specify messaging preferences.

Note: this field is deprecated and is ignored. |
| preferences | [demand.v2.common.RidePreferences](#demand.v2.common.RidePreferences) |  | Optional. Preferences for the ride. |






<a name="demand.v2.c2s.GetRideListRequest"/>

### GetRideListRequest
A request to get a ride list according to query parameters.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| query | [demand.v2.common.RideQuery](#demand.v2.common.RideQuery) |  | Optional. The query parameters with which to filter results. If no query parameters are supplied, the query uses the default values for RideQuery fields (see the RideQuery message documentation). |
| get_all_apps | [bool](#bool) |  | Optional. Get rides from all applications. |






<a name="demand.v2.c2s.GetRideLocationRequest"/>

### GetRideLocationRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| ride_id | [string](#string) |  | Mandatory. The ride’s unique ID. |






<a name="demand.v2.c2s.GetRideRequest"/>

### GetRideRequest
A request to get a ride


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| ride_id | [string](#string) |  | Mandatory. The ride’s unique ID. |






<a name="demand.v2.c2s.RideOffersRequest"/>

### RideOffersRequest
A request to get ride offers for a given route. If a prebook_pickup_time value is provided, this is a request for a future pickup.
Otherwise, this is a request for an immediate pickup (within 30 minutes).


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| route | [demand.v2.common.Route](#demand.v2.common.Route) |  | Mandatory. The requested route of the ride. |
| constraints | [demand.v2.common.BookingConstraints](#demand.v2.common.BookingConstraints) |  | Optional. Ride constraints such as passenger count, child seats, number of suitcases, etc. |
| prebook_pickup_time_ms | [uint64](#uint64) |  | FUTURE FEATURE, CURRENTLY UNSUPPORTED: Optional. A future pickup time, which is at least 30 minutes after the request time. An empty value indicates a request for an immediate ride. |
| price_range | [demand.v2.common.PriceRange](#demand.v2.common.PriceRange) |  | FUTURE FEATURE, CURRENTLY UNSUPPORTED: Optional. A requested price range. If this value is set, only offers whose price is within the range are returned. Otherwise, any price is assumed to be acceptable. |
| sort_type | [demand.v2.common.RideOffer.SortType](#demand.v2.common.RideOffer.SortType) |  | FUTURE FEATURE, CURRENTLY UNSUPPORTED: Optional. How to sort the RideOffers, by price or by ETA. (The Marketplace default sort order is by best price, and then minimal ETA.). |
| passenger_note | [string](#string) |  | Optional. A free text note from the passenger. |
| transit_options | [demand.v2.common.TransitOptions](#demand.v2.common.TransitOptions) |  | Optional. Parameters for transit offers. |















<a name="marketplace/public/grpc/demand_handler/v2/gen-doc/demand_c2s_service.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/demand_handler/v2/gen-doc/demand_c2s_service.proto
The client-to-service API








<a name="demand.v2.c2s.C2SDemandApi"/>

### C2SDemandApi
A client-to-service API for creating and tracking rides.
All ride-related entities are created for the current user. The user (or session) is included in the header of all requests.

=== Normal flow before the ride is created ===
The client calls GetRideOffers() according to the time, route, price and other constraints that the user specifies.
The user chooses one ride offer, and the client calls Book().
The client calls GetRide() repeatedly until the ride status is ACCEPTED.
=== Normal flow during the ride ===
The client calls GetRide() repeatedly to get ride status updates.
The client calls GetRideLocation() repeatedly to get ride location and ETA updates. These calls should be made more frequently, as the location changes continuously.
=== Flow for getting updates on multiple rides ===
The client makes an initial call to GetRides() to receive recently updated rides.
The client repeatedly calls GetRides() to get new updates. Starting from the second call to GetRides(), send the &#39;to_update_time&#39; from the previous response as the requested minimal update time.
==== Errors ===
- NOT_FOUND code – may be returned when an entity doesn’t exist, is expired (such as an offer) or belongs to a different user.

=== Future Enhancements ===
Optimization of polling (using ETAG)
History of rides

| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetRideOffers | [RideOffersRequest](#demand.v2.c2s.RideOffersRequest) | [.demand.v2.common.RideOffersResponse](#demand.v2.c2s.RideOffersRequest) | Get ride offers based on a ride request. May take a few seconds. When no offers are available, returns an empty response. Errors: INVALID_ARGUMENT: Invalid field value. For example: prebook_pickup_time is in the past, route.pickup.lat is not a valid latitude, etc. |
| CreateRide | [CreateRideRequest](#demand.v2.c2s.CreateRideRequest) | [.demand.v2.common.Ride](#demand.v2.c2s.CreateRideRequest) | Create a new ride based on an offer ID. If the offer is valid, a ride is returned immediately with the status PROCESSING.

Errors: NOT_FOUND: The offer ID is expired or does not exist ALREADY_EXISTS: A booking already exists for this offer ID (call GetRideOffers to receive new offer IDs). |
| GetRide | [GetRideRequest](#demand.v2.c2s.GetRideRequest) | [.demand.v2.common.Ride](#demand.v2.c2s.GetRideRequest) | Get a ride by ID. Use this call to poll for the ride status (every 10 seconds). NOTE: The status of closed rides (COMPLETED, CANCELLED, REJECTED) never changes. Errors: NOT_FOUND: Ride does not exist |
| GetRides | [GetRideListRequest](#demand.v2.c2s.GetRideListRequest) | [.demand.v2.common.RideQueryResponse](#demand.v2.c2s.GetRideListRequest) | Get rides for the current user. Returns rides that were updated recently (in the last 3 hours(OnGoing)/180 days(Future)/14 days(Past), or after the given from_update_time). |
| CancelRide | [CancelRideRequest](#demand.v2.c2s.CancelRideRequest) | [.demand.v2.common.Empty](#demand.v2.c2s.CancelRideRequest) | Cancel a ride. Returns immediately without waiting for a response from the supplier. Errors: NOT_FOUND: Ride does not exist FAILED_PRECONDITION: Cancel is not allowed by policy, or because the status is REJECTED, COMPLETED, or CANCELLED. |
| GetRideLocationAndEta | [GetRideLocationRequest](#demand.v2.c2s.GetRideLocationRequest) | [.demand.v2.common.RideLocation](#demand.v2.c2s.GetRideLocationRequest) | Returns the geo-location of the ride. Use this call to poll for the ride location (every 10 seconds) NOTES: Test the flag Ride.status_log.is_ride_location_available, to learn whether ride locations are supported. Rides which are closed (COMPLETED, CANCELLED, REJECTED) never change their location. Errors: NOT_FOUND: Ride does not exist |
| CreatePublicTransportRide | [CreatePublicTransportRideRequest](#demand.v2.c2s.CreatePublicTransportRideRequest) | [.demand.v2.common.Empty](#demand.v2.c2s.CreatePublicTransportRideRequest) | Notify the marketplace that a public transportation offer was chosen |





<a name="marketplace/public/grpc/demand_handler/v2/gen-doc/demand_common_entities.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/demand_handler/v2/gen-doc/demand_common_entities.proto
Common entities, such as Route, Ride and RideOffer


<a name="demand.v2.common.BookingConstraints"/>

### BookingConstraints
A structure for defining the number of passengers and special requirements for the ride.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| passengers_no | [uint32](#uint32) |  | The number of passengers (1 or more). |
| suitcases_no | [uint32](#uint32) |  | The number of suitcases (0 or more). |






<a name="demand.v2.common.CancellationInfo"/>

### CancellationInfo
Information about a ride cancellation


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| cancelling_party | [CancellationInfo.Party](#demand.v2.common.CancellationInfo.Party) |  | Which party canceled the ride. |
| cancel_reason | [string](#string) |  | The reason the ride was canceled (a free-text string). |
| request_time_ms | [uint64](#uint64) |  | The time the cancellation was requested. |
| status | [CancellationInfo.Status](#demand.v2.common.CancellationInfo.Status) |  | The status of the cancellation request. |






<a name="demand.v2.common.DriverDetails"/>

### DriverDetails
Driver information


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The driver’s first and last name. |
| phone_number | [string](#string) |  | The driver’s telephone number. |
| photo_url | [string](#string) |  | A URL pointing to the driver’s photo. This is mandatory in some countries. |
| driving_license_id | [string](#string) |  | The driver’s driving license ID. This is mandatory in some countries. |






<a name="demand.v2.common.PassengerDetails"/>

### PassengerDetails
Passenger information


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | Mandatory. The passenger’s first and last name. |
| phone_number | [string](#string) |  | The passenger’s telephone number. |
| photo_url | [string](#string) |  | Optional. A URL pointing to the passenger’s photo. |
| email | [string](#string) |  | Optional. The passenger&#39;s email address. |






<a name="demand.v2.common.PublicTransportRouteLeg"/>

### PublicTransportRouteLeg



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| mode | [PublicTransportRouteLeg.PublicTransportMode](#demand.v2.common.PublicTransportRouteLeg.PublicTransportMode) |  | Type of transportation for the leg. |
| duration_ms | [uint64](#uint64) |  | Duration of the leg in milliseconds. |
| distance_meters | [uint32](#uint32) |  | Distance of the leg in meters. |
| line | [string](#string) |  | Name of the line of this public transportation (if relevant). |
| origin | [Location](#demand.v2.common.Location) |  | Origin location of the leg. |
| departure_time_ms | [uint64](#uint64) |  | Time of departure from the start of the leg in milliseconds. |
| destination | [Location](#demand.v2.common.Location) |  | Destination location of the leg. |
| arrival_time_ms | [uint64](#uint64) |  | Time of arrival from the start of the leg in milliseconds. |
| operator | [string](#string) |  | Name of the public transportation operator for this leg. |






<a name="demand.v2.common.Ride"/>

### Ride
A ride with a specific supplier. This entity contains relatively static info: driver, vehicle, passengers etc.
The more dynamic info of the ride, including its progress along the route, is in the entity Ride.

Below is the lifecycle of the ride:

PROCESSING [initial status of the ride after CreateRide(), lasting 0-15 sec.]
PROCESSING --&gt; ACCEPTED [For a pre-booked ride, this status will be active until 30min before the ride.]
PROCESSING --&gt; REJECTED [The ride has been rejected. Terminal state.]
ACCEPTED --&gt; PROCESSING [This transition occurs if the supplier cancels a pre-booked ride, and the Marketplace tries to book a new ride.]
ACCEPTED --&gt; ((NORMAL FLOW)) --&gt; COMPLETE [The ride has been completed. Terminal state.]

The typical flow is: DRIVER_ASSIGNED --&gt; DRIVER_EN_ROUTE --&gt; AT_PICKUP --&gt; PASSENGER_ON_BOARD --&gt; AT_DROPOFF

CANCELLED [Terminal state. Can be reached from any other state, if a demander or supplier cancels the ride.]

NOTE: Once a ride reaches a terminal state, it cannot transition to any other state.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| user_id | [string](#string) |  | The ID of the user who created this ride. |
| ride_id | [string](#string) |  | A unique ride id. |
| route | [Route](#demand.v2.common.Route) |  | The ride route. |
| prebook_pickup_time_ms | [uint64](#uint64) |  | Optional. For a pre-booked ride, contains the requested pickup time. |
| booking_estimated_price | [PriceEstimate](#demand.v2.common.PriceEstimate) |  | Optional. The estimated price at the time of booking. |
| constraints | [BookingConstraints](#demand.v2.common.BookingConstraints) |  | Constraints defined at the time of booking, such as number of passengers and suitcases. |
| status_log | [RideStatusLog](#demand.v2.common.RideStatusLog) |  | The ride’s current status, and status history. |
| supplier | [Supplier](#demand.v2.common.Supplier) |  | Supplier details. |
| passenger | [PassengerDetails](#demand.v2.common.PassengerDetails) |  | The passenger details at the time of ride creation. |
| passenger_note | [string](#string) |  | Optional. A note added by the passenger at the time of ride creation. Can include additional information about the pickup or other special requests. |
| driver | [DriverDetails](#demand.v2.common.DriverDetails) |  | Optional. This field is only filled when the ride status changes to DRIVER_ASSIGNED and after. |
| vehicle | [Vehicle](#demand.v2.common.Vehicle) |  | Optional. This field is only filled when the ride status changes to DRIVER_ASSIGNED and after. |
| cancellation_policy | [RideOffer.CancellationPolicy](#demand.v2.common.RideOffer.CancellationPolicy) |  | The cancellation policy for the ride. |
| cancellation_info | [CancellationInfo](#demand.v2.common.CancellationInfo) |  | Optional. When a cancellation occurs, this field contains information about the cancellation. |
| cancellation_request_received_but_not_allowed | [bool](#bool) |  | When a cancellation occurs, this field value is TRUE if cancellation isn&#39;t allowed. |
| price | [Price](#demand.v2.common.Price) |  | Optional. The price of the ride updated by the supplier. |
| app_id | [string](#string) |  | Optional. The ID of the app. |
| confirmed_pickup_point | [Point](#demand.v2.common.Point) |  | Optional. The ride confirmed pickup point calculated by Here-API. |






<a name="demand.v2.common.RideLocation"/>

### RideLocation
Provides the real-time location and progress of the vehicle. Updated every ~10 seconds.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| ride_id | [string](#string) |  | The ID of the ride. |
| vehicle_location | [Point](#demand.v2.common.Point) |  | Optional. The current location of the vehicle. |
| estimated_pickup_time_ms | [uint64](#uint64) |  | Optional. The estimated time of pickup, constantly updated until the vehicle is at the pickup location. This field will be deprecated soon, please use estimated_pickup_time_seconds instead. |
| estimated_dropoff_time_ms | [uint64](#uint64) |  | Optional. The estimated time of drop-off, constantly updated until the vehicle is at the drop-off location. This field will be deprecated soon, please use estimated_dropoff_time_seconds instead. |
| last_update_time_ms | [uint64](#uint64) |  | The last time this entity is updated. Used for tracking updates. |
| estimated_pickup_time_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Pickup time estimate sent by the supplier. |
| estimated_dropoff_time_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Drop-off time estimate sent by the supplier or calculated by Marketplace. |






<a name="demand.v2.common.RideOffer"/>

### RideOffer
An offer for a ride on the given route.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| offer_id | [string](#string) |  | A unique offer ID. If this offer is chosen, the client sends this ID when calling CreateRide. |
| supplier | [Supplier](#demand.v2.common.Supplier) |  | The supplier details. |
| route | [Route](#demand.v2.common.Route) |  | The ride route that the supplier suggests. |
| estimated_pickup_time_ms | [uint64](#uint64) |  | Optional. Pickup time estimate sent by the supplier. NOTE: This field will be deprecated soon, please use estimated_pickup_time_seconds instead. |
| estimated_dropoff_time_ms | [uint64](#uint64) |  | Optional. Drop-off time estimate sent by the supplier. NOTE: This field will be deprecated soon, please use estimated_ride_duration_seconds instead. |
| price_estimation | [PriceEstimate](#demand.v2.common.PriceEstimate) |  | Optional. A price estimate for the ride. |
| offer_expiration_time_ms | [uint64](#uint64) |  | The offer expiration time (in milliseconds from the time the offer is sent). |
| cancellation_policy | [RideOffer.CancellationPolicy](#demand.v2.common.RideOffer.CancellationPolicy) |  | The cancellation policy of the supplier (cancellation allowed or not allowed). |
| duration_ms | [uint64](#uint64) |  | Duration of the route in milliseconds. NOTE: this field will be deprecated soon. Please use duration_seconds instead. |
| transfers | [uint32](#uint32) |  | Number of transport changes to reach the destination. |
| legs | [PublicTransportRouteLeg](#demand.v2.common.PublicTransportRouteLeg) | repeated | A list of transportation legs for the route, if this offer is a public transportation offer. |
| transit_type | [RideOffer.TransitType](#demand.v2.common.RideOffer.TransitType) |  | Specifies the transit type of this offer. |
| estimated_pickup_time_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Optional. Pickup time estimate sent by the supplier. |
| estimated_ride_duration_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Optional. Drop-off time estimate sent by the supplier or calculated by Marketplace. This is the time between pickup to dropoff. It does not contain the time to pickup. |
| duration_seconds | [uint64](#uint64) |  | Duration of the route in seconds. |






<a name="demand.v2.common.RideOffersResponse"/>

### RideOffersResponse
A list of available ride offers


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| offers | [RideOffer](#demand.v2.common.RideOffer) | repeated | A list of ride offers. |






<a name="demand.v2.common.RidePreferences"/>

### RidePreferences
Preferences of a ride


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| subscribe_to_messages | [google.protobuf.BoolValue](#google.protobuf.BoolValue) |  | Optional. Specifies if messages about the ride will be sent to the passenger. Default is false. |






<a name="demand.v2.common.RideQuery"/>

### RideQuery
A query for a list of rides matching the query filters. Used as parameter for GetRides(), which supports pagination, sorting and filtering.

To fetch the next page of results, copy the pagination field from the response to the RideQuery.from_time_ms field:
next_request.from_time_ms = response.to_time_ms

Paging can be used in 2 ways: ENDLESS PAGING and SINGLE SNAPSHOT.

ENDLESS PAGING - relevant to ascending sort orders.
In this mode, the client calls GetRides() at regular intervals to receive new or updated records.

Use the sort order UPDATE_TIME_ASC to receive all changes on rides.
Use the sort order CREATE_TIME_ASC to receive each ride exactly once (without updates).
Use the sort order PICKUP_TIME_ASC to query for future rides.

SINGLE SNAPSHOT - in this mode, the client wants to fetch all the rides currently available, and needs to know what is the last page.
To identify the last page, set the &#39;limit&#39; field in the RideQuery, and check if the amount of rides in the result
is lower than the limit. By default any result with less than 200 rides is the last page.

NOTE:
- When the sort is by CREATE_TIME (asc or desc), rides never repeat between pages.
- When the sort is by UPDATE_TIME (asc or desc), rides in previous pages can appear again (because of updates).
- When the sort is by PICKUP_TIME (asc or desc), rides in previous pages can appear again, but rarely.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| from_time_ms | [uint64](#uint64) |  | Optional. Filters rides according to update or creation time (depending on the sort type). When the sort is UPDATE_TIME_ASC, returns rides UPDATED AFTER this time. When the sort is UPDATE_TIME_DESC, returns rides UPDATED BEFORE this time. When the sort is CREATE_TIME_ASC, returns rides CREATED AFTER this time. When the sort is CREATE_TIME_DESC, return rides CREATED BEFORE this time.

Default value for ascending sort orders is NOW-3 hours, expect for FUTURE or PAST rides. Default value for FUTURE rides is Now-180 days. Default value for PAST rides is NOW-14 days. Default value for descending sort orders is NOW. This value is in UTC (milliseconds since Epoch time). |
| limit | [uint32](#uint32) |  | Optional. The maximal number of rides to return. When not set, the default is 200. |
| status_filter | [RideQuery.RideStatusFilter](#demand.v2.common.RideQuery.RideStatusFilter) |  | Optional. Return only rides with the given status. When not set, rides with all statuses are returned. |
| sort_by | [RideQuery.SortType](#demand.v2.common.RideQuery.SortType) |  | Optional. Default is UPDATE_TIME_ASC. |






<a name="demand.v2.common.RideQueryResponse"/>

### RideQueryResponse
A list of rides that matches a ride query


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| rides | [Ride](#demand.v2.common.Ride) | repeated | The list of rides that matched the query. |
| from_time_ms | [uint64](#uint64) |  | The earliest update time in this result set. The lowest possible value is current time minus 3 hours. This value is in UTC, in milliseconds since Epoch time. |
| to_time_ms | [uint64](#uint64) |  | A time &#34;cursor&#34; for pagination. Contains the last time in the result set, ordered by the sort type. To get the next page, pass this value to the next call for GetRides() to field RideQuery.from_time_ms This value is in UTC, in milliseconds since Epoch time. |






<a name="demand.v2.common.RideStatusLog"/>

### RideStatusLog
The current status of the ride, including some audit info, and a history of previous statuses


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| last_update_time_ms | [uint64](#uint64) |  | The last time this entity was updated. Used for tracking updates. |
| create_time_ms | [uint64](#uint64) |  | The time the booking was created. |
| closed_time_ms | [uint64](#uint64) |  | Optional. If relevant, the time the ride was closed (reached a terminal state). |
| is_ride_location_available | [bool](#bool) |  | If this value is TRUE, you can retrieve live updates on the ride’s location by calling GetRideLocation (during statuses DRIVER_ASSIGNED to COMPLETED). |
| current_status | [RideStatusUpdate.Status](#demand.v2.common.RideStatusUpdate.Status) |  | The ride’s current status. |
| prev_statuses | [RideStatusUpdate](#demand.v2.common.RideStatusUpdate) | repeated | A list of previous ride statuses, ordered by their timestamp values. |






<a name="demand.v2.common.RideStatusUpdate"/>

### RideStatusUpdate
A ride status update, and the time it occurred. Used in the status log.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| status | [RideStatusUpdate.Status](#demand.v2.common.RideStatusUpdate.Status) |  | The new ride status. |
| timestamp_ms | [uint64](#uint64) |  | The time the ride status changed (UNIX Epoch time in milliseconds). |






<a name="demand.v2.common.RideTrackingDetails"/>

### RideTrackingDetails
provides ride tracking details for a ride


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| ride_tracking_id | [string](#string) |  | The ride tracking ID. |
| status_log | [RideStatusLog](#demand.v2.common.RideStatusLog) |  | The tracked ride ride status log. |
| driver | [DriverDetails](#demand.v2.common.DriverDetails) |  | The ride&#39;s driver details. |
| vehicle | [Vehicle](#demand.v2.common.Vehicle) |  | The ride&#39;s vehicle details. |
| supplier | [Supplier](#demand.v2.common.Supplier) |  | The ride&#39;s supplier details. |
| location_and_eta | [RideLocation](#demand.v2.common.RideLocation) |  | The ride&#39;s location and ETA. |
| cancellation_info | [CancellationInfo](#demand.v2.common.CancellationInfo) |  | When cancellation occurs, this field contains information about the cancellation. |






<a name="demand.v2.common.Route"/>

### Route
A route between a start point and an end point


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| pickup | [Location](#demand.v2.common.Location) |  | Mandatory. The route’s pickup location. |
| destination | [Location](#demand.v2.common.Location) |  | Mandatory. The route’s destination location. |






<a name="demand.v2.common.Supplier"/>

### Supplier
Ride supplier details


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| supplier_id | [string](#string) |  | A unique supplier ID. |
| english_name | [string](#string) |  | The name of the supplier, in English. |
| local_name | [string](#string) |  | Optional. The name of the supplier in the local language. |
| logo_url | [string](#string) |  | Optional. A URL pointing to a logo image for the supplier. |
| phone_number | [string](#string) |  | The supplier’s telephone number. |
| address | [string](#string) |  | The supplier’s address. |






<a name="demand.v2.common.TransitOptions"/>

### TransitOptions



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| max_transfers | [google.protobuf.Int32Value](#google.protobuf.Int32Value) |  | Optional. Maximum number of changes or transfers allowed in a route. Default is unlimited. Range is 0-6. |
| max_walking_distance_meters | [google.protobuf.Int32Value](#google.protobuf.Int32Value) |  | Optional. Specifies a maximum walking distance in meters. Default is 2000. Range is 0-6000. |
| locale | [google.protobuf.StringValue](#google.protobuf.StringValue) |  | Optional. The client&#39;s locale. Complies with the ISO 639-1 standard and defaults to en. |






<a name="demand.v2.common.Vehicle"/>

### Vehicle
Vehicle details


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| license_plate_number | [string](#string) |  | The vehicle’s license plate number. |
| vehicle_type | [Vehicle.VehicleType](#demand.v2.common.Vehicle.VehicleType) |  | The vehicle type (standard, limo, van). |
| make | [string](#string) |  | The vehicle make. |
| model | [string](#string) |  | The vehicle model. |
| color | [string](#string) |  | The vehicle color. |








<a name="demand.v2.common.CancellationInfo.Party"/>

### CancellationInfo.Party


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 0 | The cancelling party is unknown. |
| DEMANDER | 1 | The client cancelled the ride. |
| SUPPLIER | 2 | The supplier cancelled the ride. |



<a name="demand.v2.common.CancellationInfo.Status"/>

### CancellationInfo.Status


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN_STATUS | 0 | The cancellation status is unknown. |
| PROCESSING | 1 | The cancellation request is being processed. |
| ACCEPTED | 2 | The cancellation request is accepted. |
| REJECTED | 3 | The cancellation request is rejected. |



<a name="demand.v2.common.PublicTransportRouteLeg.PublicTransportMode"/>

### PublicTransportRouteLeg.PublicTransportMode


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN_PUBLIC_TRANSPORT_MODE | 0 | Unknown. |
| HIGH_SPEED_TRAIN | 1 | High-speed train. |
| INTERCITY_TRAIN | 2 | Intercity/Euro-City train. |
| INTER_REGIONAL_TRAIN | 3 | Inter-regional or fast train. |
| REGIONAL_TRAIN | 4 | Regional train. |
| CITY_TRAIN | 5 | City train. |
| BUS | 6 | Bus. |
| FERRY | 7 | Boat or ferry. |
| SUBWAY | 8 | Subway/metro train. |
| LIGHT_RAIL | 9 | Tram. |
| PRIVATE_BUS | 10 | Privately-ordered bus or taxi. |
| INCLINED | 11 | Inclined tram/funicular. |
| AERIAL | 12 | Cable car. |
| BUS_RAPID | 13 | Rapid bus. |
| MONORAIL | 14 | Monorail. |
| WALK | 15 | Walking. |



<a name="demand.v2.common.RideOffer.CancellationPolicy"/>

### RideOffer.CancellationPolicy
Info about the ride cancellation policy

| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN_CANCEL_POLICY | 0 | Unknown cancellation policy. |
| ALLOWED | 1 | Cancellation by the client is allowed. |
| NOT_ALLOWED | 2 | Cancellation by the client is not allowed. |



<a name="demand.v2.common.RideOffer.SortType"/>

### RideOffer.SortType
Types of sort orders for the returned ride offers

| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN_SORT_TYPE | 0 |  |
| BY_PRICE | 1 | Sort by price (lowest price first). |
| BY_ETA | 2 | Sort by arrival time (earliest arrival time first). |



<a name="demand.v2.common.RideOffer.TransitType"/>

### RideOffer.TransitType


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN_TRANSIT_TYPE | 0 | Unknown transit type. |
| TAXI | 1 | Taxi ride |
| PUBLIC_TRANSPORT | 2 | Public transport ride. |



<a name="demand.v2.common.RideQuery.RideStatusFilter"/>

### RideQuery.RideStatusFilter


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN_RIDE_STATUS_FILTER | 0 | Unknown ride status. |
| PAST | 1 | Terminated rides (includes the statuses: COMPLETED, REJECTED or CANCELLED). Default: in the past 14 days. |
| FUTURE | 2 | Pre-booked rides in status PROCESSING or ACCEPTED. Default: in the past 180 days. |
| ONGOING | 3 | Ongoing rides (all rides other than PAST and FUTURE). Default: in the past 3 hours. |
| ALL | 4 | All rides. |



<a name="demand.v2.common.RideQuery.SortType"/>

### RideQuery.SortType


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN_SORT_TYPE | 0 | Unknown sort order. |
| UPDATE_TIME_ASC | 1 | Ascending order of update time. |
| UPDATE_TIME_DESC | 2 | Descending order of update time. |
| CREATE_TIME_ASC | 3 | Ascending order of creation time. |
| CREATE_TIME_DESC | 4 | Descending order of creation time. |



<a name="demand.v2.common.RideStatusUpdate.Status"/>

### RideStatusUpdate.Status
Ride status values

| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 0 | Unknown. |
| PROCESSING | 1 | Looking for a supplier. |
| REJECTED | 2 | The supplier cannot fulfill the request. Terminal state. |
| ACCEPTED | 3 | A supplier accepted the ride, but a driver is not yet assigned. For a pre-booked ride, this state may last a long while. |
| DRIVER_ASSIGNED | 4 | Driver and vehicle are assigned to the ride. |
| DRIVER_EN_ROUTE | 5 | Vehicle on its way to pickup. |
| AT_PICKUP | 6 | Vehicle at pickup. |
| PASSENGER_ON_BOARD | 7 | Vehicle on the way, and passenger on board. |
| AT_DROPOFF | 8 | Vehicle arrived at drop-off. |
| COMPLETED | 9 | Ride finished successfully. Terminal state. |
| CANCELLED | 10 | Ride cancelled by supplier or demander. Terminal state. |
| FAILURE | 11 | Ride closed after a duration with no updates. |



<a name="demand.v2.common.Vehicle.VehicleType"/>

### Vehicle.VehicleType


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 0 |  |
| STANDARD | 1 | Standard vehicle. |
| LIMO | 2 | Limousine. |
| VAN | 3 | Van. |
| OTHER | 4 | Other vehicle. |
| NOT_SUPPLIED | 5 | Vehicle type not supplied. |










<a name="marketplace/public/grpc/demand_handler/v2/gen-doc/demand_common_types.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/demand_handler/v2/gen-doc/demand_common_types.proto
Basic types


<a name="demand.v2.common.Address"/>

### Address



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| country | [string](#string) |  | Localized country name. |
| country_code | [string](#string) |  | ISO 3166-alpha-3 country code. |
| state | [string](#string) |  | State (first subdivision level below the country, if relevant). |
| county | [string](#string) |  | County (second subdivision level below the country, if relevant). |
| city | [string](#string) |  | City/town. |
| district | [string](#string) |  | District (subdivision level below the city). |
| sub_district | [string](#string) |  | Sub-district (subdivision level below the district; e.g. commonly used in IND). |
| street | [string](#string) |  | Street name. |
| house_number | [string](#string) |  | House number; depending on regional characteristics, can also be house name. |
| postal_code | [string](#string) |  | Postal code (zipcode). |
| building | [string](#string) |  | Building name; e.g. commonly used in HKG. |
| line | [string](#string) | repeated | Formatted address lines. |






<a name="demand.v2.common.Empty"/>

### Empty







<a name="demand.v2.common.Location"/>

### Location
A start/end/midpoint location in a ride


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| point | [Point](#demand.v2.common.Point) |  | Geo-location (latitude and longitude). |
| address | [Address](#demand.v2.common.Address) |  | Street address. |
| free_text | [string](#string) |  | Place name or street address in a free text format. |






<a name="demand.v2.common.Point"/>

### Point
A point in the world, expressed as a {latitude, longitude) pair. Latitude values range from -180 to 180.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| lat | [double](#double) |  | Latitude. |
| lng | [double](#double) |  | Longitude. |






<a name="demand.v2.common.Price"/>

### Price
A price value


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| amount | [string](#string) |  | The price’s numeric amount in decimal format. For example &#34;12.5&#34;, &#34;12&#34;, etc. Unsigned. |
| currency_code | [string](#string) |  | The price currency. An ISO 4217 Currency Code, for example: &#34;USD&#34;, &#34;EUR&#34;, &#34;JPY&#34;. |






<a name="demand.v2.common.PriceEstimate"/>

### PriceEstimate
A price estimate for a ride. Contains only one field value: either a fixed price, or a price range.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| fixed | [Price](#demand.v2.common.Price) |  | A single fixed price amount. |
| range | [PriceRange](#demand.v2.common.PriceRange) |  | Lower and upper limits of a price range. |






<a name="demand.v2.common.PriceRange"/>

### PriceRange
A price range. For example, the range $10.75-$12 is represented as: { from_amount: &#34;10.75&#34;, to_amount: &#34;12&#34;, currency_code: &#34;USD&#34;}


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| lower_bound | [string](#string) |  | The range’s lower limit, for example: &#34;12.5&#34;, &#34;12&#34;, etc. Unsigned. |
| upper_bound | [string](#string) |  | The range’s upper limit, for example: &#34;12.5&#34;, &#34;12&#34;, etc. Unsigned. |
| currency_code | [string](#string) |  | The price currency. An ISO 4217 Currency Code, for example: &#34;USD&#34;, &#34;EUR&#34;, &#34;JPY&#34;. |






<a name="demand.v2.common.TimeRange"/>

### TimeRange
A time range


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| from_ms | [uint64](#uint64) |  | The time range’s lower limit (in milliseconds from Epoch time). |
| to_ms | [uint64](#uint64) |  | The time range’s upper limit (in milliseconds from Epoch time). |















<a name="marketplace/public/grpc/demand_handler/v2/gen-doc/demand_s2s_messages.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/demand_handler/v2/gen-doc/demand_s2s_messages.proto



<a name="demand.v2.s2s.CancelRideRequest"/>

### CancelRideRequest
A request to cancel a ride


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| ride_id | [string](#string) |  | Mandatory. The unique ride ID. |
| user_id | [google.protobuf.StringValue](#google.protobuf.StringValue) |  | Optional. The ID of the requesting user. |
| cancel_reason | [string](#string) |  | Optional. Free text. The reason for the cancellation. |






<a name="demand.v2.s2s.CancelTrackedRideRequest"/>

### CancelTrackedRideRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| ride_tracking_id | [string](#string) |  | Mandatory. The ID from the ride tracker url. |
| passenger_phone | [string](#string) |  | Mandatory. the passenger phone for validation purposes. |
| cancel_reason | [string](#string) |  | Optional. Free text. The reason for the cancellation. |






<a name="demand.v2.s2s.CreatePublicTransportRideRequest"/>

### CreatePublicTransportRideRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| user_id | [string](#string) |  | Mandatory. The user ID for which the ride is created. |
| offer_id | [string](#string) |  | Mandatory. An offer ID that was returned by GetRideOffers(). |
| passenger | [demand.v2.common.PassengerDetails](#demand.v2.common.PassengerDetails) |  | Mandatory. The passenger details at the time of booking. |
| preferences | [demand.v2.common.RidePreferences](#demand.v2.common.RidePreferences) |  | Optional. Preferences for the ride NOTE: this field is not yet supported. |






<a name="demand.v2.s2s.CreateRideRequest"/>

### CreateRideRequest
A request to create a new ride by offer ID


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| user_id | [string](#string) |  | Mandatory. The user ID for which the ride is created. |
| offer_id | [string](#string) |  | Mandatory. An offer ID that was returned by GetRideOffers(). |
| passenger | [demand.v2.common.PassengerDetails](#demand.v2.common.PassengerDetails) |  | Mandatory. The passenger details at the time of booking. |
| subscribe_to_messages | [google.protobuf.BoolValue](#google.protobuf.BoolValue) |  | DEPRECATED. Please use the RidePreferences object to specify messaging preferences.

Note: this field is deprecated and is ignored. |
| preferences | [demand.v2.common.RidePreferences](#demand.v2.common.RidePreferences) |  | Optional. Preferences for the ride. |






<a name="demand.v2.s2s.GetOfferTrackingDetailsRequest"/>

### GetOfferTrackingDetailsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| offer_tracking_id | [string](#string) |  | Mandatory. The ID from the public transport tracker url. |
| transit_type | [demand.v2.common.RideOffer.TransitType](#demand.v2.common.RideOffer.TransitType) |  | Mandatory. The transit type of the offer. |






<a name="demand.v2.s2s.GetRecentRidesRequest"/>

### GetRecentRidesRequest
A request to get recently-update rides


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| min_update_time_ms | [uint64](#uint64) |  | Optional. The minimum update time. If this value is supplied, only rides updated AFTER this time are returned. Otherwise, the default is used (the current time minus 2 hours). |






<a name="demand.v2.s2s.GetRideListByUserRequest"/>

### GetRideListByUserRequest
A request to get rides for a specific user


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| query | [demand.v2.common.RideQuery](#demand.v2.common.RideQuery) |  | Optional. Additional query parameters. |
| user_id | [string](#string) |  | Mandatory. The ID of the user whose rides you want to retrieve. |
| get_all_apps | [bool](#bool) |  | Optional. Get rides from all applications. |






<a name="demand.v2.s2s.GetRideListRequest"/>

### GetRideListRequest
A request to get a ride list according to query parameters


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| query | [demand.v2.common.RideQuery](#demand.v2.common.RideQuery) |  | Optional. The query parameters with which to filter the rides returned. If no query parameters are supplied, the query uses the default values for RideQuery fields (see the RideQuery message documentation). |
| get_all_apps | [bool](#bool) |  | Optional. Get rides from all applications. |






<a name="demand.v2.s2s.GetRideLocationRequest"/>

### GetRideLocationRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| ride_id | [string](#string) |  | Mandatory. The ride’s unique ID. |
| user_id | [google.protobuf.StringValue](#google.protobuf.StringValue) |  | Optional. The ID of the requesting user. |






<a name="demand.v2.s2s.GetRideRequest"/>

### GetRideRequest
A request to get a ride


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| ride_id | [string](#string) |  | Mandatory. The ride’s unique ID. |
| user_id | [google.protobuf.StringValue](#google.protobuf.StringValue) |  | Optional. The ID of the requesting user. |






<a name="demand.v2.s2s.GetRideTrackingDetailsRequest"/>

### GetRideTrackingDetailsRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| ride_tracking_id | [string](#string) |  | Mandatory. The ID from the ride tracker url. |






<a name="demand.v2.s2s.RideOffersRequest"/>

### RideOffersRequest
A request to get ride offers for a given route. If a prebook_pickup_time value is provided, this is a request for a future pickup.
Otherwise, this is a request for an immediate pickup (within 30 minutes).


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| user_id | [string](#string) |  | Mandatory. The ID of the user requesting the ride. |
| route | [demand.v2.common.Route](#demand.v2.common.Route) |  | Mandatory. The requested route of the ride. |
| constraints | [demand.v2.common.BookingConstraints](#demand.v2.common.BookingConstraints) |  | Optional. Ride constraints such as passenger count, child seats, number of suitcases, etc. |
| prebook_pickup_time_ms | [uint64](#uint64) |  | Optional. A future pickup time, which is at least 30 minutes after the request time. An empty value indicates a request for an immediate ride. |
| price_range | [demand.v2.common.PriceRange](#demand.v2.common.PriceRange) |  | FUTURE FEATURE, CURRENTLY UNSUPPORTED: Optional. A requested price range. If this value is set, only offers whose price is within the range are returned. Otherwise, any price is assumed to be acceptable. |
| sort_type | [demand.v2.common.RideOffer.SortType](#demand.v2.common.RideOffer.SortType) |  | FUTURE FEATURE, CURRENTLY UNSUPPORTED: Optional. How to sort the RideOffers, by price or by ETA. (The Marketplace default sort order is by best price, and then minimal ETA.). |
| passenger_note | [string](#string) |  | Optional. A free text note from the passenger. |
| transit_options | [demand.v2.common.TransitOptions](#demand.v2.common.TransitOptions) |  | Optional. Parameters for transit options. |















<a name="marketplace/public/grpc/demand_handler/v2/gen-doc/demand_s2s_service.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/demand_handler/v2/gen-doc/demand_s2s_service.proto
The server to service API








<a name="demand.v2.s2s.S2SDemandApi"/>

### S2SDemandApi
A service-to-service API for creating and tracking rides.
All ride-related entities are created for the current user. The user (or session) is included in the header of all requests.

=== Normal flow before the ride is created ===
The client calls GetRideOffers() according to the time, route, price and other constraints that the user specifies.
The user chooses one ride offer, and the client calls Book().
The client calls GetRide() repeatedly until the ride status is ACCEPTED.
=== Normal flow during the ride ===
The client calls GetRide() repeatedly to get ride status updates.
The client calls GetRideLocation() repeatedly to get ride location and ETA updates. These calls should be made more frequently, as the location changes continuously.
=== Flow for getting updates on multiple rides ===
The client makes an initial call to GetRides() to receive recently updated rides.
The client repeatedly calls GetRides() to get new updates. Starting from the second call to GetRides(), send the &#39;to_update_time&#39; from the previous response as the requested minimal update time.
==== Errors ===
- NOT_FOUND code – may be returned when an entity doesn’t exist, is expired (such as an offer) or belongs to a different user.

=== Future Enhancements ===
Optimization of polling (using ETAG)
History of rides

| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| GetRideOffers | [RideOffersRequest](#demand.v2.s2s.RideOffersRequest) | [.demand.v2.common.RideOffersResponse](#demand.v2.s2s.RideOffersRequest) | Get ride offers based on a ride request. May take a few seconds. When no offers are available, returns an empty response. Errors: INVALID_ARGUMENT: Invalid field value. For example: prebook_pickup_time is in the past, route.pickup.lat is not a valid latitude, etc. |
| CreateRide | [CreateRideRequest](#demand.v2.s2s.CreateRideRequest) | [.demand.v2.common.Ride](#demand.v2.s2s.CreateRideRequest) | Create a new ride based on an offer ID. If the offer is valid, a ride is returned immediately with the status PROCESSING.

Errors: NOT_FOUND: The offer ID is expired or does not exist ALREADY_EXISTS: A booking already exists for this offer ID (call GetRideOffers to receive new offer IDs). |
| GetRide | [GetRideRequest](#demand.v2.s2s.GetRideRequest) | [.demand.v2.common.Ride](#demand.v2.s2s.GetRideRequest) | Get a ride by ID. Use this call to poll for the ride status (every 10 seconds). NOTE: The status of closed rides (COMPLETED, CANCELLED, REJECTED) never changes. Errors: NOT_FOUND: Ride does not exist. |
| GetRidesByUser | [GetRideListByUserRequest](#demand.v2.s2s.GetRideListByUserRequest) | [.demand.v2.common.RideQueryResponse](#demand.v2.s2s.GetRideListByUserRequest) | Get rides for a single user. Returns rides that were updated recently (in the last 3 hours, or after the given from_update_time). |
| GetRides | [GetRideListRequest](#demand.v2.s2s.GetRideListRequest) | [.demand.v2.common.RideQueryResponse](#demand.v2.s2s.GetRideListRequest) | Get rides for all users. Returns rides that were updated recently (in the last 3 hours(OnGoing)/180 days(Future)/14 days(Past), or after the given from_update_time). |
| CancelRide | [CancelRideRequest](#demand.v2.s2s.CancelRideRequest) | [.demand.v2.common.Empty](#demand.v2.s2s.CancelRideRequest) | Cancel a ride. Returns immediately without waiting for a response from the supplier. Errors: NOT_FOUND: Ride does not exist. FAILED_PRECONDITION: Cancel is not allowed by policy, or because the ride status is REJECTED, COMPLETED, or CANCELLED. |
| GetRideLocationAndEta | [GetRideLocationRequest](#demand.v2.s2s.GetRideLocationRequest) | [.demand.v2.common.RideLocation](#demand.v2.s2s.GetRideLocationRequest) | Returns the geo-location of the ride. Use this call to poll for the ride location (every 10 seconds) NOTES: Test the flag Ride.status_log.is_ride_location_available, to learn whether ride locations are supported. Rides which are closed (COMPLETED, CANCELLED, REJECTED) never change their location. Errors: NOT_FOUND: Ride does not exist |
| CreatePublicTransportRide | [CreatePublicTransportRideRequest](#demand.v2.s2s.CreatePublicTransportRideRequest) | [.demand.v2.common.Empty](#demand.v2.s2s.CreatePublicTransportRideRequest) | Notify the marketplace that a public transportation offer was chosen |
| GetRideTrackingDetails | [GetRideTrackingDetailsRequest](#demand.v2.s2s.GetRideTrackingDetailsRequest) | [.demand.v2.common.RideTrackingDetails](#demand.v2.s2s.GetRideTrackingDetailsRequest) | Returns the ride tracking details by ride tracking ID Errors: INVALID_ARGUMENT - ride tracking id was not supplied NOT_FOUND - ride not found for the specified ride tracking ID, or ride tracking ID is invalid |
| CancelTrackedRide | [CancelTrackedRideRequest](#demand.v2.s2s.CancelTrackedRideRequest) | [.demand.v2.common.Empty](#demand.v2.s2s.CancelTrackedRideRequest) | Cancel a tracked ride by ride tracking ID. validation is done by comparing the request passenger phone to the passenger phone number as retrieved in Create Ride Request Errors: INVALID_ARGUMENT - ride tracking id or passenger phone were not supplied NOT_FOUND - ride not found for the specified ride tracking ID, or ride tracking ID is invalid UNAUTHENTICATED: Validation failed for the given passenger phone number |
| GetOfferTrackingDetails | [GetOfferTrackingDetailsRequest](#demand.v2.s2s.GetOfferTrackingDetailsRequest) | [.demand.v2.common.RideOffer](#demand.v2.s2s.GetOfferTrackingDetailsRequest) | Returns the offer by offer tracking ID Errors: INVALID_ARGUMENT - offer tracking id was not supplied NOT_FOUND - offer not found for the specified offer tracking ID, or offer tracking ID is invalid |

 



## Scalar Value Types

| .proto Type | Notes | C++ Type | Java Type | Python Type |
| ----------- | ----- | -------- | --------- | ----------- |
| <a name="double" /> double |  | double | double | float |
| <a name="float" /> float |  | float | float | float |
| <a name="int32" /> int32 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint32 instead. | int32 | int | int |
| <a name="int64" /> int64 | Uses variable-length encoding. Inefficient for encoding negative numbers – if your field is likely to have negative values, use sint64 instead. | int64 | long | int/long |
| <a name="uint32" /> uint32 | Uses variable-length encoding. | uint32 | int | int/long |
| <a name="uint64" /> uint64 | Uses variable-length encoding. | uint64 | long | int/long |
| <a name="sint32" /> sint32 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int32s. | int32 | int | int |
| <a name="sint64" /> sint64 | Uses variable-length encoding. Signed int value. These more efficiently encode negative numbers than regular int64s. | int64 | long | int/long |
| <a name="fixed32" /> fixed32 | Always four bytes. More efficient than uint32 if values are often greater than 2^28. | uint32 | int | int |
| <a name="fixed64" /> fixed64 | Always eight bytes. More efficient than uint64 if values are often greater than 2^56. | uint64 | long | int/long |
| <a name="sfixed32" /> sfixed32 | Always four bytes. | int32 | int | int |
| <a name="sfixed64" /> sfixed64 | Always eight bytes. | int64 | long | int/long |
| <a name="bool" /> bool |  | bool | boolean | boolean |
| <a name="string" /> string | A string must always contain UTF-8 encoded or 7-bit ASCII text. | string | String | str/unicode |
| <a name="bytes" /> bytes | May contain any arbitrary sequence of bytes. | string | ByteString | str |
