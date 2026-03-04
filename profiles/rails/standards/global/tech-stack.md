## Tech stack

### Framework & Runtime
- **Application Framework:** Rails 8.1.1
- **Language/Runtime:** Ruby
- **Package Manager:** bundler

### Frontend
- **Rendering:** Server-rendered ERB with Turbo (Hotwire) for interactivity and Turbo Streams for realtime updates.
- **Client-side controllers:** Stimulus (ESM import maps) for lightweight behavior.
- **Styling:** Tailwind CSS 4; Lucide Icons.

### Database & Storage
- **Database:** PostgreSQL 17
- **ORM/Query Builder:** ActiveRecord
- **Caching:** SolidCache

### Testing & Quality
- **Test Framework:** RSpec
- **Linting/Formatting:** RuboCop

### Deployment & Infrastructure
- **Hosting:** TBD
- **CI/CD:** Kamal 2.0

### Third-Party Services
- **Authentication:** Devise
- **Email:** Resend (future scope)
- **Monitoring:** Grafana (future scope)
