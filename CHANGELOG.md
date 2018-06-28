## [3.0.0]
### New Features

- Extended backend app for adding/editing new/existing modules
- Import/Export from/to JSON functions in backend
- New Smarty functions and modifiers available for compiling dataLayers
  - `{dbquery}` query the database
  - `{*|request_get}` get request parameters
  - `[*|to_string}` force cast to string
- Added config fields for inline JS before/after GTM snippet

### Changes

- Moved GTM snippet after `<meta charset>` element if possible on Google's updated directive
- Optional compiling of dataLayers on `preDispatch` events via module setting
- Added/updated default dataLayers with values utilizing `{dbquery}` to fetch additional data for tracking
  - force cast `id` product numbers as strings
  - `category` on `impressions` when loaded through ajax infinite scrolling
  - `price` on `addToCart`
  - `id`, `price` and `quantity` on `removeFromCart`
- Smarty syntax-errors will be caught and will output within the dataLayer instead
- Refactored methods concerning dataLayer compiling into `wbm_tag_manager.variables` service
- Refactored event subscribers with streamlined injection
- Optionally drop database tables on uninstall

## [2.1.9]

- Values for fields in datalayer may now be longer than 255 characters

## [2.1.8]

- Bugfix for multiple array iterations

## [2.1.7]

- Use existing elements for noscript content to avoid regex mishaps in body

## [2.1.6]

- Fixes issues in combination with use of Shopware Advanced Cart (thanks @akkushopJK)

## [2.1.5]

- Support AddToCart Event for deactivated off-canvas basket

## [2.1.4]

- Option to deactive the integration by subshop

## [2.1.3]

- Fixes a bug with the conexco bootstrap theme's ajax filter and full page ajax requests

## [2.1.2]

- Adjusted AddTo/removeFrom basket events for e-commerce tracking

## [2.1.1]

- Check for set Container ID before dataLayer query

## [2.1.0]

- Refactored for Shopware 5.3

## [2.0.4]

- Fixed dataLayer structure for purchase tracking

## [2.0.3]

- Fixed dataLayer structure for detail product impressions

## [2.0.2]

- dataLayer Initialisierung vor GTM Script in Header

## [2.0.1]

- Use allowed modifier only since 5.2.25 in default config