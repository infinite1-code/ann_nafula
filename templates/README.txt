ANN NAFULA G — MULTI-PAGE WEBSITE
index.html -> Profile.html -> Package.html -> Payment.html -> Success-1.html

Payment.html calls the existing Flask endpoints POST /api/donate and GET /api/status/<checkout_request_id>.
Profile details are stored in browser sessionStorage only, not a database.
Success is shown only after the backend reports status='success'.
The current in-memory backend transaction store may not work reliably on Vercel serverless; persistent storage is needed for production callback/status tracking.
