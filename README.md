[![](https://scdn.rapidapi.com/RapidAPI_banner.png)](https://rapidapi.com/package/Robin/functions?utm_source=RapidAPIGitHub_RobinFunctions&utm_medium=button&utm_content=RapidAPI_GitHub)

# Robin Package
Robin's API gives developers the power to interact with their team's data (locations, spaces, presence, etc.) and build third-party applications to extend Robin's capabilities..
* Domain: [robinpowered.com](https://robinpowered.com)
* Credentials: accessToken

## How to get credentials: 
1. Navigate to your [Robin dashboard](https://dashboard.robinpowered.com/rapidapi/settings/integrations).
2. Open Settings -> Integrations.
3. Click ```Generate new token```
 
## Robin.getOrganization
Get an organization's details.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID or slug (i.e. username) of the organization.

## Robin.getOrganizationLocations
Get all of an organization's locations.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID or slug (i.e. username) of the organization.
| query      | String     | Will filter by a specified location name.
| page       | Number     | The page of the result.
| perPage    | Number     | How many results are returned per page.

## Robin.createOrganizationLocation
Creates a new location for the organization.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID or slug (i.e. username) of the organization.
| name       | String     | The locations name.
| description| String     | The locations description.
| address    | String     | The street address of the location.
| image      | String     | A URL containing an image of the location.

## Robin.getOrganizationUsers
Get all of users in an organization

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID or slug (i.e. username) of the organization.
| query      | String     | Will filter by a specified user name.
| page       | Number     | The page of the result.
| perPage    | Number     | How many results are returned per page.
| ids        | String     | A comma separated list of IDs to retrieve.

## Robin.inviteOrganizationUser
Invites new users to an organization

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID or slug (i.e. username) of the organization.
| name       | String     | The name of the user to invite.
| email      | String     | The email of the user to invite.

## Robin.getOrganizationUser
Get details about an organization's user.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID or slug (i.e. username) of the organization.
| userId     | String     | The ID or slug of the user.

## Robin.getOrganizationAmenities
Get details about an organization's amenities.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID or slug (i.e. username) of the organization.

## Robin.createOrganizationAmenities
Create a new amenity for the organization.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID or slug (i.e. username) of the organization.
| name       | String     | The name of the amenity.

## Robin.getSingleUser
Gets a User resource.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID or slug of the user.

## Robin.getUserPresence
Gets a list of a User's presence history.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID or slug of the user.

## Robin.getUserEvents
Get a user's events.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID or slug of the user.

## Robin.getMe
Get the current authenticated user.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token

## Robin.getMePresence
Get the currently authenticated user's presence.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token

## Robin.getMeEvents
Get the currently authenticated user's events.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token

## Robin.getSingleLocation
Returns a Location resource, containing information about the location.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the location

## Robin.updateSingleLocation
Updates a Location resource.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the location
| name       | String     | The location name.
| description| String     | The location's description.
| address    | String     | The address of the location. When changed, the longitude and latitude will automatically be recalculated if the address is valid.
| image      | String     | A URL containing a photo of the location.

## Robin.getLocationSpaces
Get all of a location's spaces.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the location
| query      | String     | Will filter by a specified space name.
| page       | Number     | The page of the result.
| perPage    | Number     | How many results are returned per page.

## Robin.createLocationSpaces
Create a new space in the location.

| Field       | Type       | Description
|-------------|------------|----------
| accessToken | credentials| Your Robin access token
| id          | String     | The ID of the location
| name        | String     | The name of the space.
| description | String     | The space's description.
| image       | String     | A URL containing a photo of the space.
| capacity    | Number     | The maximum capacity of the space.
| type        | String     | The space type. Must be a valid type from the list that can be found on the space resource page.
| isAccessible| Boolean    | Whether the space meets accessibility requirements for the disabled. A false value means that it is unspecified, not that it does not meet the criteria.

## Robin.getLocationPresence
Get current presence for a location

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the location
| spaceIds   | String     | A comma separated list of space IDs to filter by.
| page       | Number     | The page of the result.
| perPage    | Number     | How many results are returned per page.

## Robin.addPresenceToLocation
Add presence to a space

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the location
| userId     | String     | The ID of the user who is present.
| deviceId   | String     | The ID of the device reporting the presence. This parameter is only required if user_ref is omitted.
| sessionTtl | Number     | How long to extend the presence session for, in seconds. If presence is posted with a TTL of 60 seconds and then again 120 seconds later, Robin will treat these as two separate sessions.

## Robin.deletePresenceToLocation
Expire a user or device's presence in a space

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the location
| userId     | String     | The ID of the user who is present.
| deviceId   | String     | The ID of the device reporting the presence. This parameter is only required if user_ref is omitted.

## Robin.getSingleSpace
Get details about a space.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the space to return.
| spaces     | String     | Optional submodel includes, such as calendar.

## Robin.updateSingleSpace
Update's the properties of an existing Space.

| Field          | Type       | Description
|----------------|------------|----------
| accessToken    | credentials| Your Robin access token
| id             | String     | The ID of the space to return.
| name           | String     | The name of space.
| description    | String     | The space's description.
| discoveryRadius| String     | A decimal number that specifies the distance in meters from a beacon that a person should be standing within to be counted as present in the space.
| capacity       | Number     | The maximum capacity for the space.
| image          | String     | A URL containing an image of the space.
| type           | String     | The space type. Must be a valid type from the list that can be found on the space resource page.
| isAccessible   | Boolean    | Whether the space meets accessibility requirements for the disabled. A false value means that it is unspecified, not that it does not meet the criteria.

## Robin.deleteSingleSpace
Permanently deletes a Space resource and all of it's related submodels, such as events.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the space to remove.

## Robin.getSpaceEvents
Get a list of a space's events.

| Field       | Type       | Description
|-------------|------------|----------
| accessToken | credentials| Your Robin access token
| id          | String     | The ID of the space
| after       | String     | Lower bound for an event's end property
| before      | String     | Upper bound for an event's start property
| creationType| Select     | Either automatic, manual or synced
| page        | Number     | The page to return
| perPage     | Number     | The amount of results to return per page

## Robin.createSpaceEvents
Book an event in a space

| Field        | Type       | Description
|--------------|------------|----------
| accessToken  | credentials| Your Robin access token
| id           | String     | The ID of the space
| title        | String     | A title for the event. If omitted, a title will be automatically generated from the space's name and the name of the user that is booking the event.
| startDate    | DatePicker | A composite datetime / timezone object that represents the start of the event.
| startTimeZone| String     | A valid IANA timezone identifier, such as America/New_York.
| endDate      | DatePicker | An ISO-8601 timestamp representing the end of the event.
| endTimeZone  | String     | A valid IANA timezone identifier, such as America/New_York.
| description  | String     | Description for event. Will show up in meeting invite.
| visibility   | String     | The visibility type. See the event resource page for a list of valid types.
| recurrence   | String     | An array RFC-5545 compliant content-lines that are of the type RRULE, RDATE, and EXDATE.
| invitees     | Array      | The invitees to invite.

## Robin.getSpaceAmenities
Get the amenities for a space.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the space

## Robin.getSingleAmenity
Get a specific amenity or check if an amenity exists in a space.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the space
| amenityId  | Number     | The amenity ID

## Robin.addAmenityToSpace
Adds an amenity to a space.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the space
| amenityId  | Number     | The amenity ID

## Robin.removeSpaceAmenity
Removes an amenity to a space.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the space
| amenityId  | Number     | The amenity ID

## Robin.getCurrentPresence
Get any current presence for a space

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the space
| query      | String     | Will filter by a specified space name
| page       | Number     | The page of the result
| perPage    | Number     | How many results are returned per page

## Robin.addPresenceToSpace
Add presence to a space

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the space
| userId     | String     | The ID of the user who is present.
| deviceId   | String     | The ID of the device reporting the presence. This parameter is only required if user_ref is omitted.
| sessionTtl | Number     | How long to extend the presence session for, in seconds. If presence is posted with a TTL of 60 seconds and then again 120 seconds later, Robin will treat these as two separate sessions.

## Robin.removePresenceFromSpace
Expire a user or device's presence in a space

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the space
| userId     | String     | The ID of the user who is present.
| deviceId   | String     | The ID of the device reporting the presence. This parameter is only required if user_ref is omitted.

## Robin.getSpaceDevices
Returns a list of devices that belong to the Space resource. This is indicative of hardware that is physically inside the space, such as a beacon, motion sensor, or projector.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the space
| manifest   | String     | When provided, results will be filtered by the specified device manifest
| page       | Number     | The page of the result
| perPage    | Number     | How many results are returned per page

## Robin.getStateAvailability
Gets the availability state for the space.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the space

## Robin.getSingleEvent
Get an event.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the event
| include    | String     | Optional submodel includes, such as confirmation and space.

## Robin.updateSingleEvent
Update's the properties of an existing Event.

| Field        | Type       | Description
|--------------|------------|----------
| accessToken  | credentials| Your Robin access token
| id           | String     | The ID of the event
| title        | String     | A title for the event. If omitted, a title will be automatically generated from the space's name and the name of the user that is booking the event.
| startDate    | DatePicker | A composite datetime / timezone object that represents the start of the event.
| startTimeZone| String     | A valid IANA timezone identifier, such as America/New_York.
| endDate      | DatePicker | An ISO-8601 timestamp representing the end of the event.
| endTimeZone  | String     | A valid IANA timezone identifier, such as America/New_York.
| description  | String     | Description for event. Will show up in meeting invite.
| visibility   | String     | The visibility type. See the event resource page for a list of valid types.
| recurrence   | String     | An array RFC-5545 compliant content-lines that are of the type RRULE, RDATE, and EXDATE.
| invitees     | Array      | The invitees to invite.

## Robin.getEventConfirmation
Gets the confirmation or checks if a confirmation exists for an event.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the event

## Robin.confirmEvent
Confirms an event.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the event
| deviceId   | Number     | Required if not authorized as a user.

## Robin.removeConfirmForEvent
Removes a confirmation for an event.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the event

## Robin.removeEvent
Cancels an event.

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| id         | String     | The ID of the event

## Robin.searchSpaces
Search space availability based on multiple parameters and get back results in a `Best Fit` order

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| locationIds| String     | One or more location IDs, separated by commas. Will include all spaces in the given locations in the result.
| spaceIds   | String     | One or more space IDs, separated by commas. Can be combined with location_ids
| after      | DatePicker | Lower bound for free-busy query, as a valid ISO8601 DateTime format.
| before     | DatePicker | Upper bound for free-busy query, as a valid ISO8601 DateTime format.
| duration   | Number     | The amount of time required between two events for a space to be considered `free`, as a valid ISO8601 DateTime period. (eg. `PT60M`)
| types      | String     | Comma separated space types. Unmatched spaces will be filtered out entirely.
| amenityIds | String     | Comma separated amenity IDs. Unmatched spaces will be filtered out entirely.
| query      | String     | Space name filter. Unmatched spaces will be filtered out entirely.
| minCapacity| String     | Filter for max space capacity. Unmatched spaces will be filtered out entirely.
| maxCapacity| String     | Filter for max space capacity. Unmatched spaces will be filtered out entirely.
| page       | Number     | The page to return.
| perPage    | Number     | The amount of results to return per page.

## Robin.getDeviceManifests
Get a list of supported device manifests

| Field      | Type       | Description
|------------|------------|----------
| accessToken| credentials| Your Robin access token
| page       | Number     | The page to return.
| perPage    | Number     | The amount of results to return per page.

