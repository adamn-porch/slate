## Parameters

### Porch

These are used for porch tracking and other optional data

Parameter | Type | Required | Notes
---------- | ------- | ------- |---------
utm_source | partner_utm_source | yes | Value that defines the name of the partner that sent the user to porch.com.
utm_medium | `property-web` or `property-mobile` or `property-email` | yes | Identifies what referring medium–normal web page links should be "property-web"
utm_campaign | link_anchor_text | yes | Used to identify the link text on a given page.  For example "See Improvements".  This is used by porch to change our messaging to the user and improve conversion rates.
tid | homereport_partner_1_partner_2_website | yes | Porch specific identifier needed for internal tracking, provided by Porch.
test_email | string | no | if used, will send all outbound emails to specified account
brand_name | string | no | replaces the partner name with the brand_name
brand_logo_url | string | no | replaces the partner logo with the brand_logo_url

### Property

These are for the property characteristics of the home listed and the listing information.

Parameter | Type | Required | Notes
---------- | ------- | ------- |---------
property_url | string | no | url for the user to return to the listing after visiting porch.com
property_price | integer | no | current listing price of the property
property_beds | integer | no | number of bedrooms
property_baths | decimal | no | number of bathrooms
property_year_built | string | no | year property was built
property_type | string | no | type of property
property_sqft | integer | no | square foot living area of home
property_lot_sqft | integer | no | square foot lot of property
listing_date | string | no | date listing came on market

### Receiving Agent

These are for the referral agent for a given listing.

Parameter | Type | Required | Notes
---------- | ------- | ------- |---------
recv_agent_name | string | yes | name of agent
recv_agent_email | string | no | email of agent
recv_agent_website_url | string | no | url of agent's website
recv_agent_profile_url | string | no | url of agent's profile
recv_agent_office_nm | string | no | agent's office name
recv_agent_photo_url | string | no | photo url for agent
recv_agent_id | string | no | internal agent identifier
recv_agent_phone_number | string | no | contact phone number for agent

### Listing Agent

These are for the listing agent for a given listing.

Parameter | Type | Required | Notes
---------- | ------- | ------- |---------
listing_agent_nm | string | yes | name of agent
listing_agent_email | string | no | email of agent
listing_agent_advertiser_id | string | no | agent's advertiser identifier
listing_agent_photo_url | string | no | photo url for agent
listing_agent_phone_number | string | no | contact phone number for agent
listing_broker_nm | string | no | agent broker name
listing_broker_logo_url | string | no | agent broker logo url
listing_broker_phone_number | string | no | agent broker phone number