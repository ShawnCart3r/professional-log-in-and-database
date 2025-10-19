WordPress Professional Registration & Verification System

A complete user registration and email verification system for healthcare professionals, built as a custom WordPress plugin.

Features

- Custom database architecture with proper indexing and table relationships
- Email verification flow with secure token generation and expiration handling
- Dual verification paths: login-based resend and public resend options
- Rate limiting to prevent abuse (10-minute cooldown on resend requests)
- WordPress authentication integration that blocks login until email is verified
- Admin dashboard with search, filtering, pagination, and CSV export
- Real-time dashboard widget showing registration stats and recent signups
- Secure by design: nonces, prepared statements, input sanitization throughout
- Smart duplicate handling for edge cases (existing emails, multiple registrations)

Technical Stack

- PHP 7.4+
- WordPress 5.8+
- MySQL with custom tables
- AJAX for seamless user experience
- WordPress authentication hooks

What I Built

This plugin handles the complete lifecycle of professional user registration:
1. Public registration form with validation
2. Custom Users table insertion with proper data normalization
3. WordPress user account creation with role assignment
4. Email verification token generation and delivery
5. Verification landing page with success/failure states
6. Login blocking until verification complete
7. Admin tools for user management and reporting

Key Challenges Solved

- Duplicate email handling: Safe upsert logic that handles edge cases
- Verification state management: Proper token lifecycle and cleanup
- Rate limiting: Prevents spam while allowing legitimate resends
- Security: Full nonce protection, SQL injection prevention, XSS mitigation
- UX: Clear error messages, resend flows, auto-redirect after verification

Admin Features

- Searchable user list with real-time filtering
- Verification status tracking
- One-click CSV export for reporting
- Dashboard snapshot widget with key metrics
- Bulk operations support

Built to handle real-world healthcare professional onboarding with HIPAA-aware data handling practices.
