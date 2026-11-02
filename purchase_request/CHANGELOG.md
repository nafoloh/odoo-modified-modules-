# Changelog

## Unreleased

- Added "Product Description" (request line description) and "Source Document"
  search options to the Purchase Requests and Purchase Request Lines search
  views.

- Changed PO creation from purchase requests to sync the requested UoM onto the
  product's Purchase UoM first, then use that product value for the PO line.
- Added request-line and confirmation-time write-back so the product's Purchase
  UoM is updated before RFQ creation and reinforced when the PO is confirmed.
