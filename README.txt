Invoice & Quotation Manager – Professional PDF Layout

Updated:
- Uses the newly supplied authorized signature/seal image.
- Authorized Signature appears directly below Bank Details and Terms & Conditions.
- Signature image is displayed on a clean white background using its transparent PNG.
- All PDF text is bold for a stronger professional document appearance.
- Footer is pushed to the bottom/end of the A4 page.
- Existing invoice and quotation functionality is preserved.

Open index.html in a modern browser.


New functionality:
- Dashboard/landing page with website summary and live totals for created, pending, approved documents and saved products.
- Products are stored for future use and can be edited (including price, quantity, GST, code and optional image).
- Saved invoices and quotations start in Pending status.
- Pending records have a Pending button; clicking it changes the record to Approved and persists the status.
- Saved records can be edited and updated instead of creating a duplicate record.
- Pending/Approved filters are available on the Saved Invoices / Quotations page.
- Contact form on the dashboard stores enquiries in the browser.
- Existing PDF generation, company settings and signature/header assets are preserved.

Note: This is a browser-based website. Product/document/contact data is stored locally in the browser, not on a central server.


Jimco Exim default PDF layout update:
- The JIMCO EXIM default layout now uses the supplied full-page blue-and-white letterhead artwork.
- The Jimco logo/company name and contact details appear in the header; the Kochi address and GSTIN appear centered in the footer.
- The letterhead repeats on each PDF page, with document content placed between the header and footer.
- PRIME SOLUTIONS and KANNUR SAFETY layouts remain separate and unchanged.


Company-specific authorised signature:
- When Settings > Authorised Signature is set to JIMCO EXIM, the Jimco company seal and handwritten signature supplied by the user are displayed in the PDF.
- Other company selections continue to use the existing signature artwork.

Authorised signature selection:
- JIMCO EXIM: Jimco seal and handwritten signature
- PRIME SOLUTIONS: Prime Solutions seal
- KANNUR SAFETY: Kannur Safety Traders blue company seal


PDF canvas taint fix (offline-safe):
- Embedded all three authorised signature/seal PNGs directly as data URLs in app.js.
- This avoids loading relative file:// signature images into html2canvas, which can taint the canvas and make toDataURL() fail when the app is opened locally.
- Product images and uploaded custom layout images continue to be stored as data URLs.
- Cross-origin image URLs are still converted to data URLs when the remote server permits CORS; otherwise the individual remote image is skipped so PDF export can continue.
