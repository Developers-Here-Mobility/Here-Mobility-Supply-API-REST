marketplace/public/grpc/supply_handler/v1/supply_handler_rides_service.proto-REST
=================================================================================
**Version:** version not set

### /dispatch.rides.v1/offer_requests
---
##### ***POST***
**Summary:** Request ride offers from the supplier

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1GetSimpleRideOffersRequest](#v1getsimplerideoffersrequest) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1SimpleRideOffers](#v1simplerideoffers) |

### /dispatch.rides.v1/rides
---
##### ***POST***
**Summary:** Create a ride with the supplier

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [v1CreateSimpleRideRequest](#v1createsimpleriderequest) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1CreateSimpleRideResponse](#v1createsimplerideresponse) |

### /dispatch.rides.v1/rides/{ride_id}/demander_cancel
---
##### ***POST***
**Summary:** Update the supplier that the demander has cancelled the ride.

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1DemanderCancelRideRequest](#v1demandercancelriderequest) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1DemanderCancelRideResponse](#v1demandercancelrideresponse) |

### /dispatch.rides.v1/rides/{ride_id}/status
---
##### ***GET***
**Summary:** Request the latest status of the ride from the supplier

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| supplier_id | query | Mandatory. Marketplace generated supplier ID. | No | string |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1SupplierRideStatus](#v1supplierridestatus) |

### /supply.rides.v1/rides/{ride_id}/eta_update
---
##### ***POST***
**Summary:** Update the marketplace that estimated time to arrival to the origin and and to destination has changed
Recommended to update only when there is a major change (1 minute at least)

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1RideEtaUpdate](#v1rideetaupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1Empty](#v1empty) |

### /supply.rides.v1/rides/{ride_id}/location_update
---
##### ***POST***
**Summary:** Update the marketplace that the vehicle location has changed

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1RideLocationUpdate](#v1ridelocationupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1Empty](#v1empty) |

### /supply.rides.v1/rides/{ride_id}/pickup_and_destination_update
---
##### ***POST***
**Summary:** Update the marketplace that the meeting pickup and destination points changed

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1RidePickupAndDestinationUpdate](#v1ridepickupanddestinationupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1Empty](#v1empty) |

### /supply.rides.v1/rides/{ride_id}/price_update
---
##### ***POST***
**Summary:** Update the marketplace that the ride price has changed

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1RidePriceUpdate](#v1ridepriceupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1Empty](#v1empty) |

### /supply.rides.v1/rides/{ride_id}/requested_pickup_time_update
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1RideRequestedPickupTimeUpdate](#v1riderequestedpickuptimeupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1Empty](#v1empty) |

### /supply.rides.v1/rides/{ride_id}/status_update
---
##### ***POST***
**Summary:** Update the marketplace that the ride status changed

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1SupplierRideStatusUpdate](#v1supplierridestatusupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1Empty](#v1empty) |

### /supply.rides.v1/rides/{ride_id}/supplier_cancel
---
##### ***POST***
**Summary:** Update the marketplace that the assigned supplier has cancelled the ride

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1SupplierCancelRideRequest](#v1suppliercancelriderequest) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1Empty](#v1empty) |

### /supply.rides.v1/rides/{ride_id}/vehicle_and_driver_update
---
##### ***POST***
**Summary:** Update the marketplace that the assigned vehicle and driver have changed

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [v1RideVehicleAndDriverUpdate](#v1ridevehicleanddriverupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [v1Empty](#v1empty) |

### Models
---

### DemanderCancelRideRequestPassengerCancelReasonCategory

- UNKNOWN_PASSENGER_CANCEL_REASON_CATEGORY: Unknown cancellation category.
 - DRIVER_NO_SHOW: Driver did not show up.
 - PRICE_CHANGED: Ride price changed.
 - ETA_CHANGED: Ride ETA changed.
 - UNSUITABLE_VEHICLE: Ride vehicle is not suitable.
 - DRIVER_BEHAVED_INAPPROPRIATELY: Driver behaved inappropriately.
 - CHANGED_MY_PLANS: Passenger changed plans.
 - OTHER_PASSENGER_CANCEL_REASON_CATEGORY: Other.

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| DemanderCancelRideRequestPassengerCancelReasonCategory | string | - UNKNOWN_PASSENGER_CANCEL_REASON_CATEGORY: Unknown cancellation category.
 - DRIVER_NO_SHOW: Driver did not show up.
 - PRICE_CHANGED: Ride price changed.
 - ETA_CHANGED: Ride ETA changed.
 - UNSUITABLE_VEHICLE: Ride vehicle is not suitable.
 - DRIVER_BEHAVED_INAPPROPRIATELY: Driver behaved inappropriately.
 - CHANGED_MY_PLANS: Passenger changed plans.
 - OTHER_PASSENGER_CANCEL_REASON_CATEGORY: Other. |  |

### SupplierCancelRideRequestSupplierCancelReasonCategory

- UNKNOWN_SUPPLIER_CANCEL_REASON_CATEGORY: Unknown cancellation category.
 - DRIVERS_UNAVAILABLE: No available drivers for ride.
 - PASSENGER_NO_SHOW: Passenger did not show up for the ride.
 - PASSENGER_REQUESTED_TO_CANCEL: Passenger requested to cancel the ride.
 - VEHICLE_MALFUNCTION: Vehicle malfunction.
 - HEAVY_TRAFFIC: Heavy traffic.
 - OTHER_SUPPLIER_CANCEL_REASON_CATEGORY: Other cancellation category.

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| SupplierCancelRideRequestSupplierCancelReasonCategory | string | - UNKNOWN_SUPPLIER_CANCEL_REASON_CATEGORY: Unknown cancellation category.
 - DRIVERS_UNAVAILABLE: No available drivers for ride.
 - PASSENGER_NO_SHOW: Passenger did not show up for the ride.
 - PASSENGER_REQUESTED_TO_CANCEL: Passenger requested to cancel the ride.
 - VEHICLE_MALFUNCTION: Vehicle malfunction.
 - HEAVY_TRAFFIC: Heavy traffic.
 - OTHER_SUPPLIER_CANCEL_REASON_CATEGORY: Other cancellation category. |  |

### VehicleVehicleType

 - UNKNOWN: Default value - unknown vehicle type.
 - STANDARD: Standard vehicle.
 - LIMO: Limousine.
 - VAN: Van.
 - OTHER: Other known type - not specified.

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| VehicleVehicleType | string |  - UNKNOWN: Default value - unknown vehicle type.
 - STANDARD: Standard vehicle.
 - LIMO: Limousine.
 - VAN: Van.
 - OTHER: Other known type - not specified. |  |

### commonv1Location

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| point | [v1Point](#v1point) | Mandatory. Geographic coordinates (latitude, longtitude). | No |
| address | [v1Address](#v1address) | Optional. | No |
| place | [v1Place](#v1place) | Optional. Place information of the location. | No |
| free_text | string | Optional. Street address in a free text format. | No |

### protobufUInt32Value

Wrapper message for `uint32`.

The JSON representation for `UInt32Value` is JSON number.

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| value | long | The uint32 value. | No |

### v1Address

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| country | string | Optional. Localized country name. | No |
| country_code | string | Optional. ISO 3166-alpha-3 country code. | No |
| state | string | Optional. State (first subdivision level below the country, if relevant). | No |
| county | string | Optional. County (second subdivision level below the country, if relevant). | No |
| city | string | Optional. City/town. | No |
| district | string | Optional. District (subdivision level below the city). | No |
| sub_district | string | Optional. Sub-district (subdivision level below the district; e.g. commonly used in IND). | No |
| street | string | Optional. Street name. | No |
| house_number | string | Optional. House number; depending on regional characteristics, can also be house name. | No |
| postal_code | string | Optional. Postal code (zipcode). | No |
| building_name | string | Optional. Building name; e.g. commonly used in HKG. | No |
| line | [ string ] | Optional. Formatted address lines. | No |

### v1CreateSimpleRideRequest

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Mandatory. Marketplace ID of the supplier for which we want to create the ride. | No |
| ride_id | string | Mandatory. Marketplace generated ride ID which will be used to identify this ride. | No |
| ride_details | [v1SimpleRideDetails](#v1simpleridedetails) | Mandatory. Details of the ride creation request. | No |

### v1CreateSimpleRideResponse

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| accepted_and_looking_for_driver | boolean (boolean) | Mandatory. Return true if ride was accepted and supplier is looking for a driver, or false if the ride is rejected. This call should return quickly and not wait for human confirmation. | No |
| pickup_eta | [v1UnixTime](#v1unixtime) | Optional. Not yet supported. Estimated time of arrival to pickup. | No |
| booking_estimated_price | [v1Price](#v1price) | Optional. Not yet supported. Estimated price. | No |

### v1DemanderCancelRideRequest

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Mandatory. Marketplace generated supplier ID. | No |
| ride_id | string | Mandatory. Marketplace generated ride ID. | No |
| cancel_reason | string | Optional. Cancellation reason. | No |
| cancel_reason_category | [DemanderCancelRideRequestPassengerCancelReasonCategory](#demandercancelriderequestpassengercancelreasoncategory) | Optional. Cancellation reason category. | No |

### v1DemanderCancelRideResponse

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| cancel_accepted | boolean (boolean) | Mandatory. True if cancellation went through, false it if ride cannot be cancelled. TBD: cancel and pay fee. | No |
| cancel_reason | string | Optional. In case cancellation failed, a textual reason explaining the cause. | No |

### v1DriverDetails

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| driver_id | string | Mandatory. Unique ID of the driver in the dispatcher system. | No |
| name | string | Mandatory. Full name of the driver, in English. | No |
| phone | string | Mandatory. Phone number through which the driver is reachable. | No |
| picture_url | string | Optional. URL of the driver's photo. | No |
| driving_license_id | string | Mandatory in some jurisdictions. License ID of the driver. | No |

### v1Empty

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1Empty | object |  |  |

### v1GetSimpleRideOffersRequest

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| request_id | string | Mandatory. Unique request ID generated by the marketplace. | No |
| supplier_id | string | Mandatory. Marketplace ID of the supplier from which we want to recieve offers. | No |
| pickup | [commonv1Location](#commonv1location) | Mandatory. Origin of the ride (pickup location). | No |
| destination | [commonv1Location](#commonv1location) | Mandatory. Destination of the ride (dropoff location). | No |
| constraints | [v1SimpleRideBookingConstraints](#v1simpleridebookingconstraints) | Mandatry. Constraints representing the requested ride parameters. | No |
| pickup_time | [v1UnixTime](#v1unixtime) | Mandatory. Pickup time. | No |
| passenger_note | string | Optional. Free-text comments by the passenger. | No |

### v1PassengerDetails

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string | Mandatory. Full name of the passenger. | No |
| phone_number | string | Mandatory. Phone number in full international format. | No |
| photo_url | string | Optional. URL. | No |

### v1PaymentFlow

- OFFLINE_PAYMENT: Offline payment flow is used.
 - ONLINE_PAYMENT: Online payment flow is used.

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1PaymentFlow | string | - OFFLINE_PAYMENT: Offline payment flow is used.
 - ONLINE_PAYMENT: Online payment flow is used. |  |

### v1Place

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string | Optional. The place's name. | No |
| category | string | Optional. The place's category (e.g.: Airport, Restaurant, Park, etc.). | No |

### v1Point

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| lat | double | Mandatory. Latitude. | No |
| lng | double | Mandatory. Longtitude. | No |

### v1Price

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| fixed | string (uint64) | Optional. Amount in cents. Fixed price means a price which the supplier commits to in advance. | No |
| lower_bound | string (uint64) | Optional. Amount in cents. Lower bound of an estimated price. | No |
| upper_bound | string (uint64) | Optional. Amount in cents. Upper bound of an estimated price. | No |
| currency | string | Optional. ISO 4217 code. | No |

### v1RideEtaUpdate

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Mandatory. Marketplace generated supplier ID. | No |
| ride_id | string | Mandatory. Marketplace generated ride ID. | No |
| eta_to_pickup_seconds | [protobufUInt32Value](#protobufuint32value) | Optional. Estimated number of seconds until pickup.
For example: 60 seconds until the driver will pick you up
NOTE: At least one of eta_to_pickup_seconds, eta_to_destination_seconds, eta_to_pickup and eta_to_destination
is mandatory. | No |
| eta_to_destination_seconds | [protobufUInt32Value](#protobufuint32value) | Optional. Estimated number of seconds until dropoff.
For example: 20 minutes left until dropoff (20*60 = 1200 seconds)
NOTE: At least one of eta_to_pickup_seconds, eta_to_destination_seconds, eta_to_pickup and eta_to_destination
is mandatory. | No |
| update_id | string | Mandatory. Dispatcher-generated ID which uniquely identifies this update. | No |
| update_ts | dateTime | Mandatory. Dispatcher-generated timestamp which identifies the update time. | No |

### v1RideLocationUpdate

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Mandatory. Marketplace generated supplier ID. | No |
| ride_id | string | Mandatory. Marketplace generated ride ID. | No |
| current_location | [v1Point](#v1point) | Mandatory. Updated location of the vehicle. | No |
| update_id | string | Mandatory. Dispatcher-generated ID which uniquely identifies this update. | No |
| update_ts | dateTime | Mandatory. Dispatcher-generated timestamp which identifies the update time. | No |

### v1RidePickupAndDestinationUpdate

Not yet supported.

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Mandatory. Marketplace generated supplier ID. | No |
| ride_id | string | Mandatory. Marketplace generated ride ID. | No |
| pickup | [commonv1Location](#commonv1location) | Optional. Updated pickup location.
NOTE: At least one of pickup, destination, eta_to_pickup and eta_to_destination is mandatory. | No |
| destination | [commonv1Location](#commonv1location) | Optional. Updated destination location.
NOTE: At least one of pickup, destination, eta_to_pickup and eta_to_destination is mandatory. | No |
| eta_to_pickup_seconds | [protobufUInt32Value](#protobufuint32value) |  | No |
| eta_to_destination_seconds | [protobufUInt32Value](#protobufuint32value) |  | No |
| update_id | string | Mandatory. Dispatcher-generated ID which uniquely identifies this update. | No |
| update_ts | dateTime | Mandatory. Dispatcher-generated timestamp which identifies the update time. | No |

### v1RidePriceUpdate

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Mandatory. Marketplace generated supplier ID. | No |
| ride_id | string | Mandatory. Marketplace generated ride ID. | No |
| booking_estimated_price | [v1Price](#v1price) | Optional. Not yet supported. Updated ride estimated price. Currently not implemented. | No |
| actual_price | [v1Price](#v1price) | Mandatory. Updated ride actual price. | No |
| is_final_price | boolean (boolean) |  | No |
| update_id | string | Mandatory. Dispatcher-generated ID which uniquely identifies this update. | No |
| update_ts | dateTime | Mandatory. Dispatcher-generated timestamp which identifies the update time. | No |

### v1RideRequestedPickupTimeUpdate

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Mandatory. Marketplace generated supplier ID. | No |
| ride_id | string | Mandatory. Marketplace generated ride ID. | No |
| prebook_pickup_time | [v1UnixTime](#v1unixtime) | Mandatory. New requested pickup time form the supplier. | No |
| update_id | string | Mandatory. Dispatcher-generated ID which uniquely identifies this update. | No |
| update_ts | dateTime | Mandatory. Dispatcher-generated timestamp which identifies the update time. | No |

### v1RideVehicleAndDriverUpdate

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Mandatory. Marketplace generated supplier ID. | No |
| ride_id | string | Mandatory. Marketplace generated ride ID. | No |
| vehicle | [v1Vehicle](#v1vehicle) | Optional. Updated vehicle details.
NOTE: At least one of vehicle or driver is mandatory. | No |
| driver | [v1DriverDetails](#v1driverdetails) | Optional. Updated driver details.
NOTE: At least one of vehicle or driver is mandatory. | No |
| update_id | string | Mandatory. Dispatcher-generated ID which uniquely identifies this update. | No |
| update_ts | dateTime | Mandatory. Dispatcher-generated timestamp which identifies the update time. | No |

### v1SimpleRideBookingConstraints

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| passengers_no | long | Mandatory. Number of passengers. | No |
| suitcases_no | long | Mandatory. Number of suitcases. | No |

### v1SimpleRideDetails

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| pickup | [commonv1Location](#commonv1location) | Mandatory. Origin of the ride. | No |
| destination | [commonv1Location](#commonv1location) | Mandatory. Destination of the ride. | No |
| constraints | [v1SimpleRideBookingConstraints](#v1simpleridebookingconstraints) | Mandatory. Constraints representing the requested ride parameters. | No |
| passenger_details | [v1PassengerDetails](#v1passengerdetails) | Mandatory. Details of the passenger. | No |
| pickup_time | [v1UnixTime](#v1unixtime) | Optional. Ride pickup time recieved in the supplier offer. | No |
| passenger_note | string | Optional. Free-text comments by the passenger. | No |
| dispatcher_offer_id | string | Mandatory. Supplier generated unique offer ID. See SimpleRideOffer. | No |
| payment_flow | [v1PaymentFlow](#v1paymentflow) | Optional. The ride's payment flow. | No |

### v1SimpleRideOffer

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| dispatcher_offer_id | string | Mandatory. Supplier generated unique offer ID. | No |
| booking_estimated_price | [v1Price](#v1price) | Optional. Estimated price. | No |
| pickup_eta_seconds | [protobufUInt32Value](#protobufuint32value) | Optional. Estimated number of seconds until pickup.
For example: 60 seconds until the driver will pick the passenger up. | No |
| estimated_ride_duration_seconds | [protobufUInt32Value](#protobufuint32value) | Optional. Estimated number of seconds between pickup and dropoff. It does not include the time until pickup.
For example: ride duration is 20 minutes (20*60 = 1200 seconds). | No |

### v1SimpleRideOffers

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| offers | [ [v1SimpleRideOffer](#v1simplerideoffer) ] | Mandatory. A set of offers. | No |
| sub_supplier_details | [v1Supplier](#v1supplier) | Optional. Details of the sub-supplier. Used only for aggregated suppliers. | No |

### v1Supplier

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Optional. A unique supplier ID. | No |
| english_name | string | Mandatory. The name of the supplier, in English. | No |
| local_name | string | Optional. The name of the supplier in the local language. | No |
| logo_url | string | Optional. A URL pointing to a logo image of the supplier. | No |
| phone_number | string | Mandatory. The supplier’s telephone number. | No |
| website_url | string | Optional. URL of the supplier’s website. | No |

### v1SupplierCancelRideRequest

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Mandatory. Marketplace generated supplier ID. | No |
| ride_id | string | Mandatory. Marketplace generated ride ID. | No |
| cancel_reason | string | Optional. Cancellation reason. | No |
| cancel_reason_category | [SupplierCancelRideRequestSupplierCancelReasonCategory](#suppliercancelriderequestsuppliercancelreasoncategory) | Mandatory. Cancellation reason category. | No |
| update_id | string | Mandatory. Dispatcher-generated ID which uniquely identifies this update. | No |
| update_ts | dateTime | Mandatory. Dispatcher-generated timestamp which identifies the update time. | No |

### v1SupplierRideStatus

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Mandatory. Marketplace generated supplier ID. | No |
| ride_id | string | Mandatory. Marketplace generated ride ID. | No |
| status_code | [v1SupplierRideStatusRideStatus](#v1supplierridestatusridestatus) | Mandatory. Current status of the ride. | No |
| status_information | string | Optional. Additional information regarding the current state. | No |

### v1SupplierRideStatusRideStatus

RideStatus represents the different statuses a ride can be at.

 - UNKNOWN: Status is unknown.
 - ACCEPTED: Supplier confirmed the ride, but driver is not yet allocated.
 - DRIVER_ASSIGNED: Driver is allocated, but ride has not yet started.
 - DRIVER_EN_ROUTE: Ride started and driver is en-route.
 - AT_PICKUP: Driver has arrived to the pickup point, but passenger is not yet on board.
 - PASSENGER_ON_BOARD: Passenger is on board and ride to destination started.
 - AT_DROPOFF: Driver has arrived to the dropoff point.
 - COMPLETED: Ride complete and passenger disembarked.
 - CANCELED: Ride is cancelled (due to either supplier's or demander's request).

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1SupplierRideStatusRideStatus | string | RideStatus represents the different statuses a ride can be at.

 - UNKNOWN: Status is unknown.
 - ACCEPTED: Supplier confirmed the ride, but driver is not yet allocated.
 - DRIVER_ASSIGNED: Driver is allocated, but ride has not yet started.
 - DRIVER_EN_ROUTE: Ride started and driver is en-route.
 - AT_PICKUP: Driver has arrived to the pickup point, but passenger is not yet on board.
 - PASSENGER_ON_BOARD: Passenger is on board and ride to destination started.
 - AT_DROPOFF: Driver has arrived to the dropoff point.
 - COMPLETED: Ride complete and passenger disembarked.
 - CANCELED: Ride is cancelled (due to either supplier's or demander's request). |  |

### v1SupplierRideStatusUpdate

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Mandatory. Marketplace generated supplier ID. | No |
| ride_id | string | Mandatory. Marketplace generated ride ID. | No |
| status_code | [v1SupplierRideStatusUpdateRideStatus](#v1supplierridestatusupdateridestatus) | Mandatory. Current status of the ride. | No |
| status_information | string | Optional. Additional information regarding the current state. | No |
| update_id | string | Mandatory. Dispatcher-generated ID which uniquely identifies this update. | No |
| update_ts | dateTime | Mandatory. Dispatcher-generated timestamp which identifies the update time. | No |

### v1SupplierRideStatusUpdateRideStatus

RideStatus represents the different statuses a ride can be at.

 - UNKNOWN: Status is unknown.
 - ACCEPTED: Supplier confirmed the ride, but driver is not yet allocated.
 - DRIVER_ASSIGNED: Driver is allocated, but ride has not yet started.
 - DRIVER_EN_ROUTE: Ride started and driver is en-route.
 - AT_PICKUP: Driver has arrived to the pickup point, but passenger is not yet on board.
 - PASSENGER_ON_BOARD: Passenger is on board and ride to destination started.
 - AT_DROPOFF: Driver has arrived to the dropoff point.
 - COMPLETED: Ride complete and passenger disembarked.
 - CANCELED: Ride is cancelled (due to either supplier's or demander's request).

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| v1SupplierRideStatusUpdateRideStatus | string | RideStatus represents the different statuses a ride can be at.

 - UNKNOWN: Status is unknown.
 - ACCEPTED: Supplier confirmed the ride, but driver is not yet allocated.
 - DRIVER_ASSIGNED: Driver is allocated, but ride has not yet started.
 - DRIVER_EN_ROUTE: Ride started and driver is en-route.
 - AT_PICKUP: Driver has arrived to the pickup point, but passenger is not yet on board.
 - PASSENGER_ON_BOARD: Passenger is on board and ride to destination started.
 - AT_DROPOFF: Driver has arrived to the dropoff point.
 - COMPLETED: Ride complete and passenger disembarked.
 - CANCELED: Ride is cancelled (due to either supplier's or demander's request). |  |

### v1UnixTime

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| seconds_since_epoch | string (uint64) | Seconds since epoch UTC. | No |

### v1Vehicle

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| license_plate_number | string | Optional. The vehicle’s license plate number. | No |
| vehicle_type | [VehicleVehicleType](#vehiclevehicletype) | Optional. The vehicle's type (standard, limo, van). | No |
| make | string | Optional. The vehicle's make. | No |
| model | string | Optional. The vehicle's model. | No |
| color | string | Optional. The vehicle's color. | No |