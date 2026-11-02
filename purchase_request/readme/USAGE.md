Purchase requests are accessible through a new menu entry 'Purchase
Requests', and also from the 'Purchase' menu.

Users can access the list of Purchase Requests or Purchase Request
Lines.

It is possible to filter requests by its approval status.

To find a request, type in the search bar of Purchase Requests and pick
one of the options in the dropdown:

- **Purchase Request**: the request reference, e.g. `PR00800`.
- **Product Description**: the Description text on the request lines.
  Use this when the real item is only written in the description, e.g.
  lines on a placeholder product.
- **Product**: the product on the request lines, by name or internal
  reference.
- **Source Document**: the Source Document field of the request.

Description, Product and Source Document searches are partial and
case-insensitive. Description and Product find a request when any of
its lines matches. Different options are combined with AND; several
values for the same option are combined with OR. The list opens
filtered to "My requests"; remove that filter to search everyone's
requests.

The Purchase Request Lines list offers the same Product Description,
Product and Source Document search options, applied to each line.

When transferring approved request lines to a new Purchase Order via the
"Make Purchase Order" wizard, each line shows a "Copy descriptions to new
PO" checkbox. It is pre-checked automatically only when the requester
edited the line's description away from the default text Odoo fills in
when a product is selected; lines still showing that default description
start unchecked.

- Unchecked lines: if the target PO already has a line for the same
  product and unit of measure, the quantity is added to that existing
  line instead of creating a new one.
- Checked lines: a new, separate PO line is always created so the
  requester's custom description is not lost or overwritten by an
  existing line.

Users can still tick or untick the checkbox manually before confirming
the wizard to override this default.
