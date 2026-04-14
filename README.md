# WishList

ServiceNow scoped application for a **personal wish list**. Users track desired items with optional links and quantities, associated with a requester (`sys_user`).

| | |
| --- | --- |
| **Scope** | `x_snc_wishlist` |
| **Version** | 1.0.0 |
| **Primary table** | `x_snc_wishlist_wish_item` (Wish Item) |

## Data model

The **Wish Item** table includes:

- **Item** (string, required) — description of the wish
- **Request** (reference to `sys_user`, required) — who the wish belongs to
- **Quantity** (integer)
- **URL** (URL) — optional link to the product or page
- **Display Name** (string, read-only) — derived display label

There is an index on **Request** for lookups by user.

## Repository layout

Application metadata and update sets live under the folder named with the app’s `sys_id`:

- **`069f06f4831202107f4408006eda1eec/`** — application source (XML updates, dictionary, checksum)
- **`sn_source_control.properties`** — maps this repo to that folder (`path=069f06f4831202107f4408006eda1eec`)

Import and sync this repository from a ServiceNow instance using **Source Control** for the scoped application **WishList**.

## ServiceNow–generated content

Files under the app folder are produced by the platform. If imports fail because of checksum mismatches, merge issues, or edits made outside an instance, see the recovery notes in:

**[`069f06f4831202107f4408006eda1eec/README.md`](069f06f4831202107f4408006eda1eec/README.md)**
