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
    - [GetVerticalsCoverageRequest](#demand.v2.c2s.GetVerticalsCoverageRequest)
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
    - [TransportTypePreference](#demand.v2.common.TransportTypePreference)
    - [Vehicle](#demand.v2.common.Vehicle)
    - [VerticalsCoverageResponse](#demand.v2.common.VerticalsCoverageResponse)

    - [CancellationInfo.CancelReasonCategory](#demand.v2.common.CancellationInfo.CancelReasonCategory)
    - [CancellationInfo.Party](#demand.v2.common.CancellationInfo.Party)
    - [CancellationInfo.Status](#demand.v2.common.CancellationInfo.Status)
    - [CancellationInfo.StatusReason](#demand.v2.common.CancellationInfo.StatusReason)
    - [DemandCancellingParty](#demand.v2.common.DemandCancellingParty)
    - [PassengerCancelReasonCategory](#demand.v2.common.PassengerCancelReasonCategory)
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
    - [Place](#demand.v2.common.Place)
    - [Point](#demand.v2.common.Point)
    - [Price](#demand.v2.common.Price)
    - [PriceEstimate](#demand.v2.common.PriceEstimate)
    - [PriceRange](#demand.v2.common.PriceRange)
    - [TimeRange](#demand.v2.common.TimeRange)

    - [Place.PlaceCategory](#demand.v2.common.Place.PlaceCategory)




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
    - [GetVerticalsCoverageRequest](#demand.v2.s2s.GetVerticalsCoverageRequest)
    - [RideOffersRequest](#demand.v2.s2s.RideOffersRequest)





- [marketplace/public/grpc/demand_handler/v2/gen-doc/demand_s2s_service.proto](#marketplace/public/grpc/demand_handler/v2/gen-doc/demand_s2s_service.proto)



    - [S2SDemandApi](#demand.v2.s2s.S2SDemandApi)


- [marketplace/public/grpc/demand_handler/v2/gen-doc/demand_webhooks_messages.proto](#marketplace/public/grpc/demand_handler/v2/gen-doc/demand_webhooks_messages.proto)
    - [DemandInfo](#demand.v2.webhooks.DemandInfo)
    - [DriverVehicleDetails](#demand.v2.webhooks.DriverVehicleDetails)
    - [ETAUpdate](#demand.v2.webhooks.ETAUpdate)
    - [EventMetadata](#demand.v2.webhooks.EventMetadata)
    - [LocationUpdate](#demand.v2.webhooks.LocationUpdate)
    - [RideUpdate](#demand.v2.webhooks.RideUpdate)
    - [StatusChange](#demand.v2.webhooks.StatusChange)





- [marketplace/public/grpc/demand_handler/v2/gen-doc/demand_webhooks_service.proto](#marketplace/public/grpc/demand_handler/v2/gen-doc/demand_webhooks_service.proto)



    - [DemandWebhooksAPI](#demand.v2.webhooks.DemandWebhooksAPI)


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
| cancel_reason_category | [demand.v2.common.PassengerCancelReasonCategory](#demand.v2.common.PassengerCancelReasonCategory) |  | Optional. The cancellation reason category. |






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
| payment_ticket_id | [string](#string) |  | Optional. Ticket to be used for online payment. |






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






<a name="demand.v2.c2s.GetVerticalsCoverageRequest"/>

### GetVerticalsCoverageRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| point | [demand.v2.common.Point](#demand.v2.common.Point) |  | Mandatory. |
| filter_by_restrictions | [bool](#bool) |  | Optional. Required to filter blacklist/whitelist suppliers. Default - false. |






<a name="demand.v2.c2s.RideOffersRequest"/>

### RideOffersRequest
A request to get ride offers for a given route. If a prebook_pickup_time value is provided, this is a request for a future pickup.
Otherwise, this is a request for an immediate pickup (within 30 minutes).


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| route | [demand.v2.common.Route](#demand.v2.common.Route) |  | Mandatory. The requested route of the ride. |
| constraints | [demand.v2.common.BookingConstraints](#demand.v2.common.BookingConstraints) |  | Optional. Ride constraints such as passenger count, child seats, number of suitcases, etc. |
| prebook_pickup_time_ms | [uint64](#uint64) |  | Optional. For taxi rides, this should be a future pickup time, which is at least 30 minutes after the request time. For public transport rides this can be any pickup time that is not in the past. In all cases, an empty value indicates a request for an immediate ride. |
| price_range | [demand.v2.common.PriceRange](#demand.v2.common.PriceRange) |  | FUTURE FEATURE, CURRENTLY UNSUPPORTED: Optional. A requested price range. If this value is set, only offers whose price is within the range are returned. Otherwise, any price is assumed to be acceptable. |
| sort_type | [demand.v2.common.RideOffer.SortType](#demand.v2.common.RideOffer.SortType) |  | FUTURE FEATURE, CURRENTLY UNSUPPORTED: Optional. How to sort the RideOffers, by price or by ETA. (The Marketplace default sort order is by best price, and then minimal ETA.). |
| passenger_note | [string](#string) |  | Optional. A free text note from the passenger. |
| transit_options | [demand.v2.common.TransitOptions](#demand.v2.common.TransitOptions) |  | Optional. Parameters for transit offers. |
| transport_type_preference | [demand.v2.common.TransportTypePreference](#demand.v2.common.TransportTypePreference) |  | Optional. |
| locale | [string](#string) |  | Optional. Indicates the language of passenger. Will be used to determine language of addresses and SMSs sent to demander. |















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
| GetVerticalsCoverage | [GetVerticalsCoverageRequest](#demand.v2.c2s.GetVerticalsCoverageRequest) | [.demand.v2.common.VerticalsCoverageResponse](#demand.v2.c2s.GetVerticalsCoverageRequest) | Returns the verticals in which the point is covered |





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
| cancel_reason_category | [CancellationInfo.CancelReasonCategory](#demand.v2.common.CancellationInfo.CancelReasonCategory) |  | The cancellation reason cateory. |
| status_reason | [CancellationInfo.StatusReason](#demand.v2.common.CancellationInfo.StatusReason) |  | The reason for the cancellation status (e.g. why it was rejected). |






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
| phone_number | [string](#string) |  | Mandatory. The passenger’s telephone number. |
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
| route | [Route](#demand.v2.common.Route) |  | The ride route as confirmed by the marketplace and the supplier. |
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
| confirmed_pickup_point | [Point](#demand.v2.common.Point) |  | Optional. The ride confirmed pickup point calculated by Here-API. NOTE: This field will be deprecated soon, please use route.pickup.point instead. */ |
| requested_route | [Route](#demand.v2.common.Route) |  | The ride route as the user requested. |






<a name="demand.v2.common.RideLocation"/>

### RideLocation
Provides the real-time location and progress of the vehicle. Updated every ~10 seconds.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| ride_id | [string](#string) |  | The ID of the ride. |
| vehicle_location | [Point](#demand.v2.common.Point) |  | Optional. The current location of the vehicle. |
| estimated_pickup_time_ms | [uint64](#uint64) |  | Optional. The estimated time (in epoch) of pickup, constantly updated until the vehicle is at the pickup location. This field will be deprecated soon, please use estimated_pickup_time_seconds instead. |
| estimated_dropoff_time_ms | [uint64](#uint64) |  | Optional. The estimated time (in epoch) of drop-off, constantly updated until the vehicle is at the drop-off location. This field will be deprecated soon, please use estimated_dropoff_time_seconds instead. |
| last_update_time_ms | [uint64](#uint64) |  | The last time this entity is updated. Used for tracking updates. |
| estimated_pickup_time_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Estimated number of seconds until the driver will pick the passenger up. For example: 60 seconds to pickup |
| estimated_dropoff_time_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Estimated number of seconds until dropoff. For example: 10 minutes until dropoff (10*60 = 600 seconds) |






<a name="demand.v2.common.RideOffer"/>

### RideOffer
An offer for a ride on the given route.


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| offer_id | [string](#string) |  | A unique offer ID. If this offer is chosen, the client sends this ID when calling CreateRide. |
| supplier | [Supplier](#demand.v2.common.Supplier) |  | The supplier details. |
| route | [Route](#demand.v2.common.Route) |  | The ride route as confirmed by the marketplace and the supplier. |
| estimated_pickup_time_ms | [uint64](#uint64) |  | Optional. Pickup time (in epoch) estimate sent by the supplier. NOTE: This field will be deprecated soon, please use estimated_pickup_time_seconds instead. |
| estimated_dropoff_time_ms | [uint64](#uint64) |  | Optional. Drop-off time (in epoch) estimate sent by the supplier. NOTE: This field will be deprecated soon, please use estimated_ride_duration_seconds instead. |
| price_estimation | [PriceEstimate](#demand.v2.common.PriceEstimate) |  | Optional. A price estimate for the ride. |
| offer_expiration_time_ms | [uint64](#uint64) |  | The offer expiration time (in milliseconds from the time the offer is sent). |
| cancellation_policy | [RideOffer.CancellationPolicy](#demand.v2.common.RideOffer.CancellationPolicy) |  | The cancellation policy of the supplier (cancellation allowed or not allowed). |
| duration_ms | [uint64](#uint64) |  | Duration of the route in milliseconds. NOTE: this field will be deprecated soon. Please use duration_seconds instead. |
| transfers | [uint32](#uint32) |  | Number of transport changes to reach the destination. |
| legs | [PublicTransportRouteLeg](#demand.v2.common.PublicTransportRouteLeg) | repeated | A list of transportation legs for the route, if this offer is a public transportation offer. |
| transit_type | [RideOffer.TransitType](#demand.v2.common.RideOffer.TransitType) |  | Specifies the transit type of this offer. |
| estimated_pickup_time_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Optional. Estimated number of seconds until the driver will pick the passenger up. For example: 60 seconds to pickup |
| estimated_ride_duration_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Optional. Estimated number of seconds between pickup and dropoff. NOTE: It does not include the time until pickup. |
| duration_seconds | [uint64](#uint64) |  | Duration of the route in seconds. NOTE: this field will be deprecated soon. Please use estimated_ride_duration_seconds instead. |
| requested_route | [Route](#demand.v2.common.Route) |  | The ride route as the user requested. |






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
| locale | [string](#string) |  | Optional. Indicates the language of passenger. Will be used to determine language of addresses and SMSs sent to demander. |






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
| supplier_notes | [string](#string) | repeated | The supplier&#39;s notes. |






<a name="demand.v2.common.TransitOptions"/>

### TransitOptions



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| max_transfers | [google.protobuf.Int32Value](#google.protobuf.Int32Value) |  | Optional. Maximum number of changes or transfers allowed in a route. Default is unlimited. Range is 0-6. |
| max_walking_distance_meters | [google.protobuf.Int32Value](#google.protobuf.Int32Value) |  | Optional. Specifies a maximum walking distance in meters. Default is 2000. Range is 0-6000. |
| locale | [google.protobuf.StringValue](#google.protobuf.StringValue) |  | Optional. The client&#39;s locale. Complies with the ISO 639-1 standard and defaults to en. |






<a name="demand.v2.common.TransportTypePreference"/>

### TransportTypePreference



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| use_taxi | [google.protobuf.BoolValue](#google.protobuf.BoolValue) |  |  |
| use_public_transport | [google.protobuf.BoolValue](#google.protobuf.BoolValue) |  |  |






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






<a name="demand.v2.common.VerticalsCoverageResponse"/>

### VerticalsCoverageResponse



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| verticals | [RideOffer.TransitType](#demand.v2.common.RideOffer.TransitType) | repeated |  |








<a name="demand.v2.common.CancellationInfo.CancelReasonCategory"/>

### CancellationInfo.CancelReasonCategory


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN_CANCEL_REASON_CATEGORY | 0 | Unknown cancellation category. |
| DRIVER_NO_SHOW | 1 | Passenger cancellation category. |
| PRICE_CHANGED | 2 | Passenger cancellation category. |
| ETA_CHANGED | 3 | Passenger cancellation category. |
| UNSUITABLE_VEHICLE | 4 | Passenger cancellation category. |
| DRIVER_BEHAVED_INAPPROPRIATELY | 5 | Passenger cancellation category. |
| CHANGED_MY_PLANS | 6 | Passenger cancellation category. |
| DRIVERS_UNAVAILABLE | 7 | Supplier cancellation category. |
| PASSENGER_NO_SHOW | 8 | Supplier cancellation category. |
| PASSENGER_REQUESTED_TO_CANCEL | 9 | Supplier cancellation category. |
| VEHICLE_MALFUNCTION | 10 | Supplier cancellation category. |
| HEAVY_TRAFFIC | 11 | Supplier cancellation category. |
| OTHER_CANCEL_REASON_CATEGORY | 100 | Supplier or passenger cancellation category. |



<a name="demand.v2.common.CancellationInfo.Party"/>

### CancellationInfo.Party


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 0 | The cancelling party is unknown. |
| DEMANDER | 1 | The demander cancelled the ride (e.g. concierge). |
| SUPPLIER | 2 | The supplier cancelled the ride. |
| PASSENGER | 3 | The passenger cancelled the ride. |
| MARKETPLACE | 4 | MP cancelled the ride. |



<a name="demand.v2.common.CancellationInfo.Status"/>

### CancellationInfo.Status


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN_STATUS | 0 | The cancellation status is unknown. |
| PROCESSING | 1 | The cancellation request is being processed. |
| ACCEPTED | 2 | The cancellation request is accepted. |
| REJECTED | 3 | The cancellation request is rejected. |



<a name="demand.v2.common.CancellationInfo.StatusReason"/>

### CancellationInfo.StatusReason


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN_STATUS_REASON | 0 | The cancellation status reason is unknown. |
| COULD_NOT_CONTACT_SUPPLIER | 1 | The marketplace could not contact the supplier. |
| SUPPLIER_REJECTED_CANCELLATION | 2 | The supplier rejected the cancellation request. |
| SUPPLIER_DOES_NOT_SUPPORT_CANCELLATION | 3 | The supplier does not support cancellations. |
| RIDE_STATUS_INVALID_FOR_CANCELLATION | 4 | The ride is in a status in which it cannot be canceled |



<a name="demand.v2.common.DemandCancellingParty"/>

### DemandCancellingParty
Party responsible for cancelling the ride

| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 0 | The cancelling party is unknown. |
| DEMANDER | 1 | The demander cancelled the ride (e.g. concierge). |
| PASSENGER | 2 | The passenger cancelled the ride. |



<a name="demand.v2.common.PassengerCancelReasonCategory"/>

### PassengerCancelReasonCategory
Passenger cancellation reason category

| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN_PASSENGER_CANCEL_REASON_CATEGORY | 0 | Unknown cancellation category. |
| DRIVER_NO_SHOW | 1 | Driver did not show up. |
| PRICE_CHANGED | 2 | Ride price changed. |
| ETA_CHANGED | 3 | Ride ETA changed. |
| UNSUITABLE_VEHICLE | 4 | Ride vehicle is not suitable. |
| DRIVER_BEHAVED_INAPPROPRIATELY | 5 | Driver behaved inappropriately. |
| CHANGED_MY_PLANS | 6 | Passenger changed plans. |
| OTHER_PASSENGER_CANCEL_REASON_CATEGORY | 100 | Other. |



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
| free_text | [string](#string) |  | Optional. Street address in a free text format. |
| place | [Place](#demand.v2.common.Place) |  | Optional. Place information of the location. |






<a name="demand.v2.common.Place"/>

### Place



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| name | [string](#string) |  | The place name. |
| category | [Place.PlaceCategory](#demand.v2.common.Place.PlaceCategory) |  | The place category (e.g.: Airport, Restaurant, Park, etc.). |






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








<a name="demand.v2.common.Place.PlaceCategory"/>

### Place.PlaceCategory


| Name | Number | Description |
| ---- | ------ | ----------- |
| UNKNOWN | 0 |  |
| RESTAURANT | 1000 | An establishment that prepares and serves refreshments and prepared meals. |
| COFFEE_TEA | 1100 | An establishment that sells drinks, such as coffee and tea, as well as refreshments. |
| NIGHTLIFE | 2000 | An establishment that provides evening entertainment and usually serves alcoholic beverages. |
| CINEMA | 2100 | An establishment that shows movies through screen projection. |
| CULTURE | 2200 | An establishment where various types of performing arts are presented. |
| GAMBLING_LOTTERY | 2300 | An establishment that provides gambling entertainment. |
| ATTRACTION | 3000 | A designated area of special interest to tourists. |
| MUSEUM | 3100 | An establishment dedicated to the preservation and exhibition of artistic, historical, or scientific artifacts. |
| RELIGIOUS_PLACE | 3200 | An establishment of special religious significance or where religious services are held. |
| WATER | 3500 | A natural and geographical feature of the earth&#39;s surface that is covered with water, such as a lake, river, stream or ocean. |
| MOUNTAIN | 3510 | A natural and geographical feature that is higher than the surrounding land. |
| UNDERSEA | 3520 | Undersea attractions |
| FOREST | 3522 | A forest, heath or other vegetation |
| GEOGRAPHICAL | 3550 | Natural and geographical locations |
| AIRPORT | 4000 | A designated area that serves various aspects of aviation related sports, including gliders, recreational aircraft and model airplanes. |
| PUBLIC_TRANSPORTATION | 4100 | A facility for travelers who are travelling between stops on public transport. |
| CARGO_TRANSPORTATION | 4200 | A facility that handles some aspect of the transportation of cargo freight. |
| REST_AREA | 4300 | An establishment along a motorway (controlled access road) that provides restrooms and parking. |
| HOTEL | 5000 | A business that provides lodging or temporary living quarters. |
| LODGE | 5100 | A business that provides lodging to the public generally without room service. |
| OUTDOORS | 5510 | Public land preserved and maintained for recreational use. |
| LEISURE | 5520 | A park that contains rides and/or other entertainment which may be based on a central theme. |
| CONVENIENCE_STORE | 6000 | An establishment that sells groceries, candy, toiletries, soft drinks, tobacco products, newspapers and other products. |
| SHOPPING_CENTER | 6100 | A complex of businesses that are co-located and share common services. |
| DEPARTMENT_STORE | 6200 | A business that sells a wide variety of merchandise that is organized by product or service departments. |
| FOOD_AND_DRINKS | 6300 | A business that sells specialty products of a particular type of food or beverage. |
| PHARMACY | 6400 | A business that sells medications, toiletry items and other retail cosmetics. |
| ELECTRONICS | 6500 | A business that sells consumer electronics and electronic entertainment equipment. |
| HARDWARE_HOUSE_GARDEN | 6600 | A business that sells crafts, gardening, remodeling, or decorating items for the home. |
| BOOKSTORE | 6700 | A business that sells books, magazines and other reading material. |
| CLOTHING_AND_ACCESSORIES | 6800 | A business that sells apparel items, garments or fashion accessories for men, women, and children. |
| STORE | 6900 | A business that sells a variety of products targeted to consumers. |
| HAIR_BEAUTY | 6950 | A business that provides hair styling and personal appearance services. Places in this category may also sell hair products and other related cosmetic items. |
| BANKING | 7000 | Businesses that specialize in the maintenance, lending, exchange, or issuance of money. |
| ATM | 7010 | A computer terminal that allows bank customers to deposit, withdraw, or transfer funds without the assistance of a bank teller. |
| MONEY_SERVICES | 7050 | Businesses that provide money related services. |
| MEDIA | 7100 | Businesses that provide communication services. |
| COMMERCIAL_SERVICES | 7201 | Businesses that provide a service or product for use by other businesses. |
| BUSINESS_INDUSTRY | 7250 | Businesses that employ people in and around the city in which it is located. |
| EMERGANCY_SERVICES | 7300 | Municipal emergency services |
| CONSUMER_SERVICES | 7400 | An organization that provides consumer services for a variety of products for used by the public. |
| POST_OFFICE | 7450 | An office or station that receives, sorts, dispatches and delivers mail to a specific area or region. |
| TOOURIST_INFORMATION | 7460 | Businesses that provide a variety of information for visiting tourists, such as event schedules, lodging/accommodations, restaurants, attractions and more |
| FEUL_STATION | 7600 | Businesses that sell fuel for vehicles |
| CAR_DEALER | 7800 | Businesses that sell new automobiles and motorcycles. |
| CAR_REPAIR | 7850 | Businesses that provide automotive repair services. |
| CAR_RENTAL | 7851 | Businesses that rent or lease automobiles. |
| TRUCK_SERVICES | 7900 | Business that sell or service trucks and tractor trailers. |
| HEALTH_CARE | 8000 | Facilities that include dental offices, hospitals, nursing homes and other health care-related services. |
| GOVERNMENT | 8100 | A Place where government services are provided. |
| EDUCATION | 8200 | Facilities that are used for educational purposes including primary schooling, secondary schooling, universities and more. |
| LIBRARY | 8300 | Facilities that offer books, periodicals, audio, video and other material for public use. |
| EVENTS | 8400 | An area or facility used for the hosting of fairs and conventions. |
| PARKING | 8500 | Area or building used for parking cars |
| SPORTS | 8600 | A facility used for individual and team sports including recreational sports. |
| FACILITIES | 8700 | Facilities with miscellaneous uses such as Clubhouses, Offices, and Registration Offices. |
| CITY | 9100 | Represents a named settlement that may be a (large) city, town, or tiny village |
| OUTDOORS_COMPLEX | 9200 | Outdoor areas or complexes with designations for specific businesses or interests. |
| BUILDING | 9300 | Areas and buildings designated for residential or office use |
| ADMINISTRATIVE_REGION | 9400 | An administrative region, such as a postal area, or a named street/square/intersection. |










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
| cancel_reason_category | [demand.v2.common.PassengerCancelReasonCategory](#demand.v2.common.PassengerCancelReasonCategory) |  | Optional. The category of the cancellation. |
| cancelling_party | [demand.v2.common.DemandCancellingParty](#demand.v2.common.DemandCancellingParty) |  | Optional. The party cancelling the ride - demander or passenger. Default is passenger. |






<a name="demand.v2.s2s.CancelTrackedRideRequest"/>

### CancelTrackedRideRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| ride_tracking_id | [string](#string) |  | Mandatory. The ID from the ride tracker url. |
| passenger_phone | [string](#string) |  | Mandatory. the passenger phone for validation purposes. |
| cancel_reason | [string](#string) |  | Optional. Free text. The reason for the cancellation. |
| cancel_reason_category | [demand.v2.common.PassengerCancelReasonCategory](#demand.v2.common.PassengerCancelReasonCategory) |  | Optional. The category of the cancellation. |






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
| payment_ticket_id | [string](#string) |  | Optional. Ticket to be used for online payment. |






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






<a name="demand.v2.s2s.GetVerticalsCoverageRequest"/>

### GetVerticalsCoverageRequest



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| point | [demand.v2.common.Point](#demand.v2.common.Point) |  | Mandatory. |
| filter_by_restrictions | [bool](#bool) |  | Optional. Required to filter blacklist/whitelist suppliers. Default - false. |






<a name="demand.v2.s2s.RideOffersRequest"/>

### RideOffersRequest
A request to get ride offers for a given route. If a prebook_pickup_time value is provided, this is a request for a future pickup.
Otherwise, this is a request for an immediate pickup (within 30 minutes).


| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| user_id | [string](#string) |  | Mandatory. The ID of the user requesting the ride. |
| route | [demand.v2.common.Route](#demand.v2.common.Route) |  | Mandatory. The requested route of the ride. |
| constraints | [demand.v2.common.BookingConstraints](#demand.v2.common.BookingConstraints) |  | Optional. Ride constraints such as passenger count, child seats, number of suitcases, etc. |
| prebook_pickup_time_ms | [uint64](#uint64) |  | Optional. For taxi rides, this should be a future pickup time, which is at least 30 minutes after the request time. For public transport rides this can be any pickup time that is not in the past. In all cases, an empty value indicates a request for an immediate ride. |
| price_range | [demand.v2.common.PriceRange](#demand.v2.common.PriceRange) |  | FUTURE FEATURE, CURRENTLY UNSUPPORTED: Optional. A requested price range. If this value is set, only offers whose price is within the range are returned. Otherwise, any price is assumed to be acceptable. |
| sort_type | [demand.v2.common.RideOffer.SortType](#demand.v2.common.RideOffer.SortType) |  | FUTURE FEATURE, CURRENTLY UNSUPPORTED: Optional. How to sort the RideOffers, by price or by ETA. (The Marketplace default sort order is by best price, and then minimal ETA.). |
| passenger_note | [string](#string) |  | Optional. A free text note from the passenger. |
| transit_options | [demand.v2.common.TransitOptions](#demand.v2.common.TransitOptions) |  | Optional. Parameters for transit options. |
| transport_type_preference | [demand.v2.common.TransportTypePreference](#demand.v2.common.TransportTypePreference) |  | Optional. |
| locale | [string](#string) |  | Optional. Indicates the language of passenger. Will be used to determine language of addresses and SMSs sent to passenger. |















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
| GetVerticalsCoverage | [GetVerticalsCoverageRequest](#demand.v2.s2s.GetVerticalsCoverageRequest) | [.demand.v2.common.VerticalsCoverageResponse](#demand.v2.s2s.GetVerticalsCoverageRequest) | Returns the verticals in which the point is covered |





<a name="marketplace/public/grpc/demand_handler/v2/gen-doc/demand_webhooks_messages.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/demand_handler/v2/gen-doc/demand_webhooks_messages.proto



<a name="demand.v2.webhooks.DemandInfo"/>

### DemandInfo



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| demander_id | [string](#string) |  |  |
| user_id | [string](#string) |  |  |
| app_id | [string](#string) |  |  |






<a name="demand.v2.webhooks.DriverVehicleDetails"/>

### DriverVehicleDetails



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| driver_details | [demand.v2.common.DriverDetails](#demand.v2.common.DriverDetails) |  |  |
| vehicle | [demand.v2.common.Vehicle](#demand.v2.common.Vehicle) |  |  |






<a name="demand.v2.webhooks.ETAUpdate"/>

### ETAUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| event_metadata | [EventMetadata](#demand.v2.webhooks.EventMetadata) |  | mandatory. |
| estimated_pickup_time_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Estimated number of seconds until the driver will pick the passenger up. For example: 60 seconds to pickup |
| estimated_dropoff_time_seconds | [google.protobuf.UInt32Value](#google.protobuf.UInt32Value) |  | Estimated number of seconds until dropoff. For example: 10 minutes until dropoff (10*60 = 600 seconds) |






<a name="demand.v2.webhooks.EventMetadata"/>

### EventMetadata



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| event_time | [google.protobuf.Timestamp](#google.protobuf.Timestamp) |  | mandatory. The time the event took place. |
| event_id | [string](#string) |  | mandatory. Unique ID of event, so in case of duplication you can omit by event id. |
| demand_info | [DemandInfo](#demand.v2.webhooks.DemandInfo) |  | mandatory. |
| ride_id | [string](#string) |  | mandatory. |






<a name="demand.v2.webhooks.LocationUpdate"/>

### LocationUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| event_metadata | [EventMetadata](#demand.v2.webhooks.EventMetadata) |  | mandatory. |
| point | [demand.v2.common.Point](#demand.v2.common.Point) |  | mandatory, current location of the vehicle. |






<a name="demand.v2.webhooks.RideUpdate"/>

### RideUpdate



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| event_metadata | [EventMetadata](#demand.v2.webhooks.EventMetadata) |  | mandatory. |
| status_change | [StatusChange](#demand.v2.webhooks.StatusChange) |  | In case the ride status changes, the status update will be published via webhook. |
| driver_vehicle_details | [DriverVehicleDetails](#demand.v2.webhooks.DriverVehicleDetails) |  | In case the supplier sent driver details and/or vehicle details, it will be published via webhook. |
| cancellation_info | [demand.v2.common.CancellationInfo](#demand.v2.common.CancellationInfo) |  | In case of cancellation request from demande/supply side, we will keep the demander updated regarding the cancellation status, reason etc. |
| rejection_reason | [google.protobuf.StringValue](#google.protobuf.StringValue) |  | In case of ride rejection, we will keep the demander updated regarding rejection reason. |
| price | [demand.v2.common.Price](#demand.v2.common.Price) |  | In case ride&#39;s final price is set, the final price will be published via webhook. |






<a name="demand.v2.webhooks.StatusChange"/>

### StatusChange



| Field | Type | Label | Description |
| ----- | ---- | ----- | ----------- |
| status | [demand.v2.common.RideStatusUpdate.Status](#demand.v2.common.RideStatusUpdate.Status) |  |  |















<a name="marketplace/public/grpc/demand_handler/v2/gen-doc/demand_webhooks_service.proto"/>
<p align="right"><a href="#top">Top</a></p>

## marketplace/public/grpc/demand_handler/v2/gen-doc/demand_webhooks_service.proto
The server to service API








<a name="demand.v2.webhooks.DemandWebhooksAPI"/>

### DemandWebhooksAPI


| Method Name | Request Type | Response Type | Description |
| ----------- | ------------ | ------------- | ------------|
| HandleRideUpdate | [RideUpdate](#demand.v2.webhooks.RideUpdate) | [.demand.v2.common.Empty](#demand.v2.webhooks.RideUpdate) | Handle ride update |
| HandleETAUpdate | [ETAUpdate](#demand.v2.webhooks.ETAUpdate) | [.demand.v2.common.Empty](#demand.v2.webhooks.ETAUpdate) | Handle ETA update |
| HandleLocationUpdate | [LocationUpdate](#demand.v2.webhooks.LocationUpdate) | [.demand.v2.common.Empty](#demand.v2.webhooks.LocationUpdate) | Handle location update |

 



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

