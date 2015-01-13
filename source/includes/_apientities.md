## Entities

### Listing

The listing entity contains everything needed to fill out the property card on the Porch Home Report.

Field | Type | Required | Notes
---------- | ------- | ------- |---------
testEmail | string | no |
listingId | string | no |
listingStatus | string | no |
listingPrice | integer | no |
listingPriceCurrencyCode | string | no | `USD`
listingUrl | string | no |
listingDescription | string | no |
property | property entity | no |
provider | provider entity | no |
mls | mls entity | no |
brokerage | brokerage entity | no |
agents | agent entity | no |
photos | photo entity | no |

### Property

The property entity is the property characteristics of the home listed and the address entity.

Field | Type | Required | Notes
---------- | ------- | ------- |---------
address | address entity | no |
bedrooms | integer | no |
bathrooms | decimal | no |
propertyType | string | no |
sqftLiving | integer | no |
sqftLot | integer | no |
yearBuilt | string | no |
units | integer | no |

### Address

The address entity is the listings address information.  This is used for us to relate the listing with Porch’s Home Report data.

Field | Type | Required | Notes
---------- | ------- | ------- |---------
line1 | string | yes |
line2 | string | no |
city | string | yes |
state | string | yes |
postalCode | integer | yes |
county | string | no |
latitude | real | no |
longitude | real | no |
neighborhood | string | no |

### Provider

The provider entity is the provider of the current listing.  We will use the brokerage by default, but the provider can be something other than the current brokerage.

Field | Type | Required | Notes
---------- | ------- | ------- |---------
name | string | yes |
websiteUrl | string | no |

### MLS

The MLS entity is the MLS for the listing.

Field | Type | Required | Notes
---------- | ------- | ------- |---------
number | integer | yes |
name | string | no |

### Brokerage

The brokerage entity is the current brokerage for the current listing.

Field | Type | Required | Notes
---------- | ------- | ------- |---------
name | string | required
phoneNumber | string |
email | string |
websiteUrl | string |
logoUrl | string |
address | address entity |

### Agent

The agent entity is the listing agent(s) or referral agent(s) for a given listing.

Field | Type | Required | Notes
---------- | ------- | ------- |---------
name | string | yes |
title | string | no |
email | string | no |
websiteUrl | string | no |
profileUrl | string | no |
officeName | string | no |
officePhoneNumber | string | no |
photoUrl | string | no |
agentId | string | no | internal agent identifier
agentType | string | yes | `listing` or `referral`
receivePorchEmail | boolean | yes |

### Photo

The photo entity is a photo(s) of the property.

Field | Type | Required | Notes
---------- | ------- | ------- |---------
url | string | yes |
caption | string | no |
description | string | no |