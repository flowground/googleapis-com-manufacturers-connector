# ![LOGO](logo.png) Manufacturer Center **flow**ground Connector

## Description

A generated **flow**ground connector for the Manufacturer Center API (version v1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/manufacturers/v1/swagger.json<br/>
Generated at: 2019-05-07T17:41:46+03:00

## API Description

Public API for managing Manufacturer Center related data.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Lists all the products in a Manufacturer Center account.

*Tags:* `accounts`

#### Input Parameters
* `include` - _optional_ - The information to be included in the response. Only sections listed here
will be returned.
* `pageSize` - _optional_ - Maximum number of product statuses to return in the response, used for
paging.
* `pageToken` - _optional_ - The token returned by the previous request.
* `parent` - _required_ - Parent ID in the format `accounts/{account_id}`.

`account_id` - The ID of the Manufacturer Center account.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Deletes the product from a Manufacturer Center account.

*Tags:* `accounts`

#### Input Parameters
* `name` - _required_ - Name in the format `{target_country}:{content_language}:{product_id}`.

`target_country`   - The target country of the product as a CLDR territory
                     code (for example, US).

`content_language` - The content language of the product as a two-letter
                     ISO 639-1 language code (for example, en).

`product_id`     -   The ID of the product. For more information, see
                     https://support.google.com/manufacturers/answer/6124116#id.
* `parent` - _required_ - Parent ID in the format `accounts/{account_id}`.

`account_id` - The ID of the Manufacturer Center account.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets the product from a Manufacturer Center account, including product<br/>
> issues.<br/>
> <br/>
> A recently updated product takes around 15 minutes to process. Changes are<br/>
> only visible after it has been processed. While some issues may be<br/>
> available once the product has been processed, other issues may take days<br/>
> to appear.

*Tags:* `accounts`

#### Input Parameters
* `include` - _optional_ - The information to be included in the response. Only sections listed here
will be returned.
* `name` - _required_ - Name in the format `{target_country}:{content_language}:{product_id}`.

`target_country`   - The target country of the product as a CLDR territory
                     code (for example, US).

`content_language` - The content language of the product as a two-letter
                     ISO 639-1 language code (for example, en).

`product_id`     -   The ID of the product. For more information, see
                     https://support.google.com/manufacturers/answer/6124116#id.
* `parent` - _required_ - Parent ID in the format `accounts/{account_id}`.

`account_id` - The ID of the Manufacturer Center account.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Inserts or updates the attributes of the product in a Manufacturer Center<br/>
> account.<br/>
> <br/>
> Creates a product with the provided attributes. If the product already<br/>
> exists, then all attributes are replaced with the new ones. The checks at<br/>
> upload time are minimal. All required attributes need to be present for a<br/>
> product to be valid. Issues may show up later after the API has accepted a<br/>
> new upload for a product and it is possible to overwrite an existing valid<br/>
> product with an invalid product. To detect this, you should retrieve the<br/>
> product and check it for issues once the new version is available.<br/>
> <br/>
> Uploaded attributes first need to be processed before they can be<br/>
> retrieved. Until then, new products will be unavailable, and retrieval<br/>
> of previously uploaded products will return the original state of the<br/>
> product.

*Tags:* `accounts`

#### Input Parameters
* `name` - _required_ - Name in the format `{target_country}:{content_language}:{product_id}`.

`target_country`   - The target country of the product as a CLDR territory
                     code (for example, US).

`content_language` - The content language of the product as a two-letter
                     ISO 639-1 language code (for example, en).

`product_id`     -   The ID of the product. For more information, see
                     https://support.google.com/manufacturers/answer/6124116#id.
* `parent` - _required_ - Parent ID in the format `accounts/{account_id}`.

`account_id` - The ID of the Manufacturer Center account.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-manufacturers-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
