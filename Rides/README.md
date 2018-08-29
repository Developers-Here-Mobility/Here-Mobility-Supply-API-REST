marketplace/public/grpc/supply_handler/vNext/supply_handler_rides_service.proto-REST
====================================================================================
**Version:** version not set

### /dispatch.rides.vNext/offer_requests
---
##### ***POST***
**Summary:** Request ride offers from the supplier

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [vNextGetSimpleRideOffersRequest](#vnextgetsimplerideoffersrequest) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [vNextSimpleRideOffers](#vnextsimplerideoffers) |

### /dispatch.rides.vNext/rides
---
##### ***POST***
**Summary:** Create a ride with the supplier

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| body | body |  | Yes | [vNextCreateSimpleRideRequest](#vnextcreatesimpleriderequest) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [vNextCreateSimpleRideResponse](#vnextcreatesimplerideresponse) |

### /dispatch.rides.vNext/rides/{ride_id}/demander_cancel
---
##### ***POST***
**Summary:** Update the supplier that the demander has cancelled the ride.

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [vNextDemanderCancelRideRequest](#vnextdemandercancelriderequest) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [vNextDemanderCancelRideResponse](#vnextdemandercancelrideresponse) |

### /dispatch.rides.vNext/rides/{ride_id}/status
---
##### ***GET***
**Summary:** Request the latest status of the ride from the supplier

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| supplier_id | query | Marketplace generated supplier id. | No | string |
| environment_type | query | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No | string |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [vNextSupplierRideStatus](#vnextsupplierridestatus) |

### /supply.rides.vNext/rides/{ride_id}/eta_update
---
##### ***POST***
**Summary:** Update the marketplace that estimated time to arrival to the origin and and to destination has changed
Recommended to update only when there is a major change (1 minute at least)

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [vNextRideEtaUpdate](#vnextrideetaupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [vNextEmpty](#vnextempty) |

### /supply.rides.vNext/rides/{ride_id}/location_update
---
##### ***POST***
**Summary:** Update the marketplace that the vehicle location has changed

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [vNextRideLocationUpdate](#vnextridelocationupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [vNextEmpty](#vnextempty) |

### /supply.rides.vNext/rides/{ride_id}/pickup_and_destination_update
---
##### ***POST***
**Summary:** Update the marketplace that the meeting pickup and destination points changed

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [vNextRidePickupAndDestinationUpdate](#vnextridepickupanddestinationupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [vNextEmpty](#vnextempty) |

### /supply.rides.vNext/rides/{ride_id}/price_update
---
##### ***POST***
**Summary:** Update the marketplace that the ride price has changed

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [vNextRidePriceUpdate](#vnextridepriceupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [vNextEmpty](#vnextempty) |

### /supply.rides.vNext/rides/{ride_id}/requested_pickup_time_update
---
##### ***POST***
**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [vNextRideRequestedPickupTimeUpdate](#vnextriderequestedpickuptimeupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [vNextEmpty](#vnextempty) |

### /supply.rides.vNext/rides/{ride_id}/status_update
---
##### ***POST***
**Summary:** Update the marketplace that the ride status changed

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [vNextSupplierRideStatusUpdate](#vnextsupplierridestatusupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [vNextEmpty](#vnextempty) |

### /supply.rides.vNext/rides/{ride_id}/supplier_cancel
---
##### ***POST***
**Summary:** Update the marketplace that the assigned supplier has cancelled the ride

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [vNextSupplierCancelRideRequest](#vnextsuppliercancelriderequest) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [vNextEmpty](#vnextempty) |

### /supply.rides.vNext/rides/{ride_id}/vehicle_and_driver_update
---
##### ***POST***
**Summary:** Update the marketplace that the assigned vehicle and driver have changed

**Parameters**

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| ride_id | path |  | Yes | string |
| body | body |  | Yes | [vNextRideVehicleAndDriverUpdate](#vnextridevehicleanddriverupdate) |

**Responses**

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 |  | [vNextEmpty](#vnextempty) |

### Models
---

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

### commonvNextLocation  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| point | [vNextPoint](#vnextpoint) | geographic coordinates (latitude, longtitude). | No |
| address | [vNextAddress](#vnextaddress) | description, state and zip code are optional, rest are mandatory. | No |
| free_text | string | Place name or street address in a free text format. | No |

### protobufUInt32Value  

Wrapper message for `uint32`.

The JSON representation for `UInt32Value` is JSON number.

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| value | long | The uint32 value. | No |

### vNextAddress  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| country | string | Localized country name. | No |
| country_code | string | ISO 3166-alpha-3 country code. | No |
| state | string | State (first subdivision level below the country, if relevant). | No |
| county | string | County (second subdivision level below the country, if relevant). | No |
| city | string | City/town. | No |
| district | string | District (subdivision level below the city). | No |
| sub_district | string | Sub-district (subdivision level below the district; e.g. commonly used in IND). | No |
| street | string | Street name. | No |
| house_number | string | House number; depending on regional characteristics, can also be house name. | No |
| postal_code | string | Postal code (zipcode). | No |
| building_name | string | Building name; e.g. commonly used in HKG. | No |
| line | [ string ] | Formatted address lines. | No |

### vNextCreateSimpleRideRequest  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace if of the supplier for which we want to create the ride. | No |
| ride_id | string | Marketplace generated ride id which will be used to identify this ride. | No |
| ride_details | [vNextSimpleRideDetails](#vnextsimpleridedetails) | Details of the ride creation request. | No |
| demander_id | string | additional fields for reporting and GDPR functionality. | No |
| demander_user_id | string |  | No |
| demander_product_id | string |  | No |
| environment_type | [vNextEnvironmentType](#vnextenvironmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### vNextCreateSimpleRideResponse  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| accepted_and_looking_for_driver | boolean (boolean) | Return true if ride was accepted and supplier is looking for a driver, or false if the ride is rejected. This call should return quickly and not wait for human confirmation. | No |
| pickup_eta | [vNextUnixTime](#vnextunixtime) | Estimated time of arrival to pickup. | No |
| booking_estimated_price | [vNextPrice](#vnextprice) | Estimated price. | No |

### vNextDemanderCancelRideRequest  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| cancel_reason | string | Cancellation reason. | No |
| environment_type | [vNextEnvironmentType](#vnextenvironmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### vNextDemanderCancelRideResponse  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| cancel_accepted | boolean (boolean) | true if cancellation went through, false it if ride cannot be cancelled. TBD: cancel and pay fee. | No |
| cancel_reason | string | in case cancellation failed, a textual reason explaining the cause. | No |

### vNextDriverDetails  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| driver_id | string | Mandatory. Unique Id of the driver in the dispatcher system. | No |
| name | string | Mandatory. Full name of the driver, in English. | No |
| phone | string | Mandatory. Phone number though which the driver is reachable. | No |
| picture_url | string | URL of a driver photo. | No |
| driving_license_id | string | Mandatory in some jurisdictions. License id of the driver. | No |

### vNextEmpty  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| vNextEmpty | object |  |  |

### vNextEnvironmentType  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| vNextEnvironmentType | string |  |  |

### vNextGetSimpleRideOffersRequest  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| request_id | string | Unique request id generated by the markeplace. | No |
| supplier_id | string | Marketplace ID of the supplier from which we want offers. | No |
| pickup | [commonvNextLocation](#commonvnextlocation) | Origin of the ride (pickup location). | No |
| destination | [commonvNextLocation](#commonvnextlocation) | Destination of the ride (dropoff location). | No |
| constraints | [vNextSimpleRideBookingConstraints](#vnextsimpleridebookingconstraints) | Constraints represent the requested ride parameters. | No |
| pickup_time | [vNextUnixTime](#vnextunixtime) | Pickup time. | No |
| environment_type | [vNextEnvironmentType](#vnextenvironmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### vNextPassengerDetails  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| name | string | Full name of the passenger. | No |
| phone_number | string | Phone number in full international format. | No |
| photo_url | string | Optional URL. | No |

### vNextPoint  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| lat | double | Latitude. | No |
| lng | double | Latitude. | No |

### vNextPrice  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| fixed | string (uint64) | Amount in cents. Fixed price means a price which the supplier commits to in advance. | No |
| lower_bound | string (uint64) | Amount in cents. Lower bound of an estimated price. | No |
| upper_bound | string (uint64) | Amount in cents. Lower bound of an estimated price. | No |
| currency | string | ISO 4217 code. | No |

### vNextRideEtaUpdate  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| eta_to_pickup | [vNextUnixTime](#vnextunixtime) | Updated estimated time till pickup.
NOTE: DEPRECATED soon - please use eta_to_pickup_seconds. | No |
| eta_to_destination | [vNextUnixTime](#vnextunixtime) | Updated estimated time till destination.
NOTE: DEPRECATED soon - please use eta_to_destination_seconds. | No |
| eta_to_pickup_seconds | [protobufUInt32Value](#protobufuint32value) | Updated estimated time till pickup in seconds. absolute time. | No |
| eta_to_destination_seconds | [protobufUInt32Value](#protobufuint32value) | Updated estimated time till destination in seconds. absolute time. | No |
| update_id | string | Dispatcher-generated id which uniquely identifies this update. | No |
| update_ts | dateTime | Dispatcher-generated timestamp which identifies the update time. | No |
| environment_type | [vNextEnvironmentType](#vnextenvironmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### vNextRideLocationUpdate  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| current_location | [vNextPoint](#vnextpoint) | Updated location of the vehicle. | No |
| update_id | string | Dispatcher-generated id which uniquely identifies this update. | No |
| update_ts | dateTime | Dispatcher-generated timestamp which identifies the update time. | No |
| environment_type | [vNextEnvironmentType](#vnextenvironmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### vNextRidePickupAndDestinationUpdate  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| pickup | [commonvNextLocation](#commonvnextlocation) | Updated pickup location. | No |
| destination | [commonvNextLocation](#commonvnextlocation) | Updated destination location. | No |
| eta_to_pickup | [vNextUnixTime](#vnextunixtime) | Updated estimated time of arrival to pickup.
NOTE: This field will be deprecated soon, please use eta_to_pickup_seconds instead. | No |
| eta_to_destination | [vNextUnixTime](#vnextunixtime) | Updated estimated time of arrival to destination
NOTE: This field will be deprecated soon, please use eta_to_destination_seconds instead. | No |
| update_id | string | Dispatcher-generated id which uniquely identifies this update. | No |
| update_ts | dateTime | Dispatcher-generated timestamp which identifies the update time. | No |
| environment_type | [vNextEnvironmentType](#vnextenvironmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |
| eta_to_pickup_seconds | [protobufUInt32Value](#protobufuint32value) | Updated estimated time till pickup in seconds. absolute time. | No |
| eta_to_destination_seconds | [protobufUInt32Value](#protobufuint32value) | Updated estimated time till destination in seconds. absolute time. | No |

### vNextRidePriceUpdate  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| booking_estimated_price | [vNextPrice](#vnextprice) | Updated estimated price. | No |
| actual_price | [vNextPrice](#vnextprice) | Updated actual price of the ride. | No |
| update_id | string | Dispatcher-generated id which uniquely identifies this update. | No |
| update_ts | dateTime | Dispatcher-generated timestamp which identifies the update time. | No |
| environment_type | [vNextEnvironmentType](#vnextenvironmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### vNextRideRequestedPickupTimeUpdate  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| prebook_pickup_time | [vNextUnixTime](#vnextunixtime) | New requested pickup time form the supplier. | No |
| update_id | string | Dispatcher-generated id which uniquely identifies this update. | No |
| update_ts | dateTime | Dispatcher-generated timestamp which identifies the update time. | No |
| environment_type | [vNextEnvironmentType](#vnextenvironmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### vNextRideVehicleAndDriverUpdate  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| vehicle | [vNextVehicle](#vnextvehicle) | Updated vehicle. | No |
| driver | [vNextDriverDetails](#vnextdriverdetails) | Updated driver. | No |
| update_id | string | Dispatcher-generated id which uniquely identifies this update. | No |
| update_ts | dateTime | Dispatcher-generated timestamp which identifies the update time. | No |
| environment_type | [vNextEnvironmentType](#vnextenvironmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### vNextSimpleRideBookingConstraints  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| passengers_no | long | Number of pasengers. | No |
| suitcases_no | long | Number of suitcases. | No |

### vNextSimpleRideDetails  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| pickup | [commonvNextLocation](#commonvnextlocation) | Origin of the ride. | No |
| destination | [commonvNextLocation](#commonvnextlocation) | Destination of the ride. | No |
| constraints | [vNextSimpleRideBookingConstraints](#vnextsimpleridebookingconstraints) | Special requests of the client. | No |
| passenger_details | [vNextPassengerDetails](#vnextpassengerdetails) | Details of the passenger. | No |
| pickup_time | [vNextUnixTime](#vnextunixtime) | Requested pickuo time. | No |
| passenger_note | string | Free-text comments by the passanger. | No |
| dispatcher_offer_id | string | Supplier generated unique offer ID. See SimpleRideOffer. | No |

### vNextSimpleRideOffer  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| dispatcher_offer_id | string | Supplier generated unique offer ID. Relevant only for selectable offers. | No |
| pickup_eta | [vNextUnixTime](#vnextunixtime) | Estimated pickup time.
NOTE: This field will be deprecated soon. please use pickup_eta_seconds instead. | No |
| dropoff_eta | [vNextUnixTime](#vnextunixtime) | Estimated dropoff time.
NOTE: This field will be deprecated soon. please use estimated_ride_duration_seconds instead. | No |
| booking_estimated_price | [vNextPrice](#vnextprice) | Estimated price. | No |
| pickup_eta_seconds | [protobufUInt32Value](#protobufuint32value) | Estimated pickup time in seconds. absolute time. | No |
| estimated_ride_duration_seconds | [protobufUInt32Value](#protobufuint32value) | Estimated dropoff time in seconds. absolute time. This is the time between pickup to dropoff. It does not contain the time to pickup. | No |

### vNextSimpleRideOffers  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| request_id | string | Set to the request_id received in the original GetSimpleRideOffersRequest. | No |
| is_selectable | boolean (boolean) | An offer is selectable if during ride creation, demander can ask for this specific offer to be used to create the ride. | No |
| offers | [ [vNextSimpleRideOffer](#vnextsimplerideoffer) ] | A set of offers. | No |
| supplier | [vNextSupplier](#vnextsupplier) | Details of the supplier. Given for aggregate suppliers. | No |

### vNextSupplier  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | A unique supplier ID. | No |
| english_name | string | The name of the supplier, in English. | No |
| local_name | string | Optional. The name of the supplier in the local language. | No |
| logo_url | string | Optional. A URL pointing to a logo image for the supplier. | No |
| phone_number | string | The supplier’s telephone number. | No |
| website_url | string | URL of the supplier’s website. | No |

### vNextSupplierCancelRideRequest  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| cancel_reason | string | Cancellation reason. | No |
| update_id | string | Dispatcher-generated id which uniquely identifies this update. | No |
| update_ts | dateTime | Dispatcher-generated timestamp which identifies the update time. | No |
| environment_type | [vNextEnvironmentType](#vnextenvironmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### vNextSupplierRideStatus  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| status_code | [vNextSupplierRideStatusRideStatus](#vnextsupplierridestatusridestatus) | Current status of te ride. | No |
| status_information | string | Additional information regarding the current state. | No |

### vNextSupplierRideStatusRideStatus  

RideStatus represents the different statuses a ride can be at.

 - UNKNOWN: Status is unknown.
 - ACCEPTED: Supplier confirmed the ride, but driver is not yet allocated.
 - DRIVER_ASSIGNED: Driver is allocated, but ride has not yet started.
 - DRIVER_EN_ROUTE: Drive started and driver is en-route.
 - AT_PICKUP: Driver is arrived at the pickup point, but passenger is not yet on board.
 - PASSANGER_ON_BOARD: Passenger is on board and drive to destination starterd.
 - COMPLETED: Ride complete and passenger disembarked.
 - CANCELED: Ride is cancelled (due to supplier or due to demander).

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| vNextSupplierRideStatusRideStatus | string | RideStatus represents the different statuses a ride can be at.

 - UNKNOWN: Status is unknown.
 - ACCEPTED: Supplier confirmed the ride, but driver is not yet allocated.
 - DRIVER_ASSIGNED: Driver is allocated, but ride has not yet started.
 - DRIVER_EN_ROUTE: Drive started and driver is en-route.
 - AT_PICKUP: Driver is arrived at the pickup point, but passenger is not yet on board.
 - PASSANGER_ON_BOARD: Passenger is on board and drive to destination starterd.
 - COMPLETED: Ride complete and passenger disembarked.
 - CANCELED: Ride is cancelled (due to supplier or due to demander). |  |

### vNextSupplierRideStatusUpdate  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| supplier_id | string | Marketplace generated supplier id. | No |
| ride_id | string | Marketplace generated ride id. | No |
| status_code | [vNextSupplierRideStatusUpdateRideStatus](#vnextsupplierridestatusupdateridestatus) | Current status of te ride. | No |
| status_information | string | Additional information regarding the current state. | No |
| update_id | string | Dispatcher-generated id which uniquely identifies this update. | No |
| update_ts | dateTime | Dispatcher-generated timestamp which identifies the update time. | No |
| environment_type | [vNextEnvironmentType](#vnextenvironmenttype) | Environment type. Generated per ride by the marketplace, and must be returned by dispatcher in all updates to the ride. | No |

### vNextSupplierRideStatusUpdateRideStatus  

RideStatus represents the different statuses a ride can be at.

 - UNKNOWN: Status is unknown.
 - ACCEPTED: Supplier confirmed the ride, but driver is not yet allocated.
 - DRIVER_ASSIGNED: Driver is allocated, but ride has not yet started.
 - DRIVER_EN_ROUTE: Drive started and driver is en-route.
 - AT_PICKUP: Driver is arrived at the pickup point, but passenger is not yet on board.
 - PASSANGER_ON_BOARD: Passenger is on board and drive to destination starterd.
 - COMPLETED: Ride complete and passenger disembarked.
 - CANCELED: Ride is cancelled (due to supplier or due to demander).

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| vNextSupplierRideStatusUpdateRideStatus | string | RideStatus represents the different statuses a ride can be at.

 - UNKNOWN: Status is unknown.
 - ACCEPTED: Supplier confirmed the ride, but driver is not yet allocated.
 - DRIVER_ASSIGNED: Driver is allocated, but ride has not yet started.
 - DRIVER_EN_ROUTE: Drive started and driver is en-route.
 - AT_PICKUP: Driver is arrived at the pickup point, but passenger is not yet on board.
 - PASSANGER_ON_BOARD: Passenger is on board and drive to destination starterd.
 - COMPLETED: Ride complete and passenger disembarked.
 - CANCELED: Ride is cancelled (due to supplier or due to demander). |  |

### vNextUnixTime  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| seconds_since_epoch | string (uint64) | Seconds since epoch UTC. | No |

### vNextVehicle  

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| license_plate_number | string | The vehicle’s license plate number. | No |
| vehicle_type | [VehicleVehicleType](#vehiclevehicletype) | The vehicle type (standard, limo, van). | No |
| make | string | The vehicle make. | No |
| model | string | The vehicle model. | No |
| color | string | The vehicle color. | No |