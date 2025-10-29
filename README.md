TheraConnect – Professional Registration & Verification System

A full-featured WordPress plugin that provides secure registration, email verification, and admin management tools for healthcare professionals.
Built for real-world onboarding workflows, with an emphasis on security, data integrity, and user experience.

🚀 Overview

This plugin implements a complete lifecycle for professional user registration and verification — from public signup to administrative reporting — all within WordPress.
It’s designed to be maintainable, secure, and scalable while integrating seamlessly with existing authentication systems.

🧩 Core Features

Custom Database Architecture
Dedicated tc_users and tc_email_verify_pro tables with proper indexing, relationships, and self-healing schema logic.

Email Verification Workflow
Secure token generation and validation using HMAC hashing.
Verification links expire automatically once used.

Dual Verification Paths

Login-based Resend: for existing WP users who haven’t verified.

Public Resend: for users who registered but aren’t yet in the system.

Rate Limiting & Abuse Protection
10-minute cooldown between resend attempts, with nonces and hidden honeypots to deter bots.

Login Enforcement
WordPress authentication is blocked until the user’s email is verified.

Admin Dashboard
Searchable, filterable, paginated professional list with bulk delete and CSV export.

Dashboard Widget
At-a-glance view of total, verified, and unverified users plus recent signups.

Security by Design
Nonces, prepared statements, output escaping, and strict sanitization across all inputs.
Hashed verification tokens stored in the database (never plain text).

Duplicate-Safe Registration
Gracefully updates existing professional profiles when re-registered under the same email.

⚙️ Technical Stack

Language: PHP 7.4+

Platform: WordPress 5.8+

Database: MySQL (custom tables with schema validation)

Frontend: Minimal HTML/CSS + native WordPress forms

Integration: WordPress user authentication hooks & admin UI components

🧠 What This Plugin Does

Collects professional registration data via a secure public form

Normalizes and stores data in a custom table

Creates and links a WordPress user account

Sends an email verification link using a hashed token

Blocks unverified users from logging in

Provides admin tools for listing, filtering, and exporting user data

Displays key metrics via an admin dashboard widget

🛠️ Key Engineering Challenges Solved
Challenge	Solution
Duplicate Email Conflicts	Safe upsert logic ensures data consistency without breaking unique constraints
Token Lifecycle	HMAC-hashed token storage with single-use verification links
Rate Limiting	WordPress transients to throttle resend requests per email
Secure Data Flow	Nonces, prepared queries, sanitized inputs, and generic responses prevent enumeration
UX Smoothness	Simple, mobile-friendly forms and clear messaging for all states (register, verify, resend)
Database Integrity	Automatic schema creation and repair on activation or load
🔐 Security and Compliance Notes

Built with best-practice security for WordPress (nonces, sanitization, and limited capabilities).

Handles sensitive but non-PHI data safely.

HIPAA-aware, but not a certified HIPAA compliance solution.
Full HIPAA compliance requires specialized hosting and a Business Associate Agreement (BAA).

🧾 Admin Tools

Search, filter, and paginate professionals

Track verification status in real time

Export professional data to CSV

Perform bulk deletion safely (with nonce verification)

View registration statistics via dashboard snapshot widget

📦 Summary

The TheraConnect Professional Registration & Verification System provides a secure, scalable, and intuitive workflow for onboarding healthcare professionals inside WordPress.
It balances ease of use for admins and end users with strong security controls, built-in rate limiting, and verified access enforcement — ready for production environments that demand reliability and integrity.
