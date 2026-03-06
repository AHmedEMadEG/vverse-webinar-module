# V-Verse Webinar Module

This repository showcases my work on **the architecture and core frontend logic of the Webinar module**, developed as part of the **V-Verse SaaS platform**—a multi-module application with 15 product modules.

---

## Note on Repository Scope

This repository is intended as a **code and architecture showcase**, focusing on how key features are structured and implemented rather than providing a fully runnable application.

The code included here highlights the core logic, patterns, and components used to implement the feature within a larger production SaaS platform. Because of this, the repository may not run out-of-the-box if cloned, and certain dependencies, configurations, or integrations from the original application environment are intentionally omitted.

A **runnable demo version** of these features is planned for a future update. This will include a simplified environment with minimal setup (such as a basic landing page, dummy authentication flow, and sample data) allowing the features to be explored and executed locally.

---

## Features

- Webinar creation supporting multiple types:
  - Live
  - Automated
  - Hybrid

- Webinar waiting room with countdown timer

- Video playback synchronization for late attendees

- Real-time polls with live percentage updates

- Real-time chat between attendees

- Dynamic offers displayed during sessions

---

## Webinar Types

### Live Webinar

Users are redirected to an external live streaming platform to attend the session.

### Automated Webinar

A pre-recorded video uploaded by the host is automatically streamed to attendees at the scheduled time.

### Hybrid Webinar

A combination of automated video playback and live host interaction, allowing the host to join and engage with attendees while the session runs.

---

## Key Technical Concepts

### Video Synchronization

Attendees joining after the webinar has started are automatically synchronized with the current playback position.

The system determines the correct video timestamp by:

- calculating the elapsed time since the webinar start
- comparing it with the video duration
- starting playback from the appropriate timestamp

This ensures all participants remain aligned with the session timeline.

---

### Real-Time Polls

Participants can vote in polls during the webinar and instantly see updated results and voting percentages in real time.

---

### Countdown Waiting Room

Before the webinar begins, attendees enter a waiting room displaying a countdown timer until the scheduled start time.

---

## Tech Stack

- **Next.js**
- **TypeScript**
- **React**
- Real-time messaging (WebSockets / Firebase / similar services)
