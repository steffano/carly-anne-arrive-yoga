# Mission Control: Arrive Website Implementation

## Phase 0: SEO & Accessibility Foundation (Priority — Quick Wins)
- [x] Add `<meta name="description">` with compelling retreat summary
- [x] Add Open Graph tags (`og:title`, `og:description`, `og:image`, `og:url`, `og:type`) for social sharing previews
- [x] Add Twitter Card meta tags (`twitter:card`, `twitter:title`, `twitter:description`)
- [x] Add `<link rel="icon">` favicon (generate or source a small brand icon)
- [x] Remove `maximum-scale=1.0, user-scalable=no` from viewport meta (WCAG 2.1 AA violation)
- [x] Add `lang` attribute confirmation and semantic HTML audit (ensure single `<h1>` per page-view)

## Phase 1: Form Validation & Data Persistence
- [x] Connect `pricing-terms-check` checkbox to dynamically toggle `reserve-btn` disable state (already implemented via `toggleReserveButton()`)
- [x] Implement localStorage persistence for lead capture (`#quiz-name`, `#quiz-email`, `#quiz-spiritual-check`) — auto-populate on return visits
- [x] Standardize `showCustomAlert()` calls across all form submission steps (quiz, contact, checkout)
- [x] Add email format validation on `#quiz-email` and `#contact-email` beyond HTML `required`
- [x] Add defensive null-checks to all DOM-manipulating functions per rules.md

## Phase 2: FAQ Expansion & Animation Polish
- [x] Add FAQ: Dietary requirements & vegan/vegetarian/GF menu options
- [x] Add FAQ: Packing list recommendations for Costa Rica
- [x] Add FAQ: Refund & cancellation policy details
- [x] Replace hard `hidden` toggle in `toggleFAQ()` with animated CSS transitions (max-height or opacity+transform)
- [x] Ensure all 7 FAQ accordions work cleanly with exclusive-open behavior (close others when one opens)

## Phase 3: Dynamic Checkout & Stripe Integration
- [x] Populate `#stripe-checkout-modal` with full line-item breakdown (package name, each excursion, spa service + duration) matching the receipt sidebar
- [x] Add `id` attributes to all Stripe modal input fields (cardholder, card number, expiry, CVV)
- [x] Add client-side validation for Stripe modal fields (card number format, expiry date, CVV length)
- [x] Add clear "DEMO MODE" / "TEST CHECKOUT" indicator on the mock Stripe modal until real integration
- [x] Wire contact form (`handleContactSubmit`) to an external service (Formspree, Netlify Forms, or Google Forms) so messages are actually received

## Phase 4: Performance & Image Hardening
- [ ] Add `loading="lazy"` to all `<img>` tags in accommodations section
- [ ] Add `font-display=swap` parameter to Google Fonts `<link>` URL
- [ ] Replace external Unsplash URLs with self-hosted images or generate branded resort imagery
- [ ] Optimize the sacred geometry SVG animation for reduced GPU usage on mobile
- [ ] Consider obfuscating email/phone in contact section to reduce spam scraping

## Phase 5: UI Verification & Mobile QA
- [ ] Visual review of HUD header on mobile viewports (`< 640px`) — verify nav bar doesn't overflow
- [ ] Confirm `psychedelic-sunset-bg` non-repetitive vertical gradient rendering on all viewport heights
- [ ] Test all modal overlays (alert, terms, Stripe) on mobile — ensure scrollability and close buttons are reachable
- [ ] Verify quiz flow on mobile: lead form → questions → results → pricing scroll
- [ ] Cross-browser check: Chrome, Safari, Firefox (at minimum)

## Phase 6: Conversion Optimization (Post-Launch Enhancements)

- [ ] Add dynamic countdown timer to retreat date (August 2026)
- [ ] Add `IntersectionObserver`-based scroll-spy to highlight active nav section
- [ ] Add floating back-to-top button (appears on scroll)
- [ ] Improve quiz tie-breaking logic (3 questions = frequent ties between archetypes)
