PDF.js 5.6.205 (legacy build) is included in pdfjs-bundle.js as plain scripts (no modules, blob or CDN loading) with its matching worker code. This is the only PDF.js version in the app.
PDF.js talks to that worker through a MessageChannel inside the page, or through a real Web Worker for very large files when the browser allows one.
Only OCR for scanned PDFs downloads tesseract.js from a CDN the first time it is needed.
