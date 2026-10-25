# Field-Service Mobile Engineering — WorkPilot
Flutter field workflows backed by a service-business and compliance platform.

## My ownership
Sole/lead engineering ownership across mobile and backend workflows, including jobs, reports, technical notes, media submissions and compliance workflows.

## The mobile problem
Field teams must be able to capture work when a connection is unavailable, understand what remains unsynchronized and recover when an API rejects a submission.

## Implementation
- Persist queued operations locally so pending submissions survive application restarts.
- Process job-status changes, reports, notes and media submissions in order.
- Expose pending counts, processing status, retry controls and blocking errors in the interface.
- Store large JSON payloads in application-support files rather than keeping every payload inline.
- Resume queue processing on initialization when online.
- Connect field workflows to the backend rather than treating mobile as an isolated interface.

This implementation does not claim exactly-once delivery or server-side idempotency guarantees.

## Product and stack
[WorkPilot](https://work-pilot.co) · Flutter/Dart · GetX · Dio · GetStorage · local file persistence · REST API integration

## What this demonstrates
Mobile/backend systems thinking, explicit failure and recovery states, and independent ownership of a field-service product.

## Evidence and confidentiality
Descriptive case study only; proprietary client source is not included. Existing screenshots are generic mockups, not verified production screenshots. Usage figures and measured business outcomes are not asserted.

[Portfolio](https://mehtadarshil.site) · [Profile](https://github.com/mehtadarshil)
