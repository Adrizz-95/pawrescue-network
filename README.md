# PawRescue Network

See The Starting Prototype Here :
https://adrizz-95.github.io/pawrescue-network/dist/
Every dog deserves a way home. An English-language, open-source community platform, starting in **Valencia, Spain**, expanding municipality by municipality.

## Three goals

1. Photo reports for lost, found and suspected stolen dogs.
2. Nearby participating vets and rescue organisations, with confirmed intake availability.
3. Transparent donations to clearly identified beneficiaries.

## Current prototype

Dependency-free static HTML, CSS and JavaScript. Report filtering, search, photo upload, browser-local report creation, reunited status and reset are functional. Three fictional sample reports are included. All created reports and images are stored in localStorage on the current browser only. They are not submitted to a server or rescue team. Do not enter sensitive personal information. Donation and partner onboarding dialogs explain what remains to be connected; no payment or registration occurs.

Run `python3 -m http.server 8080 --directory dist` and open http://localhost:8080. No compilation required. Optional Google Fonts fall back to system fonts if unavailable.

## Municipality model for the production application

A shared platform with stable municipality IDs, country, display name, timezone and geographic boundaries. Valencia is the first active municipality; Mislata and Alboraia are future expansion options, not active chapters. Search across nearby municipalities should use distance and geographic data rather than administrative boundaries alone.

Planned entities: Municipality, DogReport, ReportPhoto, Organisation, IntakeAvailability, DonationBeneficiary and ModerationAction. Reports belong to a municipality. Organisations can serve multiple municipalities. Availability must expire or require reconfirmation; never infer capacity from opening hours.

## Production roadmap

- Authenticated accounts and server persistence; private contact relay.
- Moderated report submission, spam protection, abuse reporting and photo validation.
- Approximate public locations; restricted exact holding locations.
- Verified organisations, expiry of availability updates and geographic distance sorting.
- Clearly labelled suspected-theft reports without public accusations.
- Verified donation recipient and payment-provider integration; no card data stored by the app.
- Accessibility review, privacy documentation, retention/deletion flows and review of requirements before public launch.
- Repeatable municipal onboarding and translations beyond the initial English UI.

## GitHub setup

Create a public repository named `pawrescue-network`, then push this source tree. No GitHub repository has been created automatically. Hosting configuration in `.openai/` is specific to the prototype's deployment and can be removed for another host. Never commit personal reports, credentials, payment keys or user uploads.

## Contributing

See CONTRIBUTING.md. Code is available under the MIT license. Sample reports and dog illustrations were created for this prototype and do not represent real animals or affiliated organisations.
