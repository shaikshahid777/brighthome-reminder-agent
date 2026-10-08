# BrightHome Reminder Agent — Architecture

## Dynamic Context
The agent receives appointment-specific values through:
- customer_name
- appointment_date
- appointment_time
- service_type
- service_address
- reschedule_link

## Conversation Model
1. Load appointment context.
2. Personalize the greeting when the customer name is present; otherwise use a generic greeting.
3. Confirm the appointment details.
4. Handle confirmation, inability to attend, or rescheduling requests.
5. Provide the reschedule link when available.
6. Route missing-link follow-up to the office when no link is available.
7. Close professionally.

## Reliability Principles
- Never invent missing customer data.
- Gracefully handle missing dynamic variables.
- Do not read or fabricate a blank reschedule link.
- Preserve a professional, concise reminder experience.
