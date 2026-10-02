# Software Architecture

## TimeBite Core iOS Product

Highest priority path: alpha -> TestFlight beta -> stable beta -> App Store v1 -> iteration.

Alpha must work locally:

- create and edit tasks
- organize by projects/goals
- set Daily Intent
- prioritize today's tasks
- start, pause, and complete timer sessions
- update Activity Ring/progress
- capture reflection
- persist locally with SwiftData or equivalent local-first store

TestFlight beta requires:

- reliable onboarding/account path if needed
- basic crash/error handling
- data migration confidence
- calendar import or lightweight calendar visibility
- speech-to-task capture
- clear beta feedback mechanism
- privacy messaging

App Store v1 requires:

- stable core loop
- resilient persistence and migration
- App Store-compliant auth/privacy
- accessible empty/error/loading states
- enough analytics or feedback to diagnose user flow issues
- no dependency on unfinished Meta, Unity, or charm work

## Shared Contracts

The app may own the first implementation of shared actions, but the action names and payloads live in `timebite-ecosystem`.

Experimental interfaces must adapt to the app contract. They should not force the production app to absorb unstable prototype logic.
