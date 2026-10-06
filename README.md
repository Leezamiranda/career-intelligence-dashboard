# Career Intelligence Dashboard

## What It Does
A data pipeline and analytics tool that collects job postings from public 
job board APIs, normalizes skills and salaries, and tracks my own 
applications and contacts. It answers practical questions like which 
skills appear most in Strategy & Operations roles, or how often 
international companies ask for French or German.

## Why I Built This
I'm a CS student and operations leader moving into tech roles. I wanted 
to job search with data instead of guesswork, and I wanted a project that 
reflects how software actually gets built now: AI agents write much of 
the code, and the engineer's job is to define the problem, set the rules, 
and verify the output.

## How It's Built
This project is spec first, AI implemented, and human verified.

- **Specification before code.** A product requirements doc, an explicit 
  business rules doc, and architecture decision records come first.
- **Rules enforced in the database.** Application status transitions, 
  deduplication, and skill normalization are enforced with constraints 
  and covered by tests, not left to application code.
- **AI as implementer, not decision maker.** Code is written with Claude 
  Code against my specs and tests. Every change is reviewed before commit.
- **Corrections log.** I document every case where the AI got something 
  wrong and how I caught it.

## Tech Stack
- **Database:** PostgreSQL
- **Ingestion/ETL:** Python (requests, psycopg2), Greenhouse and Lever public APIs
- **Testing/CI:** pytest, GitHub Actions
- **Analysis:** SQL, Pandas
- **Visualization:** Streamlit
- **AI tooling:** Claude Code

## Project Status
🚧 In progress: specification phase

## Roadmap
- [ ] Product requirements and business rules documented
- [ ] Architecture decisions recorded
- [ ] Schema built with rule-enforcing constraints and tests
- [ ] Ingestion from Greenhouse, then Lever
- [ ] Skill normalization and cross-source deduplication
- [ ] CI running tests on every push
- [ ] Dashboard and case study write-up

## Repository Guide
- `docs/prd.md`: problem, scope, and success criteria
- `docs/business-rules.md`: the rules the system enforces
- `docs/adr/`: architecture decision records
- `docs/ai-corrections-log.md`: where the AI was wrong and how it was caught

## Key Findings
*Will populate once real posting data is flowing.*
